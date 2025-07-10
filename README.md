# создание просто nginx через k8s
до работы с k8s нужно установить  ... и настроить ...
1) создал NS `kubectl create namespace my-app`
2) пишем код для pod и сервис
3) запускаем `kubectl apply -f deployments/ -f services/`
4) kubectl get pods -n my-app -w - проверяем что все норм с контейнерами
5)   ждем EXTERNAL-IP `kubectl get svc -n my-app -w` и проверяем http://EXTERNAL-IP
<img width="2380" height="752" alt="image" src="https://github.com/user-attachments/assets/087a2bd8-3a2b-4c58-8cf9-471dd100f5ea" />
6) `kubectl delete namespace my-app`        - удалил NS
7) Но после удаления что-то пошло не так - применил конмаду `kubectl delete namespace my-app`       
