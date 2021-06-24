node {
    checkout scm
    stage('Build'){
        def customImage = docker.build("nginximage")
    }     
    stage('Test'){
        docker.image('nginximage:0.1').withRun(){
    sh "docker run -p 80:80 --name nginx nginximage"}
    }
}
