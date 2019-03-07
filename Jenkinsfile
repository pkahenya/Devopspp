node {

stage('Clone Repository')
{
checkout scm
}

stage('Show me the files'){
sh "ls -l"
}

stage('Build docker image'){

sh "docker build -t devopsp:latest ."
}

stage('Docker login to hub and push the image'){
sh "docker login -u 'pkkahenya' -p '91674Petenimnoma' "
sh "docker tag devopsp:latest pkkahenya/devopsp:latest"
sh "docker push 91674Petenimnoma/devopsp:latest"
}

stage('Apply changes to the environment') {
sh "ls -l"
}


}
