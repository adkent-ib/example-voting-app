pipeline {
    agent any
    stages {
        stage('Build')
        {
            steps {
                sh "k create -f k8s-specifications/"
            }
        }
    }
}