# lab6_spraw
Do zbudowania obrazu użyłem komendy:
buildctl build --frontend=dockerfile.v0 --local context=. --local dockerfile=. --output type=image,name=docker.io/marcinequ/lab:lab6,push=true 
![Zrzut ekranu 2023-04-08 132731](https://user-images.githubusercontent.com/83167368/230718671-8cbd1630-8f9e-452e-aad7-deb77bbaad10.png)

Następnie uruchomiłem obraz komendą:
lab6# docker run -it docker.io/marcinequ/lab:lab6
![Zrzut ekranu 2023-04-08 132927](https://user-images.githubusercontent.com/83167368/230718729-6871bb36-e445-4a8d-9c54-07d8c9b8376f.png)
