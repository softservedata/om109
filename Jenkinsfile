pipeline {
    agent any
    stages {
        stage('Hello') {
            steps {
                bat 'echo START'
            }
        }
        stage('Clone') {
            steps {
                git url: 'https://github.com/softservedata/om109.git', branch: 'main'
            }
        }
        stage('Build') {
            steps {
                bat 'mvn -B package -DskipTests'
            }
        }
        stage('Unit Test') {
            steps {
                bat 'mvn -B clean test'
            }
        }
    }
}
