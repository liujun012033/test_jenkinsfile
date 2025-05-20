@Library('shared_jenkins') _
import com.bne.utils.Utils

pipeline {
    agent any
    stages {
        stage('Test') {
            steps {
                script {
                    Utils.printHello(this)
                    deploy appName: 'my-app', environment: 'prod'
                    def dockerTemplate = libraryResource 'com/company/templates/dockerfile.template'
                    writeFile file: 'Dockerfile', text: dockerTemplate.replace('${appJar}', 'my-app.jar')
                }
            }
        }
    }
}
