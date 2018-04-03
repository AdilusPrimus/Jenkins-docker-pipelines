pipeline {
    agent {
        def alpine-image = docker { image 'node:7-alpine' }
    }
    stages {
        stage('Test') {
            steps {
                sh 'node --version'
            }
        }
        stage('PWD') {
            steps {
                alpine-image.inside {
                    sh 'pwd'
                }
            }
        }        
    }
}
