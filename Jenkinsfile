node() {
    
    /*
    stage 'start mvn'
    
    docker.image('maven:3-alpine').inside {
            sh "mvn --version"
        }
    
    stage 'start pwd'
    
    docker.image('maven:3-alpine').inside {
            sh "pwd"
        }
   */
    
  def maven = docker.image('maven:3-alpine'); // https://registry.hub.docker.com/_/maven/

  stage('Mirror') {
    // First make sure the slave has this image.
    // (If you could set your registry below to mirror Docker Hub,
    // this would be unnecessary as maven.inside would pull the image.)
    maven.pull()
  }
    
}
