pipeline {
    agent any
    stages {
        stage('Permission1')
        {
            steps {
                sh "sudo chmod -R 644 /home/adkent/.minikube/profiles/minikube/client.key"
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
