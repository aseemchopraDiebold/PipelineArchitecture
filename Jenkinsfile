pipeline {
  agent any
  stages {
    stage('Build Vista') {
      parallel {
        stage('Build WebApp') {
          steps {
            build 'Build Control Pipeline'
          }
        }
        stage('Build C++ Customization') {
          steps {
            build 'angularDependencyManagement'
          }
        }
      }
    }
    stage('Build Vista Smart App') {
      steps {
        echo 'Hello Smart App Build Stage'
      }
    }
    stage('Test Terminal App') {
      steps {
        build 'Test Control Pipeline'
      }
    }
  }
}