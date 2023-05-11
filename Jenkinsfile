node {
    stage('SCM') {
        git branch: 'main', url: 'insert github project url here', credentialsId: ''
    }
    stage('SonarQube analysis') {
        def scannerHome = tool 'SonarQube Scanner';
        withSonarQubeEnv('Sonarqube') { // If you have configured more than one global server connection, you can specify its name
            sh "${scannerHome}/bin/sonar-scanner"
        }
    }
}