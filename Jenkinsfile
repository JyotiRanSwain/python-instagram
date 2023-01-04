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

    stage ('Upload packages') {
        steps {
            rtUpload (
                serverId: "ARTIFACTORY_SERVER",
                    spec: '''{
                        "files": [
                            {
                                "pattern": "dist/",
                                "target": "artifactory-python-dev-local/"
                            }
                        ]
                    }'''
                )
            }
        }
        }
    }
