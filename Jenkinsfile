pipeline {
    agent any
    stages {
        stage('Deploy')
        {
            steps {
                sh "minikube stop && minikube delete"
                sh "minikube start"
                sh "kubectl create -f k8s-specifications/"
            }
        }
    }
}