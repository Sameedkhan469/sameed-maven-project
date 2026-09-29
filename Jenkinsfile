pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                sh 'mvn clean compile'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }

        stage('Package') {
            steps {
                sh 'mvn package -DskipTests'
            }
        }
    }

    post {
        success {
            echo 'Maven CI/CD pipeline completed successfully!'
        }

        failure {
            echo 'Maven CI/CD pipeline failed!'
        }
    }
}
