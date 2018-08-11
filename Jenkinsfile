#!/usr/bin/env groovy
pipeline {
    agent any

    stages {
        stage('compile stage') {
            steps {
              withmaven(maven: 'maven_install'){
                    sh'mvn compile'
            }
          }
        }
        stage('Test') {
            steps {
                withmaven(maven: 'maven_install'){
                    sh'mvn test'
            }
          }
        }
               
        stage('Deploy') {
            steps {
                withmaven(maven: 'maven_install'){
                    sh'mvn deploy'
          }
        }
      }
   }
}
