pipeline{
    agent { label "nodo1"}
    stages{
        stage("Build"){
            steps{
               sh "cd /home/ebian/vue/vue-project ; docker-compose up -d"
            }
        }
    }
}
