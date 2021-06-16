pipeline {
  agent any
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
