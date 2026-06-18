pipeline{
  agent any
  tools{
    maven 'Maven'
  }
  stages{
    stage('checkout'){
      steps{
        git 'https://github.com/Ranjana2225/guava1.git'
      }
    }
    stage('Build'){
      steps{
        sh 'mvn clean install'
      }
    }
    stage('adding text to source'){
          steps{
            sh 'echo "this is copied text from source" >source.txt'
          }
          }
     stage('Run'){
       steps{
         sh'mvn exec:java -Dexec.mainClass="com.example.App"'
       }
     }
     stage('verification'){
       steps{
         sh 'cat destination.txt'
       }
     }
          }
          }
