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
                script{
                sh "docker pull ferrarimarco/github-changelog-generator"
                // docker run -it --rm -v "$(pwd)":/usr/local/src/your-app ferrarimarco/github-changelog-generator
                
                sh "docker run -it --rm -v "$(pwd)":/usr/local/src/TestVersion arimarco/github-changelog-generator  --user  balkrishna28  --project TestVersion" 
            }
            }
        } 
    }
}
