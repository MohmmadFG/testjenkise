pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                                // سحب الكود من GitHub باستخدام SSH
                git branch: 'main', url: 'git@github.com:MohmmadFG/testjenkise.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Building project.. sdadsada.'
                // يمكن هنا إضافة أوامر البناء مثل mvn build أو npm build
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                // هنا يمكن وضع أوامر تشغيل الاختبارات
            }
        }
    }
}
