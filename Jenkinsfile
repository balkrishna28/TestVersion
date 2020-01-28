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
                sh "docker run ferrarimarco/github-changelog-generator  --user  balkrishna28  --project TestVersion " 
                sh "docker run -it --rm -v "$(pwd)":/usr/local/src/your-app ferrarimarco/github-changelog-generator"

            }
        } 
    }
}
