@Library('shared-library') _
pipeline {
    agent any
    environment {
        DOCKER_CRED = 'dockerhub'
    }
    stages {
        stage("Checkout code") {
            steps {
                script {
                   scmCheckOut()
                }
            }
        }
        stage("Build image") {
            steps {
                script {
                    step.buildNum()
                    step.buildImage('abigael081497')
                }
            }
        }
        stage("Push image") {
            steps {
                script {
                    step.pushImage()
                }
            }
          }        
        }
   }
