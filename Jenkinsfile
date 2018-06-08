pipeline {
    agent { dockerfile true }
    stages {
        stage('Test') {
            steps {
                sh 'go --version'
            }
        }
        stage('Push') {
            steps {
              docker.withRegistry('https://docker.majustfortesting.com') {

              def customImage = docker.build("my-image:${env.BUILD_ID}")

              /* Push the container to the custom Registry */
              customImage.push()
              }
           }
        }    
    }
}
