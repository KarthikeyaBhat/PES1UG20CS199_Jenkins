pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'make -C main'
                sh 'cd main'
                sh 'make -f make1.mk'
                echo 'Build Stage Successful'
            }
        }
        stage('Test') {
            steps {
                sh '/var/jenkins_home/workspace/PES1UG20CS199-1/main/hello_exec'
                sh '/var/jenkins_home/workspace/PES1UG20CS199-1/main/second_exec'
                echo 'Test Stage Successful'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deployed Sucessfully'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}