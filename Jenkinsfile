pipeline {
    agent any
environment{
     PATH = "C:\\Windows\\System32"
}
    triggers {
        pollSCM '* * * * *'
    }
    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out code from GitLab...'
                // Add your GitLab repository URL
                git branch: 'main', url: 'https://github.com/Monisha22-S/mavenwithjenkins.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Building the standalone application...'
                // Add your build commands here
            }
        }

        stage('Test') {
            steps {
                bat ''' cd  C:/Program Files/apache-maven-3.9.6-bin (1)/apache-maven-3.9.6/bin
                mvn clean test
                '''
                
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the application to localhost...'
                // Add your deployment commands here
            }
        }
    }
}

