pipeline {
    agent none
    stages {
        stage('Back-end') {
            agent {
                docker { image 'maven:3.9.7-eclipse-temurin-21-alpine' }
            }
            steps {
                sh 'mvn --version'
            }
        }
        stage('Front-end') {
            agent {
                docker { image 'node:20.14.0-alpine3.20' }
            }
            steps {
                sh 'node --version'
                sh 'docker'
                sh 'docker compose'
            }
        }
    }
}
