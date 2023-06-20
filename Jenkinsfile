def SANITIZED_BRANCH_NAME = env.BRANCH_NAME ? env.BRANCH_NAME.toLowerCase().replaceAll("/", "-") : "default-branch-name"
pipeline {
    agent any
    stages {
        stage("Declarative: Checkout SCM") {
            steps {
                checkout scm
            }
        }

        stage("hello world develop") {
            steps {
                script {
                    sh "git branch -a" // Add this line to check the current branch
                    echo "Branch Name: ${env.BRANCH_NAME}"
                    if (env.BRANCH_NAME == 'develop') {
                        sh "whoami"
                    }
                }
            }
        }

        stage("hello world master") {
            steps {
                script {
                    sh "git branch -a" // Add this line to check the current branch
                    echo "Branch Name: ${env.BRANCH_NAME}"
                    if (env.BRANCH_NAME == 'master') {
                        sh "pwd"
                    }
                }
            }
        }
    }
}
