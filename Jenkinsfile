pipeline { 
   agent { 
       docker { 
           image 'gcc:latest'
           args '-u root: '
       } 
   } 
   stages { 
       stage('Build') { 
           steps { 
               sh 'cl -o hello hello.c'
           } 
       } 
       stage('Archive') { 
           steps { 
               archiveArtifacts 'hello'
           } 
       } 
   } 
}