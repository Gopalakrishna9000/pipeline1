node ('jdk8'){
    stage ('source code') {
        gitbranch : 'master', url: 'https://github.com/Gopalakrishna9000/time-tracker.git'
    }
     stage ('build') {
           sh 'mvn clean package'
    }
    stage ('Archiving and Test Results') {
               junit '**/surefire-reports/*.xml'
               archiveArtifacts artifacts: '**/*.war', followSymlinks: false
    }
    
}
