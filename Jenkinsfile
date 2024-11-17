pipeline {
    agent any
    environment {
        SSH_KEY = credentials('ssh_credentials') 
        server_ip = '34.239.143.81'
        server_user = 'ubuntu'
    }
    stages {
        stage('Copy WorkSpace') {
            steps {
                sh'scp -i ${SSH_KEY} -r . $server_user@$server_ip:.'
            }
        }
    }
}
