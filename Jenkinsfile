pipeline {
    agent any

    triggers {
        pollSCM('* * * * *') // Check minutes for changes
    }

    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/pavan11133/PollScm.git', branch: 'main'
            }
        }

        stage('Run Script') {
            steps {
                echo 'Running deployment script...'
                sh './Deploy.sh'
            }
        }
    }
}
