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
                // bat 'cd "C:/Users/HP/eclipse-workspace/Assesment5"'
                bat 'mvn clean test'
            }
        }

        // stage('Test') {
        //     steps {
        //         echo 'Running tests...'
        //     }
        // }

        // stage('Deploy') {
        //     steps {
        //         echo 'Deploying the application to localhost...'
        //         // Add your deployment commands here
        //     }
        // }
    }
}
