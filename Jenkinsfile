#!/usr/bin/env groovy
pipeline {
   agent {
        docker {
            image 'node:6-alpine' 
            args '-p 3000:3000' 
        }
    }
    stages {
        stage('Server Tests'){
            steps {
							  sh 'echo running server tests ...'
            }
        }
        stage('Build React code ') {
            steps {
				sh 'echo building React code ...'
            }
        }
        stage('Build Docker Image'){
            steps {
								sh 'cd ..'
								sh 'docker build -t Docker-cicd:0.0.1'
            }
        }
    }

}


