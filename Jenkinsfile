pipeline {
    agent any
    
    stages {
        stage('Clone Repository') {
            steps {
                script {
                    sh 'git clone https://github.com/lolithaa999/PES1UG22CS308_Jenkins_1.git'
                }
            }
        }
        
        stage('Build') {
            steps {
                script {
                    sh 'g++ -o pes1ug22cs308-1 PES1UG22CS308_Jenkins_1/pes1ug22cs308.cpp'
                }
            }
        }
        
        stage('Test') {
            steps {
                script {
                    sh './pes1ug22cs308-1'
                }
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'deploy'
                // Add deployment steps here
            }
        }
    }
    
    post {
        failure {
            echo 'pipeline failed'
        }
    }
}
