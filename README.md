### AWS 

# ## Инфраструктура:

Общая инфраструктура находится в AWS***** и состоит из одного (в данном примере) сервера с Ubuntu в качестве операционной системы. 
Точкой входа в инфраструктуру будет AWS load-balancer, который будет терминировать SSL (SSL termination) и заботиться о дальнейшей маршрутизации. 

## Приложение:

Наш сайт необходимо поместить в Docker контейнер (для этого нужно использовать nginx в качестве веб-сервера внутри самого контейнера) поскольку позже он будет запускаться через Docker. 

## CI/CD:

Создание автоматизированного пайплайна по сборке и деплою данного приложения в инфраструктуру, которую ранее создали. Для этого желательно использовать GitLab CI/CD, так как оно предоставляет все необходимые для этого задания возможности бесплатно.


Для хранения Docker image с сайтом можно использовать AWS ECR (для доступа к ECR твоему серверу нужно дать необходимые права).


## Схема итоговой инфраструктуры:

https://faint-adasaurus-4bc.notion.site/image/https%3A%2F%2Fs3-us-west-2.amazonaws.com%2Fsecure.notion-static.com%2F3b90dfff-afae-436c-86f7-df1f805f2f7c%2FUntitled.png?table=block&id=95e3686b-202d-44a8-bb5c-ff7f4f36d775&spaceId=56b261ac-032c-4a60-9a87-b00f64f920b2&width=2000&userId=&cache=v2
