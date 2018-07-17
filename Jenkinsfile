pipeline {
  agent any
  stages {
    stage('Build Control') {
      parallel {
        stage('Build WebApp') {
          steps {
            build 'Build Control Pipeline'
          }
        }
        stage('Build Vista') {
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
    stage('Test Control Pipeline') {
      steps {
        build 'Test Control Pipeline'
      }
    }
  }
}