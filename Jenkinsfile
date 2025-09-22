pipeline {
    agent{
        label 'Agent'
    }

   

    stages {
        stage('Checkout') {
            steps {
                // Pull code from GitHub
                git branch: 'main', url: 'https://github.com/peterduong/CucumberBasicsWithJekinsAgent.git'
            }
        }

        stage('Build & Verify') {
            steps {
                // Run Maven verify
                sh 'mvn verify'
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
