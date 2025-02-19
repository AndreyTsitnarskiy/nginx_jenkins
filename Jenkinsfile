pipeline {
    agent any
    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
                pwd()
                sh 'uname -a'
            }
        }
        stage('Check nginx'){
            steps {
            sh 'systemctl status nginx'
            }
        }
    }
    post { 
        always { 
            echo 'I will always say Hello again!'
            cleanWs()
        }
    }
}