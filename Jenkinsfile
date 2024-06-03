pipeline {
    agent any

    stages {
        

        stage('Navigate to Frontend Directory') {
            steps {
                dir('frontend') {
                    // 全局安装 Vue CLI
                    sh 'npm install -g @vue/cli'

                    // 使用 npm 安装项目依赖
                    sh 'npm install'

                    // 运行构建命令
                    sh 'npm run build'
                }
            }
        }

        stage('Archive Artifacts') {
            steps {
                dir('frontend') {
                    // 存档构建产物以供后续步骤使用
                    archiveArtifacts artifacts: 'dist/**', allowEmptyArchive: true
                }
            }
        }

        
        
    }

    
}