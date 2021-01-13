pipeline
 {
  agent any
  stages{
   stage('Build Application'){
   steps{
   bat 'mvn clean install'
   }
   }
   
   stage('Deploy Application to CloudHub'){
   steps{
   bat 'mvn package deploy -DmuleDeploy'
   }
   }
   
   stage('Regression Testing'){
   steps{
   bat 'CD C:\\Users\\shefr\\AppData\\Roaming\\npm\\newman run "C:\\NJC Labs\\Projects\\PostManCollection\\worldtimezone.postman_collection.json"'
   }
   }
  }
 
 }