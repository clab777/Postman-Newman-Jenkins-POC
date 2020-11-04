pipeline {
    agent any
    environment { 
      HOME="."
      NPM_CONFIG_PREFIX="${pwd()}/.npm-global"
      PATH="$PATH:${pwd()}/.npm-global/bin:${pwd tmp: true}/.npm-global/bin"
    }
    withEnv(["PATH=$PATH", /*or*/ "PATH=${PATH}", /*or*/ "PATH+NPM=${pwd()}/.npm-global/bin:${pwd tmp: true}/.npm-global/bin"]) {
      stages {
        stage('NPM Config') {
          steps { 
              sh 'npm install'
          }
        }
        stage('Run Tests') {
            steps {
                sh 'npm api-tests-prod'
            }
        }
      }
    }
  }
