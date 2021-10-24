node {
    stage('SCM Checkout') {
        git 'https://github.com/sunnynjoy/jenkins-pro'
    }
    stage('Compile-Package') {
       sh 'mvn package'
    }
    stage('Slack Notification'){
    slackSend channel: '#jenkins',
    color: 'good',
    baseUrl: 'https://hooks.slack.com/services/',
    message: 'welcome to Jenkins, Slack!',
    teamDomain: 'joyfeebles',
    tokenCredentialId: 'slack-demo'
    }
}