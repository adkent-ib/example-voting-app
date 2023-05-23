pipeline {
    agent any
    post { 
        always 
        { 
            cleanWs()
        }
    }
    stages {
        stage('Build')
        {
            steps {
                sh "cd k8s-specifications/ && kubectl apply -f vote-deployment.yaml"
            }
        }
    }
}