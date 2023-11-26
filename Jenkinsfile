pipeline {
    agent any
    
    stages {
        stage("Getting source code...") {
            steps {
                echo "Pulling";
                git branch: "main",
                url: "https://github.com/JawherBalti/java-calculator.git";
            }
        }
        
        stage("Deleting files under target folder...") {
            steps {
                sh """mvn clean"""
            }
        }
        
        stage("Compiling..."){
            steps {
                sh """mvn compile"""
            }
        }
        
        stage("Creating deliverable...") {
            steps {
                sh """mvn package"""
            }
        }
    }
}
