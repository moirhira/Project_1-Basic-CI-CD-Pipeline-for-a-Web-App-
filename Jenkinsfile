pipeline {
        agent any
        tools {
                manve 'maven-3.9'
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
                stages ('Test') {
                        steps {
                                echo 'Testing the app...'
                                sh 'mvn test'
                        }
                }
                stages ('Packahe') {
                        steps {
                                sh 'mvn package'
                        }
                }
        }
}