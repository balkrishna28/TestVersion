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
                sh script: "docker run -it --rm -v "$(pwd)":/usr/local/src/TestVersion ferrarimarco/github-changelog-generator"
            }
        }

    }
}
