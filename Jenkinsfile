pipeline {
    agent none
    
    def maven = docker.image('maven:3-alpine')
    
    stages {
        stage('Back-end') {
            agent {
                /* def maven-image = docker { 
                    image 'maven:3-alpine'
                    args '-v maven-home:/root/.m2'
                }
                */
                maven.pull()
            }
            steps {
                maven.inside { 
                    sh 'pwd'
                }
                /*
                git url: 'https://github.com/WebGoat/WebGoat.git'
                sh 'mvn clean install --fail-never'
                */
            }
        }
        stage('Front-end') {
            agent {
                docker { image 'node:7-alpine' }
            }
            steps {
                sh 'node --version'
            }
        }
    }
}
