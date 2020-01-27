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
                sh "docker run -it --rm -v "$(pwd)":/usr/local/src/your-app ferrarimarco/github-changelog-generator"
            }
        }

    }
}
