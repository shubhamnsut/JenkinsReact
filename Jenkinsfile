pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/shubhamnsut/JenkinsReact.git'
            }
        }

        stage('Build') {
            steps {
                sh 'npm install'
                sh 'npm run build'
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
