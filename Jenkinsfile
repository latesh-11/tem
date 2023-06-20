def SANITIZED_BRANCH_NAME = env.BRANCH_NAME ? env.BRANCH_NAME.toLowerCase().replaceAll("/", "-") : "default-branch-name"
pipeline {
    agent any
    stages {
        stage("hello world develop") {
            when {
                if { env.BRANCH_NAME == 'develop' }
            }
            steps {
                echo 'hello world develop'
            }
        }
        
        stage("hello world master") {
            when {
                if { env.BRANCH_NAME == 'master' }
            }
            steps {
                echo 'hello world master'
            }
        }
    }
}
