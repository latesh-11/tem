def getBranchName() {
    return sh(script: 'git rev-parse --abbrev-ref HEAD', returnStdout: true).trim()
}

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
                    def branchName = getBranchName()
                    echo "Branch Name: ${branchName}"
                    if (branchName == 'develop') {
                        sh "whoami"
                    }
                }
            }
        }

        stage("hello world master") {
            steps {
                script {
                    def branchName = getBranchName()
                    echo "Branch Name: ${branchName}"
                    if (branchName == 'master') {
                        sh "pwd"
                    }
                }
            }
        }
    }
}
