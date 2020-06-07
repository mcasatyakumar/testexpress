node {
     
     def nodeHome = tool 'nodejs'
     env.PATH="${env.PATH}:${nodeHome}/bin"
   
     
 
     stage("Checkout") {
      
       echo ("Git Checkout")
       checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'ad2c3325-2572-46da-933e-8adad09a4648', url: 'https://github.com/mcasatyakumar/testexpress.git']]]) 
     }
  
     stage("Build") {
       echo ("Building NodeJs App")
       sh label: '', script: 'npm install'
     
     }


}
