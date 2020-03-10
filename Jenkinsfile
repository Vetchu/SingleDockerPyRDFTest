node() {
    stage ("Get image") {
        git 'http://localhost:3000/Vetch/DockerBaseTest.git'
    }
    stage("Build image"){
        def pyrdf = docker.build("dockerpyrdf .","--network='host'")
    }
    stage("Run image"){
        pyrdf.inside{
            sh '. root/bin/thisroot.sh && python2 PyRDF/introduction.py'
        }
    }
}