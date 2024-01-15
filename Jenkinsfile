pipeline {
    agent { node { label 'local-test' } }

    stages {
        stage('Build') {
            steps {
                sh "python3 --version"
            }
        }
        stage('Test') {
            steps {
                echo 'testing..'
            snykSecurity(
          snykInstallation: 'snyk_security',
          snykTokenId: 'andrespuerto1993',
        )
            }
        }
    }
}
