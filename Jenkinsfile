pipeline { 
  
   agent any

   stages {
   
     stage('Install Dependencies') { 
        steps { 
           sh 'npm install' 
        }
     }
     
     stage('master branch') { 
       when {
         anyOf {
             branch 'master';
         }
       }
       steps { 
           sh 'echo "running only on master branch"'
       }
     }

     stage('Non master branch') { 
       when {
         not {
           anyOf {
               branch 'master';
           }
         }
       }
       steps { 
           sh 'echo "running on non-master branch"'
       }
     }
   }
}
