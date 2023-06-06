pipeline {
    agent {
        label "demoAgent"
    }
    stages {
        stage('git') {
            steps {
                git branch: 'main', url: 'https://github.com/cofls6581/Jenkins-Webhook-Heterogeneous-agent.git'
            }
        }        
        stage('mvn') {
            steps {
                sh "mvn -Dmaven.test.failure.ignore=true clean test"
            }
        }
    }
}
