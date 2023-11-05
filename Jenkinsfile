 pipeline{
  agent { label any }
  environment { CI = 'false'}
 // tools {nodejs "node"}
    stages{
        stage('Build and Deploy Polaris GPT API') {
             when {
                allOf {
                    expression { env.CHANGE_TARGET == 'development'  }
                //    changeset 'packages/core/services/metrics-management/**'
                }
            }
            steps{
                sh 'sudo systemctl restart jenkins'
            }
        }
    }
}
