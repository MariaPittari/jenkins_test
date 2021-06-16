pipeline {
  agent {
        docker { image 'node:14-alpine' }
    }
  stages {
    stage("build") {
      steps {
        sh """
          docker build -t nginx_image .
        """
      }
    }
    stage("run") {
      steps {
        sh """
          docker run --rm nginx_image
        """
      }
    }
  }
}
