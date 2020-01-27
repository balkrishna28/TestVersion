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
                sh "docker pull prooph/github-changelog-generator"
                sh "github_changelog_generator --help"
            }
        }

    }
}
