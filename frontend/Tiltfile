docker_build('fyc-frontend', '.', live_update=[sync("./src/**/*", "/app/src")])
k8s_yaml('deployment.yml')
k8s_resource('fyc-frontend', port_forwards='8080:5173')
