pipeline {
    agent any
    stages {
        stage('Permission1')
        {
            steps {
                sh "sudo -S chmod -R 644 ~/.minikube/profiles/minikube/client.key"
            }
        }
        stage('Permission2')
        {
            steps {
                sh "sudo ln -s ~/.minikube/profiles/minikube/client.key /var/lib/jenkins/.minikube/profiles/minikube/"
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
