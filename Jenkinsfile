pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                make -C main
                sh 'g++ main.cpp -o output' 
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}