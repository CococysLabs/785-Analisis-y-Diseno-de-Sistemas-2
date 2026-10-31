# Análisis y Diseño de Sistemas 2 — Material de clase

[![TypeScript](https://img.shields.io/badge/TypeScript-5.x-3178C6?logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Node.js](https://img.shields.io/badge/Node.js-18%2B-339933?logo=node.js&logoColor=white)](https://nodejs.org/)

Presentaciones, guiones y ejemplos ejecutables del curso, organizados por semana. Cada carpeta `Semana_NN-Tema/` tiene su propio README con el material de esa clase.

## Semanas

| Semana | Tema | Qué incluye |
| --- | --- | --- |
| [02](./Semana_02-Fundamentos-SOLID/) | Fundamentos y principios SOLID | PDF, guion de video, 6 ejemplos en TypeScript |
| [03](./Semana_03-Patrones-Creacionales/) | Patrones creacionales | PDF, guion de video, 5 ejemplos en TypeScript |
| [04](./Semana_04-Patrones-Estructurales/) | Patrones estructurales | PDF, 6 ejemplos en TypeScript |
| [05](./Semana_05-Patrones-Comportamiento/) | Patrones de comportamiento | PDF, 5 ejemplos en TypeScript |
| [06](./Semana_06-Elementos-Diseno/) | Elementos de diseño (UX/UI) | PDF, PPTX, demo interactiva en HTML |
| [07](./Semana_07-Patrones-Arquitectura/) | Patrones de arquitectura | PPTX |
| [08](./Semana_08-Pruebas-Software/) | Pruebas de software y TDD | PPTX, ejercicio y API con Jest |
| [09](./Semana_09-Seguridad/) | Seguridad de sistemas | Guion, API en NestJS vulnerable vs. segura |
| [10](./Semana_10-Pruebas-No-Funcionales/) | Pruebas no funcionales | PDF, guion, scripts de carga con k6 |
| [11](./Semana_11-Cloud-PaaS/) | Cloud I: PaaS con Vercel | PPTX, guion, Docker y despliegue |
| [12](./Semana_12-Cloud-IaC/) | Cloud II: Terraform y Ansible | PPTX, guion, IaC en Azure |

## Estructura

```text
Semana_NN-Tema/
├── README.md        # punto de entrada de la semana
├── *.pdf | *.pptx   # presentación
├── Guion_*.md       # guion docente (cuando existe)
├── video/           # guion y scripts del video (semanas 02 y 03)
└── codigo/          # ejemplos o proyecto de la clase
```

## Ejecutar un ejemplo de patrones (semanas 02 a 05)

Cada archivo `.ts` exporta una función `demo...()`. El README de cada semana dice cuál es. Basta Node.js 18 o superior:

```bash
cd Semana_03-Patrones-Creacionales/codigo
npx tsx -e "import('./singleton.ts').then(m => m.demoSingleton())"
```

Los proyectos de las semanas 08 en adelante tienen su propio `package.json` e instrucciones en su README.

## Cómo estudiar un ejemplo

1. **Problema:** ¿qué cambio, dependencia o colaboración resulta difícil?
2. **Patrón o principio:** ¿qué estructura propone el ejemplo?
3. **Razón:** ¿qué responsabilidad o variación queda aislada?
4. **Riesgo:** ¿qué complejidad, costo o abuso puede introducir la solución?

Después, modifica el escenario de la función `demo...` y vuelve a ejecutarla. Los ejemplos son pequeños a propósito, para que las relaciones entre clases se vean sin el ruido de una aplicación completa.

> Refactoring.Guru puede servir como referencia conceptual para estudiar patrones. Los escenarios y el código de este repositorio están escritos para la clase y no son una copia literal de su contenido.
