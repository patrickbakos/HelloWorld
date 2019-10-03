pipeline {
agent any
  stages {
    stage('Git clone') {
      steps {
        sh 'rm -rf HelloWorld'
        sh 'git clone https://github.com/patrickbakos/HelloWorld.git'
        }
    }
    stage('Run') {
      steps {
        sh 'javac src/HelloWorld.java'
        sh 'java src/HelloWorld'
        }
     }
 }
 }
