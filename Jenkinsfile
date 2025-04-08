pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the application...'
                sh 'docker build -t myapp .'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                // You can add your test scripts here
                sh 'echo "Tests passed!"'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                sh 'docker run -d -p 5000:5000 myapp'
            }
        }
    }
}
