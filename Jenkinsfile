node{
  stage('SCM Checkout'){
  git 'https://github.com/sharath-c7/aws-mvn-build-repo'
  }
  stage('Compile-Package'){
  sh 'mvn package'
  }
}
