pipeline {
    agent {
        label 'AGENT-1'
    }
    options {
        timeout(time: 1, unit: 'SECONDS')
    }
    stages {
        stage('BUILD') {
            steps {
                sh 'echo This is build stage'
            }
        }
        stage('TEST') {
            steps {
                sh 'echo This is test stage'
                sh 'sleep 10'
            }
        }
        stage('DEPLOY') {
            steps {
                sh 'echo This is deploy stage'
            }
        }
    }

}