pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo "hello world"
            }
        }
        stage('code') {
            steps {
                git changelog: false, poll: false, url: 'https://github.com/Ajayaws773/mavenrepo.git'
            }
        }
        stage('build') {
            steps {
                sh 'mvn package'
            }
        }
    }
}
