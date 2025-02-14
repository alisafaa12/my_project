pipeline {
    agent {
        label 'DevWin'  // Ensure this runs on a Windows node
    }

    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/alisafaa12/my_project.git'
            }
        }

        stage('Build') {
            steps {
                bat '''
                echo "== Starting Build =="
                dir  // Lists files in the workspace
                npm install  // Install dependencies
                echo "== Build Completed! =="
                '''
            }
        }

        stage('Test') {
            steps {
                bat '''
                echo "== Running Tests =="
                npm test  // Replace with Maven if needed: mvn test
                echo "== Tests Completed! =="
                '''
            }
        }

        stage('Deploy') {
            steps {
                bat '''
                echo "== Deploying Application =="
                xcopy /E /I /Y build\\* "C:\\Deployments\\MyApp"
                echo "== Deployment Complete! =="
                '''
            }
        }
    }
}
