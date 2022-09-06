pipeline {
  agent any
  stages {
    stage('CloneRepo') {
      steps {
        git(url: 'https://github.com/odoo/docker.git', branch: 'master')
      }
    }

  }
}