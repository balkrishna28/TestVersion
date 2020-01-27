pipeline {
    agent any 
    stages {
        stage ("test"){
            steps{
                echo "its working"
            }
        }
        stage ("docker"){
            steps{
                sh "docker pull ferrarimarco/github-changelog-generator"
                sh "docker run ferrarimarco/github-changelog-generator - v"
            }
        }

    }
}
