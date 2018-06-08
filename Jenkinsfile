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
                withDockerRegistry([ credentialsId: "", url: "docker.majustfortesting.com" ]) {
                sh 'docker push ma/faas:latest'
                }
            }
         }
     }
}
