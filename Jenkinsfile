pipeline {
    agent any
    tools {
        maven "M3"
    }
    stages {
        stage('Checkout') {
            steps {
                git branch: "main", url: "https://github.com/Da-Santana/SpringPetClinic.git"
            }
        } // Closing Checkout stage
        
        stage('Build') {
            steps {
                sh "mvn compile"
            }
        } // Closing Build stage
        
        stage('Test') {
            steps {
                sh "mvn test"
            }
        } // Closing Test stage
        
        stage('Package') {
            steps {
                sh "mvn package"
            }
        } // Closing Package stage
        
        stage('Deploy') {
            steps {
                sh "java -jar /home/coder/.jenkins/workspace/Pet\\ Clinic\\ Declarative\\ Pipeline/target/*.jar"
            }
        } // Closing Deploy stage
    }
}
