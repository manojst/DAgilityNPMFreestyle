pipeline {
    agent {label 'chrome'}
    tools { 
          nodejs "NodeJS"
        }

    environment {
        CI = 'true'
        }
    stages {
         stage('Required dependancies') {
             steps {
                 sh 'npm install'
                 sh 'node --version' 
                 sh 'npm -version'
                 sh 'npm init'
                 sh 'npm i node-sass nodemon browserify --save-dev'
             }
         }
         stage('Test') {
             steps {
                 sh 'chmod +x ./jenkins/scripts/test.sh'
                 sh './jenkins/scripts/test.sh'
             }
         }
         stage('Build') {
             steps {
                 sh 'npm run build'
                
             }
         }
    }
}
