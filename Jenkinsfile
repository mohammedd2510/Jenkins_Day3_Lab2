pipeline {
    agent any
    environment {
        ssh_key = credentials('ssh_credentials')
        server_ip = '18.206.186.114'
        server_user = 'ubuntu'
    }
    stages {
        stage('Copy WorkSpace') {
            steps {
                scp -i $ssh_key -r * $server_user@$server_ip:.
            }
        }
    }
}
