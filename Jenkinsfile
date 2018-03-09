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
                bash '''#!/bin/bash 
		  	mv index.php /var/www
		'''
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
                bash '''#!/bin/bash
			echo "12 > index.php"
		'''
            }
        }
    }
}
