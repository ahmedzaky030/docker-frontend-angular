pipeline {
    agent any

    stages {
    //     stage('Checkout SCM') {
    //         steps {
    //             checkout scmGit(
    // branches: [[name: 'master']],
    // userRemoteConfigs: [[url: 'https://github.com/ahmedzaky030/docker-frontend-angular.git']])
    //         }
    //     }
    stage('Npm dependencies install'){
        steps{
            bat 'npm install'
        }
    }
        stage('Build'){
            steps {
                
                bat 'ng build -c production --base-href ./'
            }
        }
        stage('Deploy and Run'){
            steps{
               
                bat "copy C:\\Users\\azm03\\.jenkins\\workspace\\test-pipeline\\dist\\docker-frontend-angular\\browser C:\\Users\\azm03\\Downloads\\nginx-1.24.0\\nginx-1.24.0\\html"
                bat "start chrome http:\\localhost"
               
            }
        }
    }
}
