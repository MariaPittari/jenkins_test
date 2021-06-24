node {
    checkout scm
    stage('Build'){
        def customImage = docker.build("nginximage")
    }     
    stage('Test'){
        docker.image("nginximage:latest").withRun(){
    sh "docker rm nginx && docker run -d -p 80:80 --name nginx nginximage:latest"}
    }
}
