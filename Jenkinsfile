pipeline {
    agent {
        label 'AGENT-1' // so je nkins will run on AGENT-1 node
    }
    stages {
        stage('Build') {
            steps {
                sh 'echo This is build stage'
            }
        }
        stage('Test') {
            steps {
                sh 'echo This is test stage'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo This is deploy stage'
            }
        }
    }
}