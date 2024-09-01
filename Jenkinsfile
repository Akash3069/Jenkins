pipeline {
    agent any

    stages {
        stage('fetch'){
            steps{
                git branch: 'main', url: 'https://github.com/Akash3069/Jenkins.git'
            }
        }
        stage('check'){
            steps{
                sh 'ls'
            }
        }
        stage('conatiner'){
            steps{
                sh 'docker run --name mysql-container4 -e MYSQL_ROOT_PASSWORD=root_password -e MYSQL_DATABASE=lof -d mysql:5.7'
                sh 'docker build -t myphp .'
                sh 'docker run --name my_php -d -p 80:80 myphp '
                
            }
        }
    }
} 