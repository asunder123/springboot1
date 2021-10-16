pipeline {
agent any
tools {
maven "maven"
}
stages {
stage("Cleaning stage") {
steps {
sh "mvn clean install"
}
}
stage('Artifact Upload') {
steps {
  nexusArtifactUploader artifacts: [[artifactId: 'SpringAID', classifier: '', file: '/var/lib/jenkins/workspace/groovy test script/target/demo-1.0-SNAPSHOT.jar', type: 'jar']], credentialsId: 'a5512406-b633-44f5-af09-6031f17fa719', groupId: 'SpringGID', nexusUrl: '192.168.163.132:8081/', nexusVersion: 'nexus3', protocol: 'http', repository: 'maven-snapshots', version: '1.0-SNAPSHOT'
  nexusArtifactUploader artifacts: [[artifactId: 'SpringAID', classifier: '', file: '/var/lib/jenkins/workspace/groovy test script/target/demo-1.0-SNAPSHOT.jar', type: 'jar']], credentialsId: 'a5512406-b633-44f5-af09-6031f17fa719', groupId: 'SpringGID', nexusUrl: '192.168.163.132:8081/', nexusVersion: 'nexus3', protocol: 'http', repository: 'maven-releases', version: '2.2.3.RELEASE'
}
}
}
}
