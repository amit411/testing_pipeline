pipeline {

    agent any

    stages {

        stage('Checkout') {
        
            steps {
                 git 'https://github.com/amit411/testing_pipeline.git'
            }
           }

        stage('build and deploy') {

            steps {
                sh 'docker build -t latest-image-cicd .'
                sh 'docker run -d -it -p 80:80 latest-image-cicd'
           }
          }
         }
