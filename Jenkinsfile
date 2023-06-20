def SANITIZED_BRANCH_NAME = env.BRANCH_NAME ? env.BRANCH_NAME.toLowerCase().replaceAll("/", "-") : "default-branch-name"

pipeline {
    agent any
    stages {
        stage("whomai develop") {
            steps {
                    if (env.BRANCH_NAME == 'develop') {
                        sh 'whoami'
                    }
            }
        }

        stage("pwd master") {
            steps {
                    if (env.BRANCH_NAME == 'master') {
                        sh 'pwd'
                    }
            }
        }
    }
}

