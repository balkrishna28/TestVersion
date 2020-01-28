pipeline {
    agent any
    stages {
        stage ("test") {
            steps{
                echo "its working"
            }
        }
        stage ("docker") {
            steps{
                script {
                    sh "docker pull ferrarimarco/github-changelog-generator"
                    // docker run -it --rm -v "$(pwd)":/usr/local/src/your-app ferrarimarco/github-changelog-generator
                
                    sh 'docker run --rm -v "$(pwd)":/usr/local/src/your-app ferrarimarco/github-changelog-generator --token fc3bf78663f302344be6eb9a02626578fee63a81 --user  balkrishna28  --project TestVersion'
                    sh 'cd /var/lib/jenkins/workspace/TestVersionNumber'
                    sh 'ls'
                    sh 'git push CHANGELOG.md HEAD:TestVersion'
                }
            }
        } 
    }
}
