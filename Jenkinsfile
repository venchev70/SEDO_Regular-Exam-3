pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            when {
                branch 'main'  
            }
            steps {
                checkout scm
            }
        }

        stage('Build the project') {
            when {
                branch 'main'
            }
            steps {
                bat 'dotnet build'
            }
        }
        
        stage('Run all tests') {
            when {
                branch 'main'
            }
            steps {
                bat 'dotnet test --no-build'
            }
        }
    }
}
