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
                //docker.image('ferrarimarco/github-changelog-generator').withRun('-p 3306:3306')
                sh "docker run ferrarimarco/github-changelog-generator  --user  balkrishna28  --project TestVersion --rm "$(pwd)":/usr/local/src/NIA"
            }
        }
    }
}
