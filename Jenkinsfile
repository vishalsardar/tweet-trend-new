pipeline {
    agent {label 'maven'}


environment {
    PATH = "/opt/apache-maven-3.9.4/bin:$PATH"
}
    stages {
       stage("build"){
        steps {
            sh 'mvn clean deploy'
        }
       
    }

    stage('SonarQube analysis') {
    environment{
      scannerHome = tool 'namg-sonar-scanner'
    }
    
    steps {
    withSonarQubeEnv('namg-sonarqube-server') {
        sh "${scannerHome}/bin/sonar-scanner"
    }
    }
  } 
}
}
