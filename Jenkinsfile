pipeline {
    agent any
    //options {
        //skipDefaultCheckout true
    //}
    stages {
        stage('Build') {
            steps {
                //skipDefaultCheckout false
                sh("env")
                checkout scmGit(branches: [[name: '**']], extensions: [], userRemoteConfigs: [[refspec: "+${GIT_COMMIT}:refs/remotes/origin/${GIT_BRANCH}", url: 'https://github.com/rageshkrishna/test.git']])
                sh("echo Hello World!!")
            }
        }
    }
}
