pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'make -C main'
                echo 'Build Stage Successful'
            }
        }
        stage('Test') {
            steps {
                sh '/var/jenkins_home/workspace/PES1UG20CS199-1/main/hello_exec'
                echo 'Test Stage Successful'
            }
        }
        stage('Deploy') {
            echo 'Deployed Sucessfully'
        }
        post {
            failure {
                echo 'Pipeline failed'
            }
        }
    }
}