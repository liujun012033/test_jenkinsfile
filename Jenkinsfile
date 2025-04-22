pipeline {
    agent {
        any
        // 禁止默认的代码拉取行为
        options {
            skipDefaultCheckout(true)
        }
    }
    stages {
        stage('test') {
            steps {
                sh 'ls -al'
            }
        }
    }
    post {
        success {
            echo 'Pipeline 执行成功！'
        }
        failure {
            echo 'Pipeline 执行失败，请检查日志！'
        }
    }
}    
