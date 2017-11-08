
pipeline {
    def app
   agent {
        docker {
            image 'node:6-alpine' 
            args '-p 3000:3000' 
        }
    }
    stages {
        stage('Unit Tests'){
            steps {
							echo 'running linting ...'
							// sh 'npm run lint'
                            echo 'placeholder for UT'
							// sh 'npm test'
            }
        }
        stage('Build image') {
        /* This builds the actual image; synonymous to
         * docker build on the command line */

        app = docker.build("getintodevops/hellonodssse")
    }
        
    }     

}
