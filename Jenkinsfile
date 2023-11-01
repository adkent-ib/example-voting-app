pipeline {
    agent any
    stages {
        stage('Deploy')
        {
            steps {
                sh "kubectl create -f k8s-specifications/"
            }
        }
        stage('Permission1')
        {
            steps {
                sh "chmod -R 644 ~/.minikube/profiles/minikube/client.key"
            }
        }
    }
}
