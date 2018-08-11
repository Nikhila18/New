#!/usr/bin/env groovy
pipeline {
    agent any

    stages {
        stage('compile stage') {
            steps {
              withmaven(maven: 'maven_3.5.3'){
                    sh'mvn compile'
            }
          }
        }
        stage('Test') {
            steps {
                withmaven(maven: 'maven_3.5.3'){
                    sh'mvn test'
            }
          }
        }
               
        stage('Deploy') {
            steps {
                withmaven(maven: 'maven_3.5.3'){
                    sh'mvn deploy'
          }
        }
      }
   }
}
