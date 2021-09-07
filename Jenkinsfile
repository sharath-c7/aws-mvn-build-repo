node{
  stage('SCM Checkout'){
        checkout([$class: 'GitSCM', branches: [[name: '*/main']],
    userRemoteConfigs: [[url: 'https://github.com/sharath-c7/aws-mvn-build-repo/']]])
  }
  stage('Compile-Package'){
    // Get maven Home path
    def mvnHome = tool name: 'maven-3', type: 'maven'
    sh "${mvnHome}/bin/mvn package"
  }
  stage('Email notification'){
    mail bcc: '', body: '''Hi Welcome to jenkins email alerts
    Thanks,
    Sharath''', cc: '', from: '', replyTo: '', subject: 'Jenkins Job Status', to: 'sharath.c721@gmail.com'
  }
}
