pipeline {
    agent any
    stages {
        stage('Build')
        {
            steps {
                sh "kubectl create -f k8s-specifications/"
            }
        }
    }
}