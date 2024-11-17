pipeline {
    agent any
    environment {
        server_ip = '34.239.143.81'
        server_user = 'ubuntu'
    }
    stages {
        stage('Copy WorkSpace') {
            steps {
                withCredentials([sshUserPrivateKey(credentialsId: 'ssh_credentials', keyFileVariable: 'SSH_KEY')]) {
                sh'scp -i ${SSH_KEY} -r . $server_user@$server_ip:.'
            }
            }
        }
    }
}
