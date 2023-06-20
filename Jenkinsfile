def SANITIZED_BRANCH_NAME = env.BRANCH_NAME ? env.BRANCH_NAME.toLowerCase().replaceAll("/", "-") : "default-branch-name"
pipeline {
    agent any
     stages{
        stage("hello world develop") {
            steps {
                    if (env.BRANCH_NAME == 'develop') {
                        script {
                            sh 'whoami'
                        }
                        
                    }
            }
        }

        stage("hello world master") {
            steps {
                    if (env.BRANCH_NAME == 'master') {
                        script {
                            sh 'pwd'
                        }
                    }
            }
        }
    }
 }
