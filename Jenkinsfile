node {
    stage('SCM Checkout') {
        git 'https://github.com/sunnynjoy/jenkins-pro'
    }
    stage('Compile-Package') {
       sh 'mvn package'
    }
}