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
		  	mkdir mandeeptest
		'''
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
                bash '''#!/bin/bash
			touch mandeeptest/index.php
			echo "12 > mandeeptest/index.php"
		'''
            }
        }
    }
}
