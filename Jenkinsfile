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
                git branch: 'master', url: 'https://gitlab.com/monisha2003/simpleapp6.git'
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
                bat ''' 
                maven clean test
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

