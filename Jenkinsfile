pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                bat 'git clone https://github.com/alisafaa12/my_project.git'
            }
        }

        stage('Build') {
            steps {
                bat '''
                echo "Building the application"
                npm install
                '''
                // If using Java, replace npm with Maven:
                // bat 'mvn clean install'
            }
        }

        stage('Test') {
            steps {
                bat '''
                echo "Running tests"
                npm test
                '''
                // For Java:
                // bat 'mvn test'
            }
        }

        stage('Deploy') {
            steps {
                bat '''
                echo "Deploying application..."
                echo "Deploy process simulated"
                '''
                // If deploying to a remote server, you can use SCP:
                // bat 'scp -r build/* user@server:/deployments/'
            }
        }
    }
}
