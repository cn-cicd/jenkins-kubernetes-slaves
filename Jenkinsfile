{
    pipeline {
        agent any
        options {
            timestamps()
            skipDefaultCheckout()
        }
        triggers {
            pollSCM('H/3 * * * *')
        }
        stages {
            stage('Checkout') {
                steps {
                    checkout scm
                    stash includes: '**/*', name: 'repo-code'
                }
            }

            stage('Unit Tests') {
                agent {
                    label 'GRADLE_25_BUILDER'
                }
                steps {
                    unstash 'repo-code'
                    echo 'Unit Testing..'
                }
            }
        }
    }
}