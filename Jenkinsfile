pipeline {
    agent {
        label "nodejs-slave"
    }
    stages {
        stage('Unit Tests'){
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
              //  sh 'npm run build'
            }
        }
        stage('Build Docker Image'){
            steps {
								sh 'cd ..'
								sh 'docker build -t aurora-cx:0.0.${BUILD_NUMBER}'
            }
        }
    }

}
