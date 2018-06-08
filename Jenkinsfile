pipeline {
    agent { dockerfile true }
     stages {
         stage('Test') {
             steps {
                sh 'ls'
             }
         }
         stage('Publish') {
            when {
              branch 'master'
            }
            steps {
                withDockerRegistry([ url: "docker.majustfortesting.com" ]) {
                sh 'docker push ma/faas:latest'
                }
            }
         }
     }
}
