pipeline {
    agent any

    triggers {
        pollSCM('* * * * *') // Check every 5 minutes for changes
    }

    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/your-org/your-repo.git', branch: 'main'
            }
        }

        stage('Run Script') {
            steps {
                echo 'Running deployment script...'
            }
        }
    }
}
