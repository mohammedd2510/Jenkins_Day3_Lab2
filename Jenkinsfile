pipeline {
    agent any
    environment {
        ssh_key = credentials('ssh_credentials')
        server_ip = '34.239.143.81'
        server_user = 'ubuntu'
    }
    stages {
        stage('Copy WorkSpace') {
            steps {
                sh'scp -i $ssh_key -r * $server_user@$server_ip:.'
            }
        }
    }
}
