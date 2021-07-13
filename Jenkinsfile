pipeline {
    agent {label "master"}
    stages {
        stage('Hello'){
            steps{
                echo "hell from Jenkinsfile"
            }
        }

        stage('for the fix branch'){
            when {
                branch "fix-*"
            }
            steps{
                sh '''
                    cat REAMME.md
                '''
            }
        }

        stage('for the PR'){
            when{
                branch 'PR-*'
            }
            steps{
                echo 'this only runs for the PRs'
            }
        }
    }
}
