pipeline {
    agent { node { label 'prueba_test' } }

    stages {
        stage('Install') {
            steps {
                sh "npm -v"
                sh "npm install"
            }
        }
        stage('Test'){
             steps {
                   sh "npm run test"
                  }
               }
        stage('Build'){
            steps {
                sh "npm run build"
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
