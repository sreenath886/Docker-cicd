
podTemplate(label: 'aurora', containers: [
    containerTemplate(name: 'docker', image: 'docker', ttyEnabled: true, command: 'cat'),
    containerTemplate(name: 'kubectl', image: 'lachlanevenson/k8s-kubectl:v1.7.3', command: 'cat', ttyEnabled: true)
  ],
  volumes: [
    hostPathVolume(mountPath: '/var/run/docker.sock', hostPath: '/var/run/docker.sock'),
  ]) {

    node('aurora') {

        checkout scm

        stage('build and push the bot image') {
            container('docker') {

                 {
                    
                 sh 'docker -v'
                }
            }
        }

        stage('update kubernetes') {
           steps {
							echo 'running linting ...'
							// sh 'npm run lint'
                            echo 'placeholder for UT'
							// sh 'npm test'
            }
        }
    }
}


