pipeline {
  agent any
  stages {
    // stage('Clone repository'){ 
    //   steps {
    //     checkout([$class: 'GitSCM',
    //     branches: [[name: '*/main']],
    //     userRemoteConfigs: [[url: 'https://github.com/Jatinsharma159/Jenkins.git']]])
    //   }
    // }
    stage('Build'){
      steps{
        build 'PES1UG21CS022-1'
        sh 'g++ main.cpp -o output'
      }
    }

    stage('Test'){
      steps{
        sh ./output
      }
    }

    stage('Deploy'){
      steps {
        echo 'Deploy'
      }
    }
  }
  post {
    failure {
      error 'Pipeline Failed'
    }
  }
}