```
+------------------------------------------------------------------+
|                                                                  |
|                     N O R T H L I N E   R D                      |
|                                                                  |
|         Mensajeria  ·  Paqueteria  ·  Logistica Nacional         |
|                                                                  |
|  Santo Domingo · Santiago · La Romana · Puerto Plata · Barahona  |
|                                                                  |
+------------------------------------------------------------------+
```

<p align="center"><strong>PNETLAB</strong> · <strong>OSPF Multiárea</strong> · <strong>ITLA</strong> · <strong>Empresa 3</strong> · <em>En progreso</em></p>

<h1 align="center">Northline RD</h1>
<p align="center"><em>Proyecto Final — Conmutación y Enrutamiento · Instituto Tecnológico de las Américas (ITLA)</em></p>

---

## Tabla de contenidos

- [Quiénes somos](#quiénes-somos)
- [Misión, Visión y Valores](#misión-visión-y-valores)
- [Equipo de trabajo](#equipo-de-trabajo)
- [Sobre el proyecto](#sobre-el-proyecto)
- [Cobertura y sedes](#cobertura-y-sedes)
- [Estructura del repositorio](#estructura-del-repositorio)
- [Entrega](#entrega)
- [Créditos](#créditos)

---

## Quiénes somos

**Northline RD** es una empresa de capital dominicano dedicada a la mensajería, paquetería y logística a nivel nacional. Con presencia en Santo Domingo y sucursales en las principales ciudades del país, ofrecemos soluciones confiables de envío y distribución respaldadas por infraestructura tecnológica de comunicaciones unificadas.

Este repositorio documenta el diseño e implementación de dicha infraestructura de red, desarrollado como propuesta técnica para Northline RD por **CECOMPE (Centro de Cómputos Pelegrino)**, e implementado en el emulador **PNETLAB** por el equipo técnico listado abajo.

## Misión, Visión y Valores

| | |
|---|---|
| **Misión** | Brindar servicios de mensajería, paquetería y logística confiables, seguros y eficientes, conectando a nuestros clientes con el resto del país mediante tecnología de punta y un equipo humano comprometido. |
| **Visión** | Ser la empresa de logística y paquetería líder en República Dominicana, reconocida por su innovación tecnológica, cobertura nacional y excelencia en el servicio al cliente. |

**Valores**

- 🤝 **Confiabilidad** — Cumplimos lo que prometemos, en cada entrega.
- 💡 **Innovación** — Adoptamos tecnología para mejorar cada proceso.
- 🔒 **Seguridad** — Protegemos la información y los envíos de nuestros clientes.
- 🎯 **Compromiso** — Con nuestros clientes, colaboradores y el país.
- 🌐 **Trabajo en Equipo** — Colaboración constante entre todas nuestras sedes.

## Equipo de trabajo

| Nombre | Rol | Perfil |
|---|---|---|
| Carlos Rodríguez | Gerente de Proyecto / Director Técnico | Lidera la planificación general del proyecto y las decisiones técnicas de arquitectura de red. |
| Yadiel Santana | Administrador de Servidores | Responsable del despliegue y mantenimiento de los servicios de DNS, DHCP, Web, NFS/RADIUS y correo. |
| Alexander Cotes | Ingeniero de Seguridad de Redes | A cargo del hardening de dispositivos, control de acceso, mitigación de ataques de VLAN, DHCP, ARP y STP. |
| Irving Pujols | Ingeniero de Redes (Switching & Routing) | Diseño de la conmutación, VLANs, redundancia de capa 2 y capa 3 entre sedes. |
| Josué Reyes | Ingeniero de Telecomunicaciones (WAN/VPN) | Implementación del enrutamiento OSPF multiárea y las VPN IPSec entre sucursales y la sede principal. |
| Nathanael Moris | Técnico de Soporte | Soporte de primer nivel, pruebas de conectividad y documentación de incidencias. |


## Sobre el proyecto

Northline RD contrató a **CECOMPE** para realizar el levantamiento de requerimientos y presentar una propuesta tecnológica de comunicaciones unificadas acorde a sus necesidades. El grupo de la asignatura **Conmutación y Enrutamiento** del ITLA, a cargo del profesor **Onel Luis Pelegrino**, fue elegido para implementar el diseño de CECOMPE en el emulador **PNETLAB** y documentar los resultados obtenidos.

La topología general contempla una sede central en Santo Domingo, un router de borde conectado a un ISP, un núcleo redundante (switches de core en anillo/EtherChannel), servidores de aplicación (Web, FTP/RADIUS, correo, DNS/Web/DHCP) y sucursales remotas conectadas vía WAN, cada una con su propio bloque de switches de acceso.

## Cobertura y sedes

| Sede | Rol | Departamentos / Requisitos |
|---|---|---|
| **Santo Domingo** | Sede central | 4 departamentos — Depto. 1 (110 hosts), Depto. 2 (51 hosts), Depto. 3 (64 hosts), Depto. 4 (80 hosts). Redundancia de capa 2 y capa 3 donde aplique. |
| **Santiago** | Sucursal | 3 departamentos — Centro de Datos (10 hosts), Ventas (15 hosts), Administración (5 hosts). Aloja los servicios de DNS, DHCP, Web, NFS/RADIUS y correo (ver abajo). |
| **La Romana** | Sucursal | 3 departamentos — Depto. 1 (25 hosts), Depto. 2 (52 hosts), Depto. 3 (7 hosts). Direccionamiento asignado de modo dinámico desde el router. |
| **Puerto Plata** | Sucursal | Diseño a disposición del grupo — el enunciado no detalla departamentos ni requisitos específicos para esta sede.|
| **Barahona** | Sucursal | Diseño a disposición del grupo — el enunciado no detalla departamentos ni requisitos específicos para esta sede. |

**Servicios a implementar en Santiago** (en un servidor dedicado):

- **DNS** — sufijo `northlinerd.com.do`
- **DHCP** — una VLAN/pool por departamento de la sede
- **Web** — `www.northlinerd.com.do`, sirviendo el contenido adjunto de la página de la empresa
- **NFS / RADIUS** — un usuario por integrante del grupo
- **Correo** — dominio `northlinerd.com.do`, una cuenta por integrante del grupo

## Estructura del repositorio

```
.
├── README.md
├── CONFIG-BACKUP/
├── DOCUMENTACION/
└── Topología/
```

## Entrega

- **Institución:** Instituto Tecnológico de las Américas (ITLA)
- **Asignatura:** Conmutación y Enrutamiento
- **Profesor:** Onel Luis Pelegrino

- **Fecha límite indicada:** 16/8/2026 — *sin prórroga*





## Créditos

- **Cliente (escenario del proyecto):** CECOMPE — Centro de Cómputos Pelegrino
- **Empresa implementada:** Northline RD
- **Emulador:** PNETLAB

---

<p align="center"><sub>Proyecto académico — ITLA · Conmutación y Enrutamiento · uso educativo.</sub></p>
