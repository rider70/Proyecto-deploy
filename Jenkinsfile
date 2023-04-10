pipeline{
    agent { label "nodo1"}
    stages{
        stage("Build"){
            steps{
               sh '''cd /home/ebian/vue/vue3-recuperatorio
                     docker-compose up -d'''
            }
        }
    }
}
