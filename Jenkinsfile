node {

    checkout scm

    env.DOCKER_API_VERSION="1.23"
    env.KUBECONFIG="/root/.kube/config"
    tag = "${BUILD_NUMBER}"
    appName = "mynginx"
    imageName = "${appName}:latest"
    env.BUILDIMG=imageName
     stage "Build"
        sh "docker build -t ${imageName} -f myngnix/Dockerfile myngnix" 
     stage "Push"
        sh "docker login -u -p e"
        sh "docker tag ${imageName} kparashar/${imageName}"
        sh "docker push kparashar/${imageName}"
     stage "Deploy"
        sh "kubectl create -f  deploymet.yml"
}
