pipeline {
    agent any
    stages {
//         stage('Clone repository') {
//             steps {
//                 checkout([$class: 'GitSCM', 
//                 branches: [[name: '*/main']], 
//                 userRemoteConfigs: [[url: 'https://github.com/vardhan2404/PES1UG21CS256_Jenkins/blob/main/Jenkinsfile']]])
//             }
//         }
        stage('Build') {
            steps {
                build 'PES1UG21CS256-1'
                sh 'g++ main.cpp -o output'
            }
        }
        stage('Test') {
            steps {
                sh './output'
            }
        }
        stage('Deploy') {
            steps {
                echo 'deploy'
            }
        }
    }
    post{
        failure{
            error 'Pipeline failed'
        }
    }
}
