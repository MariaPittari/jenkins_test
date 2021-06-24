node {
    checkout scm
    stage('Build'){
        def customImage = docker.build("nginximage")
    }     
    stage('Test'){
        docker.image('nginximage:0.1').withRun(" -p 80:80")
    }
}
