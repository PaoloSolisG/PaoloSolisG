<div align="center">

<img src="brain.svg" alt="Paolo Solis — Neural Architecture" width="100%" />

<br/>

<a href="https://paolosolisg.github.io/paolosolisg/">
  <img src="https://img.shields.io/badge/%E2%97%89%20ENTRAR%20AL%20CEREBRO%20INTERACTIVO-00f5d4?style=for-the-badge&labelColor=0d1117&color=0e4f8b" alt="Cerebro interactivo" />
</a>

<br/><br/>

<a href="https://git.io/typing-svg">
  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=700&size=20&duration=3000&pause=900&color=00F5D4&center=true&vCenter=true&width=820&height=45&lines=Arquitectura+desacoplada+%7C+Microservicios+%7C+Event-Driven;Dise%C3%B1o+servidores+que+escalan+y+no+se+caen;Del+diagrama+a+producci%C3%B3n.+Sin+excusas." alt="typing" />
</a>

</div>

---

## `> boot paolo.sys`

<div align="center">
  <img src="terminal.svg" alt="Boot log" width="100%" />
</div>

---

## 🏗️ Cómo pienso la arquitectura

```mermaid
flowchart LR
    C([Clientes<br/>Web · Mobile · API]) --> E[Edge<br/>CDN · WAF · Nginx]
    E --> G{API Gateway<br/>Auth · Rate limit · Routing}

    G --> S1[Servicio<br/>Identidad]
    G --> S2[Servicio<br/>Facturación]
    G --> S3[Servicio<br/>Inventario]
    G --> S4[Servicio<br/>Notificaciones]

    S1 --> B[[Message Broker<br/>Colas · Eventos]]
    S2 --> B
    S3 --> B
    S4 --> B

    S1 --- D1[(PostgreSQL)]
    S2 --- D2[(MySQL)]
    S3 --- D3[(PostgreSQL)]
    S4 --- D4[(Redis)]

    B --> W[Workers<br/>Jobs · Procesos async]

    classDef core fill:#0e4f8b,stroke:#00f5d4,color:#fff;
    classDef data fill:#0d1117,stroke:#00f5d4,color:#00f5d4;
    class S1,S2,S3,S4,G,E,W core;
    class D1,D2,D3,D4,B data;
```

| Principio | En la práctica |
| --- | --- |
| 🔌 **Desacoplamiento** | Cada servicio con su dominio, su base de datos y su ciclo de despliegue |
| 📨 **Event-driven** | Comunicación asíncrona por eventos; los servicios no se esperan entre sí |
| 🧱 **Clean / Hexagonal** | El dominio no depende del framework, de la base de datos ni de la UI |
| 🏢 **Multi-tenant** | Aislamiento por empresa y sucursal, pensado desde el día uno |
| 🔁 **Resiliencia** | Reintentos, colas, idempotencia y fallos que no se propagan en cascada |
| 📈 **Escalabilidad** | Escalado horizontal, caché por capas y cuellos de botella medidos |

---

## 🖥️ Arquitectura de servidores

```text
┌──────────────────────────────────────────────────────────────┐
│  INTERNET                                                    │
│     │                                                        │
│  [ DNS · CDN · WAF ]                                         │
│     │                                                        │
│  [ Reverse Proxy · Nginx / Nginx Proxy Manager · SSL ]       │
│     │                                                        │
│  ┌──┴─────────────── VPS / Linux ──────────────────────┐     │
│  │  Docker · Compose · Redes aisladas                  │     │
│  │  ├─ app containers   (PHP-FPM · Node · .NET · JVM)  │     │
│  │  ├─ workers & queues (supervisor · schedulers)      │     │
│  │  ├─ databases        (MySQL · PostgreSQL · Redis)   │     │
│  │  └─ observabilidad   (logs · métricas · alertas)    │     │
│  └─────────────────────────────────────────────────────┘     │
│     │                                                        │
│  [ Backups automáticos · Hardening · Firewall · Fail2ban ]   │
└──────────────────────────────────────────────────────────────┘
```

---

## ⚔️ Arsenal

<div align="center">

<img src="https://skillicons.dev/icons?i=java,cs,cpp,php,ts,js,py&theme=dark" alt="languages" /><br/>
<img src="https://skillicons.dev/icons?i=dotnet,laravel,nodejs,fastify&theme=dark" alt="backend" /><br/>
<img src="https://skillicons.dev/icons?i=vue,tailwind,html,css,vite&theme=dark" alt="frontend" /><br/>
<img src="https://skillicons.dev/icons?i=postgres,mysql,redis&theme=dark" alt="data" /><br/>
<img src="https://skillicons.dev/icons?i=linux,docker,nginx,git,github,githubactions&theme=dark" alt="devops" />

</div>

---

## 🚀 Ecosistema Naniva

| Producto | Descripción |
| --- | --- |
| 🏢 **Naniva ERP** | ERP multiempresa y multisucursal para pymes peruanas |
| 🧾 **API de Facturación Electrónica** | Comprobantes SUNAT (UBL 2.1) como servicio independiente |
| 💬 **WhatsApp CRM** | Atención y seguimiento de clientes por WhatsApp |
| 🍽️ **Restaurantes** | Pedidos, mesas, cocina y caja en un solo sistema |

🌐 **[naniva.pe](https://naniva.pe)**

---

## 📊 Métricas

<div align="center">

<img height="175" src="https://github-readme-stats.vercel.app/api?username=paolosolisg&show_icons=true&theme=radical&hide_border=true&bg_color=0d1117&count_private=true" alt="stats" />
<img height="175" src="https://github-readme-stats.vercel.app/api/top-langs/?username=paolosolisg&layout=compact&theme=radical&hide_border=true&bg_color=0d1117" alt="langs" />

<img src="https://streak-stats.demolab.com?user=paolosolisg&theme=radical&hide_border=true&background=0d1117" alt="streak" />

</div>

---

## 📡 Contacto

<div align="center">

[![Web](https://img.shields.io/badge/WEB-naniva.pe-00f5d4?style=for-the-badge&logo=googlechrome&logoColor=0d1117&labelColor=0d1117)](https://naniva.pe)
[![GitHub](https://img.shields.io/badge/GITHUB-paolosolisg-0e4f8b?style=for-the-badge&logo=github&logoColor=white&labelColor=0d1117)](https://github.com/paolosolisg)
<!-- Descomenta y completa los que uses:
[![LinkedIn](https://img.shields.io/badge/LINKEDIN-conectar-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white&labelColor=0d1117)](https://linkedin.com/in/TU-USUARIO)
[![Email](https://img.shields.io/badge/EMAIL-escribeme-D14836?style=for-the-badge&logo=gmail&logoColor=white&labelColor=0d1117)](mailto:TU-CORREO)
[![WhatsApp](https://img.shields.io/badge/WHATSAPP-hablemos-25D366?style=for-the-badge&logo=whatsapp&logoColor=white&labelColor=0d1117)](https://wa.me/51TU-NUMERO)
-->

</div>
