# Arquitetura

Esse projeto será construído com base na arquitetura [cliente-servidor](https://pt.wikipedia.org/wiki/Modelo_cliente%E2%80%93servidor). Onde haverá uma aplicação que atuará como [servidor de requisições](https://github.com/maxandriani/booking-app-server) e manterá a atomicidade dos dados de locações. A responsabilidade pelo acesso aos dados e apresentação ao usuário cairá sobre as aplicações clientes, sendo elas [booking-app-web](https://github.com/maxandriani/booking-app-web) e [booking-app-ios](https://github.com/maxandriani/booking-app-ios).

* [Server](./arquitetura/server.md)
* [Web](./arquitetura/web.md)
* [Ios](./arquitetura/ios.md)

::: mermaid

flowchart TB

srv[BookingApp.Server]
web[BookingApp.Web]
ios[BookingApp.Ios]
db[Database]

web --> srv
ios --> srv
srv --> db

:::

---
[Índice](../Readme.md)
