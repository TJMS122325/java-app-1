@Library('my-shared-lib') _
pipeline {
  agent any
  parameters {
    booleanParam(name: 'SKIP_TESTS', defaultValue: false)
  }
  stages {
    stage('Java Pipeline') {
      steps {
        javaProject(
          skipTests: params.SKIP_TESTS,
          image: 'sample-java'
        )
      }
    }
  }
}
