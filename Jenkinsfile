node('DOTNET6') {
    stage('SCM'){
        checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false,
        extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/sstiven/dotnet6']]])
    }
    stage('Build'){
        sh 'dotnet build .'
    }
    stage('Test'){
        echo 'Execute unit test'
    }
    stage('Package'){
        echo 'Zip it up'
    }
    stage('Deploy'){
        echo 'Push to deployment'
    }
}
