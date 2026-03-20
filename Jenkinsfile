pipeline {
    agent any
    //agent {
    //    label 'AGENT-1'
    //}
    //options {
    //    timeout(time:3, unit: 'MINUTES')
    //   disableConcurrentBuilds()
    //}
    //parameters {
    //    string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
    //    text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
    //    booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
    //    choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
    //    password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    //}
    //environment {
    //    // key value pair
    //    DEPLOY_TO = 'production'
    //    GREETING = 'Good Morning'
    //}
    stages {
        stage('Build') {
            steps {
                sh 'echo This is build stage'
                sh 'env'
            }
        }
        stage('Test') {
            steps {
                sh 'echo This is test stage'
                //sh 'sleep 10'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo This is deploy stage'
            }
        }
       // stage('print params'){
       //     steps
       //     {
       //         echo "Hello ${params.PERSON}"
       //         echo "Biography: ${params.BIOGRAPHY}"
       //         echo "Toggle: ${params.TOGGLE}"
       //         echo "Choice: ${params.CHOICE}"
       //         echo "Password: ${params.PASSWORD}"
       //         echo "treggared test"
       //     }
       // }
    }
    post {
        always {
            echo 'I will always say Hello again'
        }
        success {
            echo 'I will run when pipeline is successful'
        }
        failure {
            echo 'i will run when pipeline is failure'
        }
    }
}