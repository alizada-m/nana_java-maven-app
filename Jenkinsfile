pipeline {
  
  agent any
     
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
              choise(name: 'ENV',choices: ['dev','staging','prod'], description: '')
            }
            
          }
            steps{
            echo "Deploying the application..."
              echo "Deploy to ${ENV}"
            }
     }
     }
}
