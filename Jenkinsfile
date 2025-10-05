@Library('my-shared-library') _
pipeline {
  agent any
  stages {
    stage('test shared library') {
      steps {
        hello('Shreya')
      }
    }
    stage('shared lib execution') {
      steps {
         script {
          def util = new org.example.HelloUtils(this)
          util.sayHelloJenkins()
        }
      }
    }
  }
}
