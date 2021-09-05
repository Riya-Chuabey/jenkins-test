pipeline {
    agent any
    
    environment {
        NAME = 'riya'
        LASTNAME = 'chaubey'
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh 'echo "My first pipeline"'
                sh '''
                    echo "By the way, I can do more stuff in here"
                    ls -lah
                '''
                sh 'echo $NAME $LASTNAME'
            }
        }
        
        stage('Test') {
            steps {
                echo 'Testing..'
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
        unstable {
            echo 'I will only get executed if this is unstable'
        }
    }
}
