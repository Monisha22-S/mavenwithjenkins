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
                // Run Maven from the directory where the pom.xml file exists
                bat '"C:/Program Files/apache-maven-3.9.6-bin (1)/apache-maven-3.9.6/bin/mvn" -f "C:/Users/Public/Seleniumjenkins/pom.xml" clean install'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                // Run Maven from the directory where the pom.xml file exists
                bat '"C:/Program Files/apache-maven-3.9.6-bin (1)/apache-maven-3.9.6/bin/mvn" -f "C:/Users/Public/Seleniumjenkins/pom.xml" test'
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
