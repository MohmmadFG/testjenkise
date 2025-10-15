pipeline {
    agent any
    tools {
        go 'golastversin'
    }
    stages {
        stage('Checkout') {
            steps {
                                // سحب الكود من GitHub باستخدام SSH
                git branch: 'main', url: 'git@github.com:MohmmadFG/testjenkise.git'
            }
        }


        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'go test ./...'
                echo "test succes"
            }
        }
    }
}
