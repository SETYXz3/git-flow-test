pipeline {
    agent any
    // 上記の「Global Tool Configuration」で設定したnameを指定
    tools { nodejs "nodejs" }
    stages {
        stage("Clean Up"){
            steps {
                deleteDir()
            }
        }
        stage('Install') {
            steps {
                dir ("git-flow-test/test-app") {
                  sh 'npm install'
                }
            }
        }
        stage('Build') {
            steps {
                dir ("git-flow-test/test-app") {
                  sh 'npm run build'
                }
            }
        }
    }
}
