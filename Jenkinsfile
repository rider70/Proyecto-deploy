pipeline{
    agent { label "nodo1"}
    stages{
        stage("Deploy FrontEnd"){
            steps{
               sh '''cd /home/ebian/vue/vue3-recuperatorio
                     docker-compose up -d'''
            }
        }
        stage("Deploy BackEnd"){
            steps{
               sh '''cd /home/ebian/ferroapp/mod5-proy-django/ferroapp
                     docker-compose up -d'''
            }
        }
    }
}
