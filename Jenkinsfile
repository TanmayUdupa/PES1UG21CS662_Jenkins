pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    build 'PES1UG21CS662-1'
                    sh 'g++ main/hello.cpp -o output'
                }
            }
            post {
                failure {
                    echo 'pipeline failed'
                }
            }
        }
        
        stage('Test') {
            steps {
                script {
                    sh './outp'
                }
            }
            post {
                failure {
                    echo 'pipeline failed'
                }
            }
        }
        
        stage('Deploy') {
            steps {
                script {
                  echo "deploy"
                }
            }
            post {
                failure {
                    echo 'pipeline failed'
                }
            }
        }
    }
}
