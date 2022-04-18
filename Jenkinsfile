pipeline {
    agent any

    stages {
        stage('stage-1') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'jen', url: 'https://github.com/testgithub-trial/jenkins_test.git']]])
            }
        }
        stage('stage-2') {
            steps {
                bat 'python maha.py'
            }
        }
    }
}
