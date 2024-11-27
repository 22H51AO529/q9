
pipeline {
    agent any 

    stages {
        stage('Build') {
            steps {
                script {
                    bat 'docker build -t my-nodejs-app .'
                    docker 
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    // Run tests here if you have any
                    echo 'Running tests...'
                }
            }
        }
        stage('Deploy') {
            steps {
                script {
                   bat ''' 
                    docker run -d -p 3001:3001 my-nodejs-app . '''
                    echo 'Deploying application...'
                }
            }
        }
    }
}
