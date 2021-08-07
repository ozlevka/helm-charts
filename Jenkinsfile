pipeline {
    agent {
        kubernetes {
            yaml """
kind: Pod
apiVersion: v1
metadata:
  labels:
    jenkins: "true"
spec:
  containers:
  - name: jenkins-test
    image: ubuntu:18.04
    command:
        - /bin/bash
        - -c
        - "while sleep 1000; do :; done"
            """
        }
    }
    
    stages {
        stage("Hello world") {
            steps {
                sh """
                    echo "Hello world"
                """
            }
        }
    }
}