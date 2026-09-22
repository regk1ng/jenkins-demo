pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo '开始拉取 GitHub 代码...'

                sh '''
                    rm -rf jenkins-demo
                    git clone git@github.com:regk1ng/jenkins-demo.git
                '''
            }
        }

        stage('Check') {
            steps {
                echo '检查代码...'

                sh '''
                    cd jenkins-demo
                    ls -lah
                    git log -1
                '''
            }
        }

        stage('Build') {
            steps {
                echo '执行构建...'

                sh '''
                    cd jenkins-demo
                    echo "Build Success"
                '''
            }
        }

        stage('Deploy') {
            steps {
                echo '执行部署...'

                sh '''
                    echo "Deploy Success"
                '''
            }
        }
    }

    post {
        success {
            echo '流水线执行成功！'
        }

        failure {
            echo '流水线执行失败！'
        }
    }
}
