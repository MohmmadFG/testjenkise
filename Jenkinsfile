pipeline {
    agent any
    tools {
        go 'golastversin'
    }
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'git@github.com:MohmmadFG/testjenkise.git'
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests.....'
                sh 'go test ./...'
                echo "Test success"
            }
        }
        stage('Build Image') {
            steps {
                script {
                    def imag = docker.build("myapp:1.1")
                    docker.withRegistry('https://index.docker.io/v1/', 'dockerhubC') {
                        imag.push('latest')
                    }
                }
            }
        }
    }
}
