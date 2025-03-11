pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'make -C main'
                echo 'Building completed'
            }
        }
        
        stage('Test') {
            steps {
                sh 'cd main && ./hello_exec'
                echo 'Testing completed'
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deployment completed'
            }
        }
    }
    
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}