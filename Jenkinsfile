// def SANITIZED_BRANCH_NAME = env.BRANCH_NAME.toLowerCase().replaceAll("/", "-")
pipeline {
    agent any
     stages{
        stage("hello test"){
             steps{
                script {
                          echo "${BRANCH_NAME}"
                    }
                }
             }
         
        
         stage("hello world develop"){
             steps{
                script {
                    if (env.BRANCH_NAME == 'develop') {
                        echo ${env.BRANCH_NAME}
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
