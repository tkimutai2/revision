node {

stage('Clone Repository')
{
checkout scm
}


stage('Show me the files')
{
sh "ls -l"
}


stage('Build Docker Image and push image to DockerHub')

{
sh "docker build -t revision:version1 ."
}
  
stage('Docker login to hub and push the image'){
sh "docker login -u 'tkimutai1' -p 'Yamaha250'"
sh "docker tag revision:version1 tkimutai1/revision:version1"
sh "docker push tkimutai1/revision:version1"
}


stage('Apply changes to the environment')
{
sh "ls -l"
}




}
