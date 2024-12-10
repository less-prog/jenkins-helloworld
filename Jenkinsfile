pipeline {
    agent any
    stages {
        stage('Pull') {
            steps {
                checkout([$class: 'GitSCM',
                branches: [[name: '*/master']],
                doGenerateSubmoduleConfigurations: false,
                extensions: [],
                submoduleCfg: [],
                userRemoteConfigs: [[
                    url: 'git@github.com:less-prog/jenkins-helloworld.git',
                    credentialsId: 'github-less'
                ]]])
                sh "ls"
            }
        }
        stage('Build') {
            steps {
                sh "javac Main.java"
            }
        }
        stage('Run') {
            steps {
                sh "java Main"
            }
        }
    }
}

