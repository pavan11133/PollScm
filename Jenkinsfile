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
                sh 'ls -l Deploy.sh'
                echo 'chmod 744 Deploy.sh'
                sh 'ls -l Deploy.sh'
                sh './Deploy.sh'
            }
        }
    }
}
