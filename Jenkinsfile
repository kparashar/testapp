node {
   
    checkout scm
   
    env.DOCKER_API_VERSION="1.23"
    tag = "${BUILD_NUMBER}"
    appName = "mynginx"
    imageName = "${appName}:latest"
    env.BUILDIMG=imageName
   
     stage "Build"

        sh "docker build -t ${imageName} myngnix/Dockerfile" 
     
     stage "Push"
        sh "docker login -u kparashar -p Se1fc@re"
        sh "docker tag ${imageName} kparashar/${imageName}"
        sh "docker push kparashar/${imageName}"

     stage "Deploy"
        sh "kubectl apply -f  deploymet.yml"
}
