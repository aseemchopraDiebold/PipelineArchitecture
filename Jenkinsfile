pipeline {
  agent any
  stages {
    stage('Build Control Pipeline') {
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
    stage('Build Smart App') {
      steps {
        echo 'Hello Smart App Build Stage'
      }
    }
  }
}