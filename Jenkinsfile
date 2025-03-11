pipeline {
    agent any  // Runs on any available agent
    
    stages {
        stage('Build') {
            steps {
                sh 'g++ non_existing_file.cpp -o hello' // This will cause an error
            }
        }

        stage('Test') {
            steps {
                sh './hello'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline Failed!'
        }
    }
}
