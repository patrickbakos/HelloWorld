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
      tools {
        jdk "jdk-1.13.0"
                }
      steps {
        sh 'java -version'
        sh 'javac src/HelloWorld.java'
        sh 'java -cp "src/" HelloWorld'
        }
     }
 }
 }
