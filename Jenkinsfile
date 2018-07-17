pipeline {
  agent any
  stages {
    stage('Build WebApp') {
      parallel {
        stage('Build WebApp') {
          steps {
            build 'Build Control Pipeline'
          }
        }
        stage('Build C++') {
          steps {
            build 'angularDependencyManagement'
          }
        }
      }
    }
  }
}