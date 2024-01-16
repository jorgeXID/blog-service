pipeline {
    agent { node { label 'prueba_test' } }

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
          snykInstallation: 'prueba_snyk',
          snykTokenId: 'token_snyk',
        )
            }
        }
    }
}
