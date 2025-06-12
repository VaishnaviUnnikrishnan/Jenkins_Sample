pipeline {
    agent any


    triggers {
        pollSCM('* * * * *') // Polls the repo every minute
    }

    stages {
        stage('Build') {
            steps {
                echo "Building..."
                sh '''
                    cd myapp
                    pip install -r requirements.txt
                '''
            }
        }

        stage('Test') {
            steps {
                echo "Testing..."
                sh '''
                    cd myapp
                    python3 hello.py
                    python3 hello.py --name=Brad
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
