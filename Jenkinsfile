#!/usr/bin/env groovy
pipeline {
    agent any
    tools { 
        maven 'Maven 3.5.3' 
        jdk 'jdk8' 
    }
    stages {
        stage ('Initialize') {
            steps {
                sh '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                ''' 
            }
        }

    stages ('Build stages'){
        stage ('compile stage') {
            steps {
             
                    sh 'mvn compile'
            }
          }
        
        stage ('Test') {
            steps {
                    
                    sh 'mvn test'
            }
          }
        
               
        stage('Deploy') {
            steps {
                    
                    sh 'mvn deploy'
          }
        }
      }
   }
}
