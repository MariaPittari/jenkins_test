node {
    checkout scm

    docker.withRegistry('localhost:5000', 'dockerHub') {

        def customImage = docker.build("prova/nginximage")

        /* Push the container to the custom Registry */
        customImage.push()
      
        docker.image('nginximage:0.1').withRun('-p 80:80')
    }
}
