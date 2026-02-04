@Library('my-shared-lib') _

pipeline {
  agent any
  
  stages {
    stage('Run Java Pipeline') {
      steps {
        script {
          javaProject()
        }
      }
    }
  }
}
