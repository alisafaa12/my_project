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
                echo == Starting Build ==
                dir  // Lists files in the workspace
                '''
                // If using Java, replace npm with Maven:
                // bat 'mvn clean install'
                echo == Build Completed! ==
            }
        }

        stage('Test') {
            steps {
                bat '''
                echo == Running Tests ==
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
                xcopy /E /I /Y build\* "C:\\Deployments\\MyApp"
                echo == Deployment Complete! ==
                '''
                // If deploying to a remote server, you can use SCP:
                // bat 'scp -r build/* user@server:/deployments/'
            }
        }
    }
}
