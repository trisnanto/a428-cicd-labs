node {
  stage('Build') {
    sh 'node -v' 
    sh 'npm install' 
  }
  stage('Test') {
    sh './jenkins/scripts/test.sh'
  }
}

