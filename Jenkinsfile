pipeline {
    agent{
        label 'Agent'
    }

   

    stages {
        stage('Checkout') {
            steps {
                echo 'Checkout!'
            }
        }

      
    }

    post {
        success {
            echo 'Build and tests passed!'
        }
        failure {
            echo 'Build failed.'
        }
    }
}
