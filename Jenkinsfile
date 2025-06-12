pipeline {
    agent {
        docker {
            image 'python:3.9'
        }
    }

    stages {
        stage('Build') {
            steps {
                echo "Building..."
                sh '''
                    pip install -r myapp/requirements.txt
                '''
            }
        }

        stage('Test') {
            steps {
                echo "Testing..."
                sh '''
                    python3 myapp/hello.py
                    python3 myapp/hello.py --name=Brad
                '''
            }
        }

        stage('Deliver') {
            steps {
                echo "Delivering..."
                sh '''
                    echo "doing delivery stuff..."
                '''
            }
        }
    }
}
