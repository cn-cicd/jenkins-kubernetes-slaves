podTemplate(
    label: 'GRADLE_25_BUILDER',
    containers: [
        containerTemplate(name: 'gradle', image: 'gradle', ttyEnabled: true, command: 'cat')
    ],
    volumes: [
        hostPathVolume(mountPath: '/var/run/docker.sock', hostPath: '/var/run/docker.sock'),
    ]
) 
{
    node('GRADLE_25_BUILDER') {

        stage('Checkout Workspace') {
            container('gradle') {
                steps {
                   checkout scm
                   stash includes: '**/*', name: 'repo-code'
                }
            }
        }
        stage('Unit Test') {
            steps {
                unstash 'repo-code'
                echo 'Unit Testing..'
            }
        }
        stage('Build') {
            steps {
                unstash 'repo-code'
                echo 'Building..'
            }
        }
        stage('E2E Test') {
            steps {
                unstash 'repo-code'
                echo 'E2E Testing..'
            }
        }
        stage('Deploy') {
            steps {
                unstash 'repo-code'
                echo 'Deploying....'
            }
        }
    }
}
