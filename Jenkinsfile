#!groovy
node {
  checkout(
    [
      $class: 'GitSCM', 
      branches: [[name: '*/react-app']], 
      extensions: [], 
      userRemoteConfigs: [[url: '/home/Documents/Apps/a428-cicd-labs']]
    ]
  )
  stage('Build') {
    sh 'docker inspect -f . node:16-buster-slim'
    sh 'docker pull node:16-buster-slim'
    sh 'docker run -t -d -u 1000:1000 -p 3000:3000 -w /var/jenkins_home/workspace/submission-cicd-pipeline-trisnanto -v /var/jenkins_home/workspace/submission-cicd-pipeline-trisnanto:/var/jenkins_home/workspace/submission-cicd-pipeline-trisnanto:rw,z -v /var/jenkins_home/workspace/submission-cicd-pipeline-trisnanto@tmp:/var/jenkins_home/workspace/submission-cicd-pipeline-trisnanto@tmp:rw,z -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** node:16-buster-slim cat'
    sh 'docker top e204f005d5f5ab9be69397b3bd53244cfbe1ae2892a7fd504512f74c0177b2eb -eo pid,comm'
    sh ''
    sh ''
    sh ''
    sh ''
    sh ''
    sh ''
    sh ''
    sh ''
    sh ''

    sh 'node -v' 
    sh 'npm install' 
  }
  stage('Test') {
    sh './jenkins/scripts/test.sh'
  }
}

