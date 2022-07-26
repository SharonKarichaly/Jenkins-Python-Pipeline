pipeline {
    agent any

    stages {
        stage('Git-Chekout') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/SharonKarichaly/Jenkins-Python-Pipeline.git']]])
            }
        }
        stage('Build/Execute the remote script') {
            steps {
            git branch: 'main', url: 'https://github.com/SharonKarichaly/Jenkins-Python-Pipeline.git'
            sh 'python3 python.py'
            sh 'python3 python.py > Server-Details'
            }
        
        }
    }
}
