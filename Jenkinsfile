pipeline {
    agent any
    ansiColor('xterm')
    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
                pwd()
                sh 'uname -a'
            }
        }
        stage('Check nginx'){
            sh 'systemctl status nginx'
        }
    }
    post { 
        always { 
            echo 'I will always say Hello again!'
            cleanWS()
        }
    }
}