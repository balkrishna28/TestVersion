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
                docker run -it --rm -v "$(pwd)":/usr/local/src/TestVersion ferrarimarco/github-changelog-generator"
            }
        }
    }
}
