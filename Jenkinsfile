pipeline {
    agent any
    stages {
        stage('Deploy')
        {
            steps {
                sh "kubectl create -f k8s-specifications/"
            }
        }
    }
}