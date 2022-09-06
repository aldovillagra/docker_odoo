pipeline {
  agent any
  stages {
    stage('CloneRepo') {
      steps {
        git(url: 'https://github.com/odoo/docker.git', branch: 'master')
      }
    }

    stage('Build v13') {
      steps {
        sh 'docker build -t odoo_v13:20220903 /var/jenkins/workspace/docker_odoo_master/13.0/'
      }
    }

  }
}