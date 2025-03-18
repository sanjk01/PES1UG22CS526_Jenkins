pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ -o PES1UG22CS526-1 pes1ug22cs526.cpp' 
                }
            }
        }
        
        stage('Test') {
            steps {
                script {
                    sh './PES1UG22CS526-1' 
                }
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deploying application...' 
                
            }
        }
    }
    
    post {
        failure {
            echo 'Pipeline failed! Please check the logs.'
        }
        success {
            echo 'Pipeline executed successfully!'
        }
    }
}
