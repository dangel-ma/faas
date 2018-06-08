pipeline {
    agent { dockerfile true }
    docker {
      image "markdown"
      registryUrl "https://docker.majustfortesting.com"
    }
    stages {
        stage('Test') {
            steps {
                sh 'go --version'
            }
        }
    }
}
