pipeline {
agent any
  environment {
  KAKA='MAKA'
  }
  stages {
    stage('Git clone') {
      steps {
        sh 'echo $KAKA'
        sh 'rm -rf HelloWorld'
        sh 'git clone https://github.com/patrickbakos/HelloWorld.git'
        }
    }
    stage('Run') {
      steps {
        sh 'java -version'
        sh 'javac src/HelloWorld.java'
        sh 'java -cp "src/" HelloWorld'
        }
     }
    stage('Merge into master') {
      steps {
        sh 'ls'
        sh 'git checkout master'
        sh 'git pull'
        sh 'git merge origin/develop'
        sh 'git push https://$git_username:$git_password@github.com/patrickbakos/HelloWorld.git'
      }
    }
 }
 }
