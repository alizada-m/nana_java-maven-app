pipeline {
  
  agent any
  parameters{
    choice(name:'ENV',choices:['dev','staging','prod'], description: '')
    booleanParam(name: 'executeTests', defaultvalue: true, description: '')
  }
     
     stages{
        
        stage("Build"){
            
            steps{
            echo "Building the application..."
            }
     }
        stage("Test"){
          
            
            steps{
            echo "Testing the application..."
            }
     }
        stage("Deploy"){
          input {
            message "Select the environment to deploy to"
            ok "Done"
            parameters {
              choice(name: 'ENV',choices: ['dev','staging','prod'], description: '')
            }
            
          }
            steps{
            echo "Deploying the application..."
              echo "Deploy to ${ENV}"
            }
     }
     }
}
