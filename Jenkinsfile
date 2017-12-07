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
                echo 'Running on Master - Unit Testing..'
                sh 'uname -a'
                sh 'java -version'
                sh 'javac -version'
                sh 'mvn -version'
                sh 'node --version'
                stash includes: '**/*', name: 'repo-code'
            }
        }
        stage('Unit Tests') {
            agent {
                label 'GRADLE_25_BUILDER'
            }
            steps {
                unstash 'repo-code'
                echo 'Running on JNLP Slave Java Tools - Unit Testing..'
                sh 'uname -a'
                sh 'java -version'
                sh 'javac -version'
                sh 'mvn -version'
                sh 'node --version'
            }
        }
    }
}