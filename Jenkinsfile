#!/usr/bin/env groovy

pipeline {   
    agent {
        node {
            label 'arm-microhal-eabi-gcc'
        }    
    }   

    stages {
        stage('Checkout') {
            steps {
               	checkout scm
                sh 'git submodule update --init'               
            }
        }
    } 

    post {
        always {
            deleteDir()
        }
    }
}
