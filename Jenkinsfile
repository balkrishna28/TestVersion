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
                sshagent (credentials:['github-key']){
                    script {
                        
                        sh "docker pull ferrarimarco/github-changelog-generator"
                        //sh 'git pull origin master'
                        //sh 'git checkout master'
                        sh 'docker run --rm -v "$(pwd)":/usr/local/src/your-app ferrarimarco/github-changelog-generator --user  balkrishna28  --project TestVersion'
                        //sh 'cd /var/lib/jenkins/workspace/TestVersionNumber'
                        //sh 'ls'
                        //sh 'git pull'
                        sh 'git add CHANGELOG.md'
                        //sh 'git commit -m "Auto add changelog"'
                        //sh 'git pull'
                        sh 'git push origin HEAD:master'
                    }
                }
            }
        }
    }
}
