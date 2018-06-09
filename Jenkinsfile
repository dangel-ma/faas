pipeline {
    agent { dockerfile true }
     stages {
         stage('Test') {
             steps {
                sh 'ls'
             }
         }
         stage('Publish') {
            steps {
                docker.withRegistry("https://your.ecr.domain.amazonws.com") {
                    docker.image("faas").push()
                }
            }
         }
     }
}
