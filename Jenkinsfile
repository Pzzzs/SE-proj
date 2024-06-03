pipeline {
    agent any

    stages {

        stage('Install Vue CLI') {
            steps {
                // 全局安装 Vue CLI
                sh 'npm install -g @vue/cli'
            }
        }

        stage('Install Dependencies') {
            steps {
                // 使用npm安装项目依赖
                sh 'npm install'
            }
        }

        stage('Build') {
            steps {
                // 运行构建命令
                sh 'npm run build'
            }
        }

        stage('Archive Artifacts') {
            steps {
                // 存档构建产物以供后续步骤使用
                archiveArtifacts artifacts: 'dist/**', allowEmptyArchive: true
            }
        }

        // stage('Deploy') {
        //     steps {
        //         // 假设你有一个部署脚本来处理部署
        //         sh './deploy.sh'
        //     }
        // }
         
    }
}
