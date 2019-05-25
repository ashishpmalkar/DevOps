pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        build 'mydevOpsMaven'
      }
    }
    stage('Deploy') {
      steps {
        bat(returnStatus: true, script: 'cls echo Deleting class file del *.class echo compiling javac *.java java App echo All Done!!', returnStdout: true)
      }
    }
    stage('') {
      steps {
        input(message: 'Approve ?', id: 'approve', submitter: 'Ashish Malkar', submitterParameter: 'yes')
      }
    }
  }
}