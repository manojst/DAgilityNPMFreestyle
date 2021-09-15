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
             }
         }
         stage('Build') {
             steps {
                 sh 'npm run build'                
             }
         }
    }
}
