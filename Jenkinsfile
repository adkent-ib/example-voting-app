pipeline {
    agent any
    stages {
        stage('Permission1')
        {
            steps {
                sh "chmod -R 644 ~/.minikube/profiles/minikube/client.key"
            }
        }
        stage('Deploy')
        {
            steps {
                sh "kubectl create -f k8s-specifications/"
            }
        }
    }
}
