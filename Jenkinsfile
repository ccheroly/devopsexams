node {

stage('Clone Repository')
{
checkout scm
}

stage('Show me the files'){
sh "ls -l"
}

stage('Build docker image'){

sh "docker build -t ccheroly:latest ."
}

stage('Docker login to hub'){
sh "docker login -u 'ccheroly' -p '1Mdcccl3x3' "
}

stage('Apply docker tag ') {
sh "docker tag ccheroly:latest ccheroly/ccheroly:latest"
}
 stage('push the image') {
sh "docker push ccheroly/ccheroly:latest"
}
stage('Apply changes to the environment') {
sh "ls -l"
}


}
