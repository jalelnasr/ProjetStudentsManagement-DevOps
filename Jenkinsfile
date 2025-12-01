pipeline {
    agent any

    tools {
        maven 'M2_HOME'
    }

    stages {

        stage('Exemple 1 - Hello World') {
            steps {
                echo "Hello world !"
            }
        }

        stage('Git Clone') {
            steps {
                git branch: 'master', url: 'https://github.com/jalelnasr/ProjetStudentsManagement-DevOps.git'
            }
        }

        stage('Maven Build') {
            steps {
                sh 'mvn -version'
            }
        }
        stage('Clean') {
                    steps {
                        sh 'mvn clean'
                    }
                }
                stage('Compile') {
                            steps {
                                sh 'mvn compile'
                            }
                        }
                        stage('Sonar Analysis') {
                            environment {
                                SONAR_TOKEN = credentials('sonar-token')
                            }
                            steps {
                                sh 'mvn sonar:sonar'
                            }
                        }

    }
}
