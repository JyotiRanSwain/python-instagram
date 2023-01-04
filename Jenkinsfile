pipeline {
    agent any
   stages{
    stage('build') {
      steps {
        sh 'pip install -r requirements.txt'
      }
    }
    stage('test') {
      steps {
        sh 'python tests.py'
      }   
    }

stage ('Build python package') {
            steps {
                sh 'python setup.py sdist bdist_wheel'
            }
        }
        }
    }
