pipeline {
    agent any
    stages {
        stage('Permission1')
        {
            steps {
                sh "sudo cp ~/.minikube/profiles/minikube/client.key /var/lib/jenkins/.minikube/profiles/minikube"
                sh "sudo -S chmod -R 644 ~/.minikube/profiles/minikube/client.key"
                sh "sudo -S chmod -R 644 /var/lib/jenkins/.minikube/profiles/minikube/client.key"
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
