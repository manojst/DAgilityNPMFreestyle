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
                 sh 'sudo yum install -y nodejs'
                 sh 'node --version' 
                 sh 'npm -version'
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
