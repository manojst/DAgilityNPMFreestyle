pipeline {
  agent any {    
    stage('Git') {
      steps {
        git 'https://gitlab.training.dagility.com/manojkumar_gnanasekaran/dagilitynpmfreestyle.git'
      }
    }     
    stage('Build') {
      steps {
        sh 'npm install'
      }
    }                  
    stage('Test') {
      steps {
        sh './jenkins/scripts/test.sh'
      }
    }  
  }
}
