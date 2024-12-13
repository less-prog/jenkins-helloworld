pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                sh '''
                unset http_proxy
                unset https_proxy
                git clone https://github.com/less-prog/jenkins-helloworld.git
                '''
            }
        }

        stage('Build') {
            steps {
                sh 'javac Main.java'
            }
        }

        stage('Run') {
            steps {
                sh 'java Main'
            }
        }
    }
}
