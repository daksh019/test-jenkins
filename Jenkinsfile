pipeline {
 agent any
 stages {
        stage('Lint') {
            steps {
                sh 'ng lint'
            }
        }
        stage('Test') {
            steps {
                sh 'ng test'
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
