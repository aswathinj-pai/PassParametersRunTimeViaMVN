pipeline {
    agent any

       stages {
        stage('Stage 1:Get Code from Repository') {
            steps {
                git 'https://github.com/ajautomation/PassParametersRunTimeViaMVN.git'
                sh "/usr/local/apache-maven/apache-maven-3.9.4/bin/mvn -version"
            }
        }
        stage('Stage 2:Compile code') {
            steps {
               sh "/usr/local/apache-maven/apache-maven-3.9.4/bin/mvn compile" 
            }
        }
        stage('Stage 3:Run Unit Test') {
            steps {
                sh "/usr/local/apache-maven/apache-maven-3.9.4/bin/mvn test"
            }
        }  
        stage('Stage 4:Build ') {
            steps {
                sh "/usr/local/apache-maven/apache-maven-3.9.4/bin/mvn package"

            }
        }

            
        
    }
}
