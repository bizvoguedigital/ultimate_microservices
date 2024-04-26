pipeline {
    agent any

    stages {
        stage('Deploy To Kubernetes') {
            steps {
                    sh "kubectl apply -f deployment-service.yml"
                    sleep 60
                    
                }
            }
        }
        
        stage('verify Deployment') {
            steps {
                    sh "kubectl get svc -n webapps"
                }
            }
        }
    }
}
