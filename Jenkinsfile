pipeline {
    agent any
    stages {
        stage("Clean Up"){
            steps {
                deleteDir()
            }
        }
        stage("Clone Repo"){
            steps {
                sh "git clone https://github.com/SETYXz3/git-flow-test.git"
            }
        }
        stage("Build"){
            steps {
                dir("test-app") {
                    sh "npm run build"
                }
            }
        }
        // stage("Test"){
        //     steps {
        //         dir("simple-java-maven-app") {
        //             sh "mvn test"
        //         }
        //     }
        // }
    }
}