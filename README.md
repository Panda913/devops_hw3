# devops_hw3


1)створення образу 

docker build . -t node-js-app 

node-js-app -назва node.js застосунку

2)запускання контейнеру з обмеженнями по cpu та memory. Node.js app має бути доступним на 80 порті.

docker run -d -p 8098:80 --memory="400m" --cpus="1" --name app node-js-app

зовнішній порт - 8098

назва контейнеру - app

3)Пушіння в публічний репозиторій

docker login

docker tag node-js-app yuliia1999/app

docker push yuliia1999/app
