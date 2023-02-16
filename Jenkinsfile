pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh '/main/make -f make2.mk'
                sh '/main/make -f make1.mk'
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