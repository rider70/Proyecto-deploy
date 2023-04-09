pipeline {
    agent {label "nodo1"}
    stages {
        stage('Build') {
            steps {
              sh "cd /home/ebian/vue/vue-project ; docker build -t 192.168.255.142:8082/vue-project:2.1 . ; docker push 192.168.255.142:8082/vue-project:2.1"
             
            }
        }
    }
}
