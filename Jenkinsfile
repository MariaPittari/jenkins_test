node {
    checkout scm

    docker.withRegistry('http://0.0.0.0:5000/v2') {

        def customImage = docker.build("nginximage")

        /* Push the container to the custom Registry */
        customImage.push()
      
        docker.image('nginximage:0.1').withRun('-p 80:80')
    }
}
