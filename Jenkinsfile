pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    echo "Building the C++ project..."
                    sh 'g++ -o PES1UG22AM125-1 pipe.cpp'  
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    echo "Running the C++ program..."
                    sh '.././PES1UG22AM125-1'  
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    echo "Deploying application..."
                    sh 'echo Deployment successful!'
                }
            }
        }
    }

    post {
        failure {
            echo "Pipeline failed"
        }
    }
}
