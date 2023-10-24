pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                checkout scmGit(branches: [[name: '**']], extensions: [], userRemoteConfigs: [[refspec: 'foo', url: 'https://github.com/rageshkrishna/test.git']])
                sh("echo Hello World!!")
            }
        }
    }
}
