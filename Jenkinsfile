def SANITIZED_BRANCH_NAME = env.BRANCH_NAME.toLowerCase().replaceAll("/", "-")

pipeline {
    agent {
      node {
             label 'docker-agent'
        }
    }
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
     }
      stages{
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
