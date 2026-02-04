@Library('my-shared-lib') _

pipeline {
  agent {
    docker {
      image 'docker:27-cli'
      args '-v /var/run/docker.sock:/var/run/docker.sock'
    }
  }
  
  parameters {
    booleanParam(name: 'SKIP_TESTS', defaultValue: false)
  }
  
  stages {
    stage('Run Java Pipeline') {
      steps {
        javaProject(
          skipTests: params.SKIP_TESTS,
          image: 'sample-java'
        )
      }
    }
  }
}