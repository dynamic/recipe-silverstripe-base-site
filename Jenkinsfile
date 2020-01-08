pipeline {
  agent any
  stages {

    stage('Build') {
      steps {
        sh 'mkdir silverstripe-cache'
        sh 'composer require --prefer-dist --no-update silverstripe-themes/simple:~3.2'
        sh 'composer update --no-suggest --prefer-dist'
      }
    }

    stage('Cleanup') {
      steps {
        sh 'rm -rf silverstripe-cache'
      }
    }
  }
}
