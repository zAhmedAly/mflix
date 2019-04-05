pipeline {
  agent any
    
  tools {nodejs "NodeJS"}
    
  stages {
        
    stage('Cloning Git') {
      steps {
        git 'https://github.com/zAhmedAly/mflix'
      }
    }
        
    stage('Install dependencies') {
      steps {
        sh 'npm install'
      }
    }
stage('Check Node Config') {
      steps {
        sh 'npm config ls'
      }
    }     
    stage('Test DB connection') {
      steps {
         sh 'npm test -t db-connection'
      }
    }   
    stage('Test All') {
      steps {
         sh 'npm test'
      }
    }      
  }
}
