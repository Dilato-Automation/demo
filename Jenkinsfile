pipeline {
  agent any
  stages {
    stage('stage 1 - test xxx') {
      steps {
        build 'Stage1_xxx'
      }
    }
    stage('stage 2 - test xxx') {
      parallel {
        stage('stage 2 - test xxx') {
          steps {
            build 'Stage2_xxx'
          }
        }
        stage('stage 2 - test xxx2') {
          steps {
            build 'Stage3_xxx'
          }
        }
      }
    }
    stage('stage 3 - test xxx') {
      steps {
        catchError() {
          build 'Stage4_xxx'
        }

      }
    }
  }
}