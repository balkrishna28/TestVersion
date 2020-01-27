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
                docker.image(ferrarimarco/github-changelog-generator){
                    echo "test"
                }
            }
        }

    }
}
