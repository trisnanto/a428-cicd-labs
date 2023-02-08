#!groovy
node {
  stage('Checkout Test') {
    sh 'ls'
    sh 'git init /var/jenkins_home/workspace/submission-cicd-pipeline-trisnanto # timeout=10'
  }
  checkout(
    [
      $class: 'GitSCM', 
      branches: [[name: '*/react-app']], 
      extensions: [], 
      userRemoteConfigs: [[url: '/home/Documents/Apps/a428-cicd-labs']]
    ]
  )
  stage('Build') {
    sh 'node -v' 
    sh 'npm install' 
  }
  stage('Test') {
    sh './jenkins/scripts/test.sh'
  }
}

