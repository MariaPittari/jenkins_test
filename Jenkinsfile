node {
    checkout scm

        def customImage = docker.build("nginximage")
      
        docker.image('nginximage:0.1').withRun('-p 80:80')
}
