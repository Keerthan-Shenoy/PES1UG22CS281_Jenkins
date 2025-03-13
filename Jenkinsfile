pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ -o PES1UG22CS281-1 main.cpp'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './PES1UG22CS281-1'
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploy stage'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
