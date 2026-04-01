pipeline {
    agent any
    
    triggers {
        githubPush()
    }
    
    stages {
        stage('Hello') {
            steps {
                echo 'Hello from Jenkins!'
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'echo test passed'
            }
        }
    }
    post {
        success {
            echo 'Pipeline succeeded!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
