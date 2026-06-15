pipeline {
    agent {
        label 'AGENT-1'
    }
    triggers {
        githubPush()
    }
    options {
        timeout(time: 30, unit: 'MINUTES')
        disableConcurrentBuilds()
    }
    // Define parameters for the pipeline
    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
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
        // This stage is added to print the parameters passed to the pipeline
        stage('print params') {
            steps {
                echo "Hello ${params.PERSON}"
                echo "Biography: ${params.BIOGRAPHY}"
                echo "Toggle: ${params.TOGGLE}"
                echo "Choice: ${params.CHOICE}"
                echo "Password: ${params.PASSWORD}"
                echo "triggered-test"
            }
        }
    }
}