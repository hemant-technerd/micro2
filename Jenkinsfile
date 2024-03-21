pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Jenkinsfile Fix-235'
            }
        }
        stage('for the fix branch') {
            when {
                branch "fix-"
            }
            steps {
                sh '''
                cat README.md
                '''
            }
        }
        stage('for the PR') {
            when {
                branch "PR-*"
            }
            steps {
                sh "echo this only runs for PRs"
            }
        }
    }
}
