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
                sh "docker run -it --rm -v $(pwd):/app prooph/github-changelog-generator"
            }
        }

    }
}
