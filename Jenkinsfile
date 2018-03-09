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
                sh 'echo 12 > mandeeptest/index.php'
            }
        }
    }
}
