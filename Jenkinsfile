pipeline{
    agent{
         label 'agent1'
    }
    parameters{
                    string(name: "name", defaultValue: "vimalesh")
                } 
    stages{
        stage('Build'){
            steps{
                echo(message: 'build')
                echo(message: "Build ID: ${env.BUILD_ID}, Name : ${name}")                
            }            
        }
        stage('Test'){
            steps{
                echo(message: 'Test')
                echo(message: "Build ID: ${env.BUILD_ID}, Name : ${name}")            
            }            
        }
        stage('Publish'){
            steps{
                echo(message: 'Publish') 
                echo(message: "Build ID: ${env.BUILD_ID}, Name : ${name}")            
                sh(script: 'hostname')
                 sh(script: 'ls -la')           
            }            
        }
        
    }
    post{
            always {
                script("post script"){
                    if (currentBuild.result == 'SUCCESS') {
                        echo "Build Succeeded!"
                        echo(message: " pervious build  : ${currentBuild.previousBuild}")
                    } else {
                        echo "Build Failed!"
                    }
                }
            }
              
        }
}