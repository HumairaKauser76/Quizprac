pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build') {
            steps {
                bat 'mvn -B -DskipTests clean package'
            }
        }
        stage('Run') {
            steps {
                bat 'java -jar target\\quizprac-1.0-SNAPSHOT-jar-with-dependencies.jar'
            }
        }
    }
}
