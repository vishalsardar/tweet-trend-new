pipeline {
    agent {label 'maven'}
    stages {
        stage('Clone') {
            steps {
                git branch: 'main', url: 'https://github.com/Namg04/tweet-trend-new.git'
            }
        }
    }
}
