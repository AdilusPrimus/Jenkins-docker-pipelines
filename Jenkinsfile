pipeline {
    agent none
    stages {
        stage('Back-end') {
            agent {
                docker { 
                    image 'maven:3-alpine'
                    args '-v maven-home:/root/.m2'
                }
            }
            steps {
                git url: 'https://github.com/WebGoat/WebGoat.git'               
                sh 'mvn clean install'
                sh 'pwd'
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
