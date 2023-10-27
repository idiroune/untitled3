pipeline {
    agent any
    tools {
        maven 'MavenJenkins2'
    }
    stages {
        stage('Clone Git repository'){
            steps{
                echo 'Cloning project...'
                git url: 'https://github.com/idiroune/untitled3.git'
            }
        }
        stage('Build') {
            steps {
                echo 'Building project...'
                sh 'mvn clean package'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing project...'
                sh 'mvn test'
            }
        }
    }
}
