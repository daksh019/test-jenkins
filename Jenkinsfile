pipeline {
 agent any
 stages {
        stage('Lint') {
            steps {
                sh 'npm run ng lint'
            }
        }
        stage('Test') {
            steps {
                sh 'npm run ng test'
            }
        }
    }
    post {
        always {
            cleanWs()
        }
        failure {
            echo 'All steps fail!'
        }
        success {
            echo 'All steps pass!'
        }
    }
}
