pipeline {
  agent any
  stages {
    stage('CloneRepo') {
      steps {
        git(url: 'https://github.com/odoo/docker.git', branch: 'master')
      }
    }

    stage('Build Odoo') {
      parallel {
        stage('v13') {
          steps {
            sh 'docker build -t odoo_v13:20220903 /var/jenkins/workspace/docker_odoo_master/13.0/'
          }
        }

        stage('v14') {
          steps {
            sh 'docker build -t odoo_v14:20220903 /var/jenkins/workspace/docker_odoo_master/14.0/'
          }
        }

        stage('v15') {
          steps {
            sh 'docker build -t odoo_v15:20220903 /var/jenkins/workspace/docker_odoo_master/15.0/'
          }
        }

      }
    }

  }
}