pipeline {
        agent any
        tools {
                maven 'maven-3.9'
        }
        stages {
                stage ('Checkout'){
                        steps {
                                echo 'Clonning the code from github...'
                                checkout scm
                        }                        
                }
                stage ('Build') {
                        steps {
                                echo 'Building the app...'
                                sh 'mvn clean compile'
                        }
                }
                stage ('Test') {
                        steps {
                                echo 'Testing the app...'
                                sh 'mvn test'
                        }
                }
                stage ('Package') {
                        steps {
                                sh 'mvn package'
                        }
                }
        }
}