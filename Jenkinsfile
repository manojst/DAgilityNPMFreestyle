def readfile;
node{
    stage('SCM Checkout'){
        
        git 'https://gitlab.training.dagility.com/manojkumar_gnanasekaran/dagilitynpmfreestyle'
    }
    stage('read package JSON'){
        readfile = readFile 'package.json';
    }
    withNPM(npmrcConfig: 'my-custom-nprc') {
        sh "npm install"
        sh "npm run build"
    }
}
