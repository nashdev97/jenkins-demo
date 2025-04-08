pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the application...'
                bat 'docker build -t myapp .'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                // You can add your test scripts here
                bat 'echo "Tests passed!"'
            }
        }

        stage('Deploy'){
    steps {
        bat '''
            echo Deploying the application...
            docker stop myapp || echo "Container not running"
            docker rm myapp || echo "Container not found"
            docker run -d --name myapp -p 5000:5000 myapp
        '''
    }
    }
        stage('Cleanup') {
    steps {
        echo 'Cleaning up...'
        bat '''
            docker stop myapp || echo "Container not running"
            docker rm myapp || echo "Container not found"
            docker rmi myapp --force || echo "Image not removed"
        '''
    }
        }
    }
}
