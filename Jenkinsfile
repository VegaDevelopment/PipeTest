pipeline {
  agent any
  stages {
    stage('Stufe 1') {
      parallel {
        stage('Stufe 1') {
          steps {
            echo 'Hallo, ich bin Stufe 1'
            bat 'set'
            build(job: 'Projekt1', wait: true)
          }
        }
        stage('Stufe 2') {
          steps {
            build(job: 'Projekt2', wait: true)
          }
        }
      }
    }
    stage('Stufe 3') {
      steps {
        build 'VEGALOGProxy.Setup'
      }
    }
  }
}