node('docker') {
    stage 'start mvn'
    
    docker.image('maven:3-alpine').inside {
            sh "mvn --version"
        }
    
    stage 'start pwd'
    
    docker.image('maven:3-alpine').inside {
            sh "pwd"
        }
    
    }
}
