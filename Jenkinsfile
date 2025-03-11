pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                
                sh 'g++ hello.cpp -o hello' // Compile C++ file
                
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './hello'  // Run the compiled executable
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
            echo 'Pipeline failed'
        }
    }
}
