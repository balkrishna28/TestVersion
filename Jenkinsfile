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

                        //sh 'git clone git@github.com:balkrishna28/TestVersion.git'
                        //sh 'git ls-remote -h --refs git@github.com:balkrishna28/TestVersion.git master |awk "{print $1}"'
                        //sh "docker pull ferrarimarco/github-changelog-generator"
                        //sh 'git checkout master'
                        //sh 'docker run --rm -v "$(pwd)":/usr/local/src/your-app ferrarimarco/github-changelog-generator --user  balkrishna28  --project TestVersion'
                        sh 'touch TEST.md'
                        //sh 'cd /var/lib/jenkins/workspace/TestVersionNumber'
                        //sh 'ls'
                        //sh 'git config user.name "balkrishna28"'
                        //sh 'git config user.email "balkrishna36@gmail.com"'
                        //sh 'git remote set-url origin https://github.com/balkrishna28/TestVersion.git'
                        //sh 'git remote add origin git@github.com:balkrishna28/TestVersion.git'
                        //sh 'git remote -v'
                        //sh 'git branch -a'
                        sh 'git add TEST.md'
                        sh 'git commit -m "its not working"'

                        //sh 'git pull'
                        sh 'git push origin HEAD:master'
                        //sh 'git commit -m "its not working"'
                        //sh 'git branch'
                        //sh 'git  push origin HEAD:master'
                    }
                }
            }
        }
    }
}
