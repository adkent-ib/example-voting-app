pipeline {
    agent any
    stages {
        stage('Clean')
        {
            steps {
                cleanWs()
            }
        }
        stage('Build')
        {
            steps {
                sh "cd k8s-specifications/ && kubectl apply -f vote-deployment.yaml"
            }
        }
    }
}