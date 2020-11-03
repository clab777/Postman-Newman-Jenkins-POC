node{
  stage('Postman Tests'){
    git https://github.com/clab777/Postman-Newman-Jenkins-POC.git
    sh 'npm install'
    sh 'npm api-tests-prod'
  }
}
