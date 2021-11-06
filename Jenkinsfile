pipeline {
    agent any
    
    environment {
        NOME = 'Paloma'
        SOBRENOME = 'Paradela'
    }
    
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                echo "$NOME"
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                sh 'echo $SOBRENOME'
                sh 'pwd'
                sh 'ls -la'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
    
    post {
            always {
                echo 'I will always get executed :D'
            }
            success {
                echo 'I will only get executed if this success'
            }
            failure {
                echo 'I will only get executed if this fails'
            }
        }
}
