pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git branch: '*/master', url: 'https://github.com/less-prog/jenkins-helloworld.git'
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
