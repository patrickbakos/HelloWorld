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
        sh 'java -version'
        sh 'javac src/HelloWorld.java'
        sh 'java -cp "src/" HelloWorld'
        }
     }
    stage('Merge into master') {
      steps {
        sh 'git config user.email "${params.git_username}"'
        sh 'git config user.name "${params.git_password}"'
        sh 'git checkout master'
        sh 'git pull'
        sh 'git merge origin/develop'
        sh 'git push'
      }
    }
 }
 }
