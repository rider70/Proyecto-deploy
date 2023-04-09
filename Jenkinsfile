pipeline {
    agent none

    stages{   
        stage('Clone Backend - DEV ') {
            agent { label 'nodo1' }
            steps {
                git branch: 'main', url: 'https://github.com/rider70/proy-python.git'
                echo 'Cloned Backend..'
            }
        }
        stage('Build Backend - DEV') {
            agent { label 'nodo1' }
            steps {
                sh 'docker-compose up -d'
                echo 'Build backend - DEV'
            }
        }
        stage('Clone Frontend - DEV') {
            agent { label 'nodo1' }
            steps {
                git branch: 'main', url: 'https://github.com/rider70/vue3-recuperatorio.git'
                echo 'Cloned Frontend - DEV'
            }
        }
        stage('Build Frontend - DEV') {
            agent {label 'nodo1'}
            steps {
                sh 'docker-compose up -d dev'
                echo 'Build frontend - DEV'
            }
        }
		
		
		 stage('Clone Frontend - QA') {
            agent { label 'nodo1' }
            steps {
                git branch: 'main', url: 'https://github.com/rider70/vue3-recuperatorio.git'
                echo 'Cloned Frontend - QA'
            }
        }
        stage("Run Test - QA"){
            agent { label 'nodo1' }
            steps {
                sh 'docker-compose up -d test'
                echo 'Build tests ..'
            }
        }
		
		
        stage('Clone Backend - PROD') {
            agent { label 'nodo1' }
            steps {
                git branch: 'main', url: 'https://github.com/rider70/proy-python.git'
                echo 'Cloned Backend - PROD'
            }
        }
        stage('Build Backend - PROD') {
            agent { label 'nodo1' }
            steps {
                sh 'docker-compose up -d'
                echo 'Build backend - PROD'
            }
        }
        stage('Clone Frontend - PROD') {
            agent { label 'nodo1' }
            steps {
                git branch: 'main', url: 'https://github.com/rider70/vue3-recuperatorio.git'
                echo 'Cloned Frontend - PROD'
            }
        }
        stage('Build FrontEnd - PROD') {
            agent {label 'nodo1'}
            steps {
                sh 'docker-compose up -d vue-app'
                echo 'Build FrontEnd - PROD'
            }
        }
 
    }
}
