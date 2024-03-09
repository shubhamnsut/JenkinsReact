pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/shubhamnsut/JenkinsReact'
            }
        }

        stage('Build') {
            steps {
                bat 'npm install'
                bat 'npm run build'
            }
        }
    }

    post {
        success {
            echo 'Pipeline succeeded! Your React project is ready for deployment.'
        }
        failure {
            echo 'Pipeline failed! Please check the build logs for more information.'
        }
    }
}
