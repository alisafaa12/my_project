pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/your-username/your-repository.git'
            }
        }
        stage('Build') {
            steps {
                sh 'echo "Building the application"'
                sh 'mvn clean install'  // Change based on your build tool
            }
        }
        stage('Test') {
            steps {
                sh 'echo "Running tests"'
                sh 'mvn test'  // Change based on your test framework
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo "Deploying Application"'
                sh 'scp -r target/*.jar user@server:/deployments/'  // Adjust for your server
            }
        }
    }
}
