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
                                // sh 'cd server && npm test'
								// sh 'echo running react component tests ...'
								// sh 'cd .. && cd client && npm test'
								// sh 'running linting ...'
								// sh 'npm run lint'
            }
        }
        stage('Build React code ') {
            steps {
				sh 'building React code ...'
                // sh 'npm run build'
            }
        }
        stage('Build Docker Image'){
            steps {
								sh 'cd ..'
								sh 'docker build -t DockerCiCd:0.0.1'
            }
        }
    }

}


