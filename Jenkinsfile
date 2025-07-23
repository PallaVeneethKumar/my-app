@Library("sharedlibrary2") _
pipeline {
  agent any
  tools {
    maven 'maven2'
  }
  stages{
    stage("Maven Build"){
      steps{
        sh "mvn clean package"
      }
    }
    stage("Deploy To Dev"){
      steps{
        tomcatDeploy("tomcat-dev","ec2-user",["172.31.88.123","172.31.88.123"])
      }
    }
  }
}
