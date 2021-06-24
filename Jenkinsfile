node {
    checkout scm
    stage('Build'){
        def customImage = docker.build("nginximage")
    }     
    stage('Test'){
        customImage.withRun(){
    sh "docker run -p 80:80 --name nginx customImage"}
    }
}
