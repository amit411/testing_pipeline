pipeline {

    agent any

    stages {
       # stage('Checkout') {
        #    steps {
         #     git 'https://github.com/amit411/testing_pipeline.git'
          #        }
           #      }

        stage('build and deploy') {

            steps {
                sh '''docker ps -q --filter "name=myCON" | docker stop myCON && docker rm myCON || true'''
                sh 'docker build -t latest-image-cicd .'
                sh 'docker run -d -it -p 80:80 --name myCON latest-image-cicd'
           }
          }
         }
        }
