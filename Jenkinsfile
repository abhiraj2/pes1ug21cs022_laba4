pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh 'make -C main'
                sh 'g++ main.cpp -o output' 
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                sh './output'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deployed'
            }
        }
    }
}