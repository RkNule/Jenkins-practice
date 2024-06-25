pipeline {
    agent any
    environment{
        name = 'Rohan'
    }
    parameters {
        string(name: 'person', defaultValue: 'Rohan Nule', description: 'who are you?')
        booleanParam(name: 'isMale', defaultValue: true, description: '')
        choice(name: 'City', choices: ['Jaipur', 'Mumbai', 'Pune'], description: '')
    }
    stages {
        stage('Run a command') {
            steps {
                sh '''
                ls
                date
                pwd
                cal 2024
                '''
            }
        }
        stage('Environment Variable') {
             environment{
             username = 'Rk'
            }
            steps {
                sh 'echo "${name}"'
                sh 'echo "${person}"'
            }
        }
        stage('Parameters') {
            steps {
                echo 'deploy on test'
            }
        }
        stage('Continue ?') {
            input {
                message "Should we continue?"
                ok "Yes we should"
            }
            steps {
                echo 'deploy on prod'
                sh 'echo "${username}"'
                echo 'I love you vesdshree'
            }
        }
    }
    post{
        always {
            echo "I will always say hello again."
        }
        failure {
            echo "Failure"
        }
        success {
            echo "Success definately it's on my way"
        }
    }
}
