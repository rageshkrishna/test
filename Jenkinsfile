pipeline {
    agent any
    //options {
        //skipDefaultCheckout true
    //}
    stages {
        stage('Build') {
            steps {
                script {
                    //skipDefaultCheckout false
                    echo currentBuild.getBuildCauses().toString()
                    echo "Changesets"
                    echo currentBuild.changeSets.toString()
                    echo "Changesets[0]"
                    echo currentBuild.changeSets[0].toString()
                    echo "Changesets.getLogs"
                    echo currentBuild.changeSets[0].getLogs().toString()
                    echo "Changesets.getLogs[0]"
                    echo currentBuild.changeSets[0].getLogs()[0].toString()
                }
                sh("env")
                checkout scmGit(branches: [[name: '**']], extensions: [], userRemoteConfigs: [[refspec: "+${GIT_COMMIT}:refs/remotes/origin/${GIT_BRANCH}", url: 'https://github.com/rageshkrishna/test.git']])
                sh("echo Hello World!!")
            }
        }
    }
}
