#!/usr/bin/env groovy

pipeline {

    agent {
        docker {
            image 'ubuntu'
            args '-u root'
        }
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                sh 'mkdir mandeeptest1'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
                sh 'echo 12 > index.php'
            }
        }
    }
    post {
      always {
          script {
              if (currentBuild.result == null) {
                  currentBuild.result = 'SUCCESS'    
              }
          }    
          step([$class: 'Mailer',
            notifyEveryUnstableBuild: true,
            recipients: "mandeep.singh@scalemonks.com",
            sendToIndividuals: true])
      }
  }
}
}
