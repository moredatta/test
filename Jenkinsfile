pipeline {
    agent any

    environment {
        SOURCE_BRANCH = 'origin/dev'
        TARGET_BRANCH = 'main'
        GITHUB_CREDENTIALS = 'gitub-creds' // This should be set up in Jenkins
    }

    stages {

        stage('Merge') {
            steps {
                script {
                    //sh "git checkout ${TARGET_BRANCH}"
                    
                 //   sh "git merge ${SOURCE_BRANCH} --no-ff -m 'Merge ${SOURCE_BRANCH} into ${TARGET_BRANCH}'"
                    //sh "git push origin ${TARGET_BRANCH}"
                   sh 'git pull origin main --allow-unrelated-histories'
                    sh 'git checkout dev'
                    sh 'git merge main'
                    sh 'git push -u origin dev'
                }
            }
        }
    }
}
