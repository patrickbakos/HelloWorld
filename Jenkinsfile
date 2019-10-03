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
      agent {
        docker { image 'openjdk:13-jdk' }
        }
      steps {
        sh 'java -version'
        sh 'javac src/HelloWorld.java'
        sh 'java -cp "src/" HelloWorld'
        }
     }
 }
 }
