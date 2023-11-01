pipeline {
    agent any
    stages {
        stage('Delete all nodes')
        {
            steps {
                sh "minikube stop"
                sh "kubectl start"
            }
        }
        stage('Permission1')
        {
            steps {
                sh "sudo -S chmod -R 644 ~/.minikube/profiles/minikube/client.key"
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
