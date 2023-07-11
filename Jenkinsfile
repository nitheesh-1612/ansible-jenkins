
pipeline {
    agent any
    stages {
        stage("copy files to ansible folder") {
            steps {
                script {
                    echo "copying all necessary files to ansible control node"
                    sshagent(['ansible-server-key']) {
                        sh "scp -o StrictHostKeyChecking=no ansible/* root@"
                    }
                }
            }
        }
    }   
}
