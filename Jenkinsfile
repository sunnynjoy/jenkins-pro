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
    message: 'welcome to Jenkins, Slack!',
    teamDomain: 'joy_feebles',
    tokenCredentialId: 'slack-demo'
    }
}