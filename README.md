# Customização de mapas no Android com Google Maps API.

Este aplicativo tem como intuito servir como uma demonstração do uso de custom maps usando Google Maps API e Google Styling Wizard?

## Como rodar o projeto e testar?

**1** -  Não se esqueça de colocar a SUA chave da Google Maps API. Ele fica dentro do AndroidManifest.xml

>Crie a api no Google Developers Console,esta é uma chave única, tome cuidado, pois o Google cobra por requisição depois de um certo número excedido.

**2** - Sete as suas coordenadas na variável como o exêmplo abaixo no arquivo:

```
LatLng cascavel = new LatLng(-24.952327, -53.461767);
```

E depois lembre-se de setar o estilo vindo da pasta raw como no código abaixo:

```
try {
 boolean success = googleMap.setMapStyle(
       MapStyleOptions.loadRawResourceStyle(this, R.raw.cascavel_style));
           if (!success) {
               Log.e(TAG, "Falhou ao aplicar estilo.");
           }
       } catch (Resources.NotFoundException e) {
     Log.e(TAG, "Estilo não encontrado. Error: ", e);
 }
 ```
 
 **3** - Se você quiser pode acessar o [Google Style Wizard](https://mapstyle.withgoogle.com/) e criar o seu próprio estilo.
 
 **4** - [Link da palestra no SpeakerDeck](https://speakerdeck.com/wmitrut)
