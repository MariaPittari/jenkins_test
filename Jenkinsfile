node {
    checkout scm

    docker.withRegistry('https://registry.hub.docker.com', 'dockerHub') {

        def customImage = docker.build("nginximage:0.1")

        /* Push the container to the custom Registry */
        customImage.push()
      
        docker.image('nginximage:0.1').withRun('-p 80:80')
    }
}
