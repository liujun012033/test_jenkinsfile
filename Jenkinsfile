pipeline{
  agent any
  stages{
    stage(test){
        sh 'ls -al'
    }
  }
   post {
        success {
            // 构建成功后发送通知
            echo 'Pipeline 执行成功！'
        }
        failure {
            // 构建失败后发送通知
            echo 'Pipeline 执行失败，请检查日志！'
        }
    }
}
