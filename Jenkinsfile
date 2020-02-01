node{
    stage('Git Clone'){
        git 'https://github.com/uma-2207/calcwebapp.git'
    }
    stage('Maven Package'){
        def javahome = tool name: 'Java', type: 'JDK'
        def mvnHome = tool name: 'Maven', type: 'maven'
        sh "${mvnHome}/bin/mvn package"
    }
    stage('Deployment'){ 
        sh 'cp target/*.war /opt/tomcat/webapps'
    }    
}
