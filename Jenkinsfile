// pipeline {
//     agent {
//         node {
//             label 'docker-agent-python'
//             }
//       }
//     triggers {
//         pollSCM '* * * * *'
//     }
//     stages {
//         stage('Build') {
//             steps {
//                 echo "Building.."
//                 sh '''
//                 cd myapp
//                 pip install -r requirements.txt
//                 '''
//             }
//         }
//         stage('Test') {
//             steps {
//                 echo "Testing.."
//                 sh '''
//                 cd myapp
//                 python3 hello.py
//                 python3 hello.py --name=Arshana
//                 '''
//             }
//         }
//         stage('Deliver') {
//             steps {
//                 echo 'Deliver....'
//                 sh '''
//                 echo "doing delivery stuff.."
//                 '''
//             }
//         }
//     }
// }

//===================================================================
//*******Getting docker file from repository

// pipeline {
//     agent { dockerfile true }
//     stages {
//         stage('Test') {
//             steps {
//                 sh 'node --version'
//                 sh 'svn --version'
//             }
//         }
//     }
// }

// ===========================================
//*******Getting docker file from external(Dockerhub ?)

pipeline {
    agent { docker { image 'node:18.16.0-alpine' } }
    stages {
        stage('Test') {
            steps {
                sh 'node --version'
                echo 'testing with jenkins file with docker images'
            }
        }
    }
}
