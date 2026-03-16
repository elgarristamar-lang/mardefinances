# 💳 Analizador de Gastos BBVA

Analiza tus extractos BBVA ("Últims moviments") y clasifica tus gastos por categoría usando IA.

## Características

- **Dos cuentas**: sube el extracto de cuenta corriente y cuenta ahorro/nómina por separado
- **Clasificación automática**: palabras clave + Claude AI para casos ambiguos
- **Aprende preguntando**: si no sabe dónde clasificar algo, te pregunta
- **Resumen mensual**: filtra por mes, ve gastos por categoría, ingresos y ahorro
- **Corrige categorías**: haz clic en cualquier badge para reclasificar

## Deploy en Vercel (5 minutos)

### Opción A — Sin código (interfaz web)

1. Crea cuenta en [vercel.com](https://vercel.com) si no tienes
2. Sube este repositorio a GitHub
3. En Vercel: **New Project** → importa el repo → **Deploy**
4. ¡Listo! Vercel detecta automáticamente que es HTML estático

### Opción B — Con Vercel CLI

```bash
npm i -g vercel
cd expense-tracker
vercel
```

### Opción C — Drag & Drop

Ve a [vercel.com/new](https://vercel.com/new) y arrastra la carpeta `expense-tracker` directamente.

## Uso

1. Abre la app
2. Arrastra tu extracto de **cuenta corriente** (gastos con tarjeta, bizum, etc.)
3. Arrastra tu extracto de **cuenta ahorro / nómina** (opcional)
4. Introduce tu [clave API de Anthropic](https://console.anthropic.com/settings/keys) para clasificación con IA
5. Pulsa **Analizar gastos**

> La clave API solo se usa en tu navegador y nunca se envía a ningún servidor externo.

## Estructura

```
expense-tracker/
├── index.html    ← app completa (HTML + CSS + JS en un fichero)
├── vercel.json   ← configuración Vercel
└── README.md
```

## Privacidad

- Todo se procesa en el navegador
- Los archivos XLSX nunca salen de tu dispositivo
- La clave API solo se usa para las llamadas a Anthropic directamente desde tu navegador
