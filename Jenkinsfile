node {
    checkout scm

        def customImage = docker.build("nginximage")
        customImage.withRun(' -p 80:80')
        //docker.image('nginximage:0.1').withRun('-p 80:80')
}
