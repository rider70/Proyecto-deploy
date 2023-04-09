pipeline {
    agent none

        stage('Build front - DEV') {
            agent { label 'nodo1' }
            steps {
                sh 'cd /home/ebian/vue/vue-project ; docker-compose up -d'
                echo 'Build front - DEV'
            }
        }
        
		
}
