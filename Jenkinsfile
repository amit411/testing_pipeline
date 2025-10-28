pipeline {

    agent any

    stages {

        stage('checkout') {

            stpes {
                checkout scm
               }
              }

        stage('build and deploy') {

            steps {
                sh 'docker build -t latest-image-cicd .'
                sh 'docker run -d -it -p 80:80 latest-image-cicd'
           }
          }
         }
        }
