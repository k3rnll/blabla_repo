pipeline {
    agent {
        label 'java17'
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            agent {
                docker {
                    image 'gradle:8.2.0-jdk17-alpine'
                    reuseNode true
                }
            }
            steps {
                sh 'gradle --version'
            }
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
