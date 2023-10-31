pipeline {
    agent any
    //options {
        //skipDefaultCheckout true
    //}
    stages {
        stage('Build') {
            steps {
                //skipDefaultCheckout false
                def build = Thread.currentThread()?.executable
                //def svn_branch = build.buildVariableResolver.resolve("SVN_BRANCH")
                
                if (build instanceof AbstractBuild){
                    def workspace = build.workspace
                    //def job = build.parent
                    def scm = build.parent.scm;
                    println "scm: $scm"
                }
                sh("env")
                checkout scmGit(branches: [[name: '**']], extensions: [], userRemoteConfigs: [[refspec: "+${GIT_COMMIT}:refs/remotes/origin/${GIT_BRANCH}", url: 'https://github.com/rageshkrishna/test.git']])
                sh("echo Hello World!!")
            }
        }
    }
}
