node {
    stage('SCM Checkout') {
        git 'https://github.com/sunnynjoy/jenkins-pro'
    }
    stage('Compile-Package') {
       sh 'mvn package'
    }
    stage('Slack Notification'){
    slackSend channel: '#jenkins',
    baseUrl: 'https://hooks.slack.com/services/'
    color: 'good',
    message: 'welcome to Jenkins, Slack!',
    teamDomain: 'joyfeebles',
    tokenCredentialId: 'slack-demo'
    }
}