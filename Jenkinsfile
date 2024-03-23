pipeline {
    agent any
    triggers {
        pollSCM '* * * * *'
    }
    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out code from GitLab...'
                git branch: 'main', url: 'https://github.com/Monisha22-S/mavenwithjenkins.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Building the standalone application...'
                // Make sure Maven runs from the directory where the pom.xml file exists
                dir('C:/Users/Public/Seleniumjenkins') {
                    bat '"C:/Program Files/apache-maven-3.9.6-bin (1)/apache-maven-3.9.6/bin/mvn" clean install' // Corrected Maven path
                }
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                // Make sure Maven runs from the directory where the pom.xml file exists
                dir('C:/Users/Public/Seleniumjenkins') {
                    bat '"C:/Program Files/apache-maven-3.9.6-bin (1)/apache-maven-3.9.6/bin/mvn" test' // Corrected Maven path
                }
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
