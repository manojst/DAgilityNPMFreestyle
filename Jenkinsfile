def readfile;
node{
    stage('SCM Checkout'){
        
        git 'https://gitlab.training.dagility.com/manojkumar_gnanasekaran/dagilitynpmfreestyle'
    }
    stage('read package JSON'){
        readfile = readFile 'package.json';
    }
    stage('Compile-Package'){
        //Get maven home path
        //def npmHome = tool name: 'npm', type: 'npm'
        //sh "cd ${WORKSPACE}/dagilitynpmfreestyle;"
        sh "npm run build"        
    }
}
