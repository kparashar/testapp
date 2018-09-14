node {
<<<<<<< HEAD
   
    checkout scm
   
=======
    
    checkout scm
    
>>>>>>> cf4e053d3898bdd64c97b5e119401d89908f3372
    env.DOCKER_API_VERSION="1.23"
    tag = "${BUILD_NUMBER}"
    appName = "mynginx"
    imageName = "${appName}:latest"
    env.BUILDIMG=imageName
   
     stage "Build"

<<<<<<< HEAD
        sh "docker build -t ${imageName} myngnix/Dockerfile" 
=======
        sh "docker build -t ${imageName} Dockerfile" 
>>>>>>> cf4e053d3898bdd64c97b5e119401d89908f3372
     
     stage "Push"
        sh "docker login -u kparashar -p Se1fc@re"
        sh "docker tag ${imageName} kparashar/${imageName}"
        sh "docker push kparashar/${imageName}"

     stage "Deploy"
        sh "kubectl apply -f  deploymet.yml"
}
