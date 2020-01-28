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
                
                docker.image("ferrarimarco/github-changelog-generator").inside("--volume $WORKSPACE:/app"){
                    sh script: "ferrarimarco/github-changelog-generator -v"
                }
                //sh "docker run ferrarimarco/github-changelog-generator  --user  balkrishna28  --project TestVersion " 
            }
        } 
    }
}
