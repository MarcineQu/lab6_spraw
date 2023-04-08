Do zbudowania użyłem komendy:
buildctl build --frontend=dockerfile.v0 --local context=. --local dockerfile=. --export-cache type=inline --output type=image,name=docker.io/marcinequ/lab:lab6v2,push=true
![Zrzut ekranu 2023-04-08 141741](https://user-images.githubusercontent.com/83167368/230720722-74eca795-b61a-4d6b-9446-4c7431abffa1.png)

Następnie wyczyściłem cache:
buildctl prune
![Zrzut ekranu 2023-04-08 142144](https://user-images.githubusercontent.com/83167368/230720767-0ad6f427-9e67-46ab-9d60-068cfb4b59b9.png)

Następnie do kolejnego etapu użyłem komendy:
buildctl build \
  --frontend=dockerfile.v0 \
  --local context=. \
  --local dockerfile=. \
  --export-cache type=inline \
  --import-cache type=registry,ref=docker.io/marcinequ/lab:lab6v2 \
  --output type=image,name=docker.io/marcinequ/lab:lab6v2,push=true
![image](https://user-images.githubusercontent.com/83167368/230720868-74b55c0e-debf-41c9-bad4-2d1eefaf2e55.png)
