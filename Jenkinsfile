pipeline {
    agent { node { label 'prueba_test' } }

    stages {
        stage('Install') {
            steps {
                bat "start /B npm -v"
                bat "start /B npm install"
            }
        }
        stage('Test'){
             steps {
                   bat "start /B npm run test"
                  }
               }
        stage('Build'){
            steps {
                bat "start /B npm run build"
            }
        }
        stage('Security_test') {
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
