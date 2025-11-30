pipeline {
    agent any
    stages {
        stage('Hello') {
            steps {
                echo 'Hello World !'
            }
        }
        stage('Clone Git Repository') {
            steps {
                git 'https://github.com/Leilaabendhief/ProjetStudentsManagement-DevOps.git'
            }
        }
        stage('Build Maven') {
            steps {
                sh 'chmod +x mvnw'
                sh './mvnw clean package -DskipTests'
            }
        }
    }
}
