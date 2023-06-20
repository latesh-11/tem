def SANITIZED_BRANCH_NAME = env.BRANCH_NAME ? env.BRANCH_NAME.toLowerCase().replaceAll("/", "-") : "default-branch-name"
pipeline {
    agent any
     stages{
        stage("hello world develop"){
             steps{
                script {
                    if (env.BRANCH_NAME == 'develop') {
                        echo 'hello world develop'
                    }
                }
             }
        }
     
        stage("hello world master"){
             steps{
                script {
                    if (env.BRANCH_NAME == 'master') {
                        echo 'hello world master'
                    }
                }
             }
        }

     }
 }
