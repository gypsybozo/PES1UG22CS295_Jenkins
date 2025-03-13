pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                sh 'g++ -o hello_exec hello.cpp'  // Compiling C++ file
            }
        }
        
        stage('Test') {
            steps {
                echo 'Testing...'
                sh './hello_exec'  // Running the compiled file
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deploying...'
                sh 'echo "Deployment successful!"'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline Failed'
        }
    }
}
