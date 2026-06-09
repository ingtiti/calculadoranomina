# 🧾 NóminaMX — Calculadora de Nómina CDMX 2024

> Calculadora de nómina completa para **Ciudad de México**, desarrollada conforme a la legislación vigente 2024.  
> ISR · IMSS · INFONAVIT · Impuesto sobre Nóminas CDMX · Prestaciones LFT

[![Deploy to GitHub Pages](https://github.com/tu-usuario/nomina-cdmx/actions/workflows/deploy.yml/badge.svg)](https://github.com/tu-usuario/nomina-cdmx/actions/workflows/deploy.yml)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](#licencia)

---

## 🚀 Demo en vivo

👉 **[https://tu-usuario.github.io/nomina-cdmx](https://tu-usuario.github.io/nomina-cdmx)**

> Reemplaza `tu-usuario` con tu nombre de usuario de GitHub después del deploy.

---

## 📋 ¿Qué calcula?

### Retenciones del empleado
| Concepto | Base | Artículo |
|---|---|---|
| IMSS Enf. y Maternidad | 0.375% del SBC | LSS Art. 106-I |
| IMSS Invalidez y Vida | 0.625% del SBC | LSS Art. 147 |
| IMSS Cesantía y Vejez | 1.125% del SBC | LSS Art. 168 |
| ISR (tarifa mensual) | Base gravable | LISR Art. 96 |
| Subsidio al empleo | Tabla SAT | LISR Art. 97 |

### Cuotas patronales
| Concepto | Tasa | Artículo |
|---|---|---|
| IMSS Enf. Mat. Cuota Fija | 20.40% × UMA × 30d | LSS Art. 106-I |
| IMSS Enf. Mat. Excedente | 1.10% sobre excedente 3 SMG | LSS Art. 106-I |
| IMSS Maternidad | 0.70% SBC | LSS Art. 106-II |
| IMSS Invalidez y Vida | 1.75% SBC | LSS Art. 147 |
| IMSS Riesgos de Trabajo | 0.543% SBC (Clase I) | LSS Art. 73 |
| IMSS Guarderías | 1.00% SBC | LSS Art. 211 |
| SAR / Retiro | 2.00% SBC | LSS Art. 168 |
| IMSS Cesantía y Vejez | 3.15% SBC | LSS Art. 168 |
| INFONAVIT | 5.00% SBC | Ley INFONAVIT Art. 29-II |
| Impuesto Nóminas CDMX | 3.00% sobre nómina bruta | Ley Hacienda CDMX Art. 178 |

### Prestaciones de Ley (LFT)
- **Aguinaldo**: 15 días mínimo (Art. 87)
- **Vacaciones**: Según antigüedad, reforma Feb-2023 (Art. 76)
  - 1 año: 12 días | 2 años: 14 | 3: 16 | 4: 18 | 5: 20 …
- **Prima Vacacional**: 25% sobre días de vacaciones (Art. 80)
- **Factor de Integración**: Proporcional aguinaldo + vacaciones + prima
- **Tope cotización IMSS/INFONAVIT**: 25 UMAs diarias

---

## 📐 Parámetros 2024

| Indicador | Valor | Fuente |
|---|---|---|
| UMA diaria | $108.57 | DOF 10-Ene-2024 |
| SMG Ciudad de México | $278.80 | DOF 01-Ene-2024 |
| Tope cotización | 25 UMAs = $2,714.25/día | IMSS |
| ISR — Tarifa mensual | Tabla Art. 96 LISR | SAT 2024 |
| Subsidio al empleo | Tabla Art. 97 LISR | SAT 2024 |
| Impuesto sobre Nóminas CDMX | 3% | Ley Hacienda CDMX 2024 |

---

## 🗂 Estructura del repositorio

```
nomina-cdmx/
├── index.html              # Aplicación completa (standalone, sin dependencias)
├── README.md               # Este archivo
├── LICENSE                 # Licencia MIT
└── .github/
    └── workflows/
        └── deploy.yml      # Auto-deploy a GitHub Pages
```

---

## 🛠 Cómo hacer el deploy

### Opción A — GitHub Pages (recomendado, gratis)

1. **Crea el repositorio** en [github.com/new](https://github.com/new)
   - Nombre sugerido: `nomina-cdmx`
   - Visibilidad: Public (necesario para GitHub Pages gratis)

2. **Sube los archivos**

   ```bash
   git init
   git add .
   git commit -m "feat: calculadora de nómina CDMX 2024"
   git branch -M main
   git remote add origin https://github.com/TU-USUARIO/nomina-cdmx.git
   git push -u origin main
   ```

3. **Activa GitHub Pages**
   - Ve a tu repo → **Settings** → **Pages**
   - En *Source* selecciona: **GitHub Actions**
   - Guarda los cambios

4. **¡Listo!** El workflow `.github/workflows/deploy.yml` se ejecuta automáticamente.
   Tu app estará en: `https://TU-USUARIO.github.io/nomina-cdmx`

### Opción B — Netlify (arrastrar y soltar)

1. Ve a [netlify.com/drop](https://app.netlify.com/drop)
2. Arrastra la carpeta `nomina-cdmx/`
3. Netlify genera una URL pública en segundos

### Opción C — Local (sin servidor)

Simplemente abre `index.html` en tu navegador. No requiere servidor, build ni dependencias.

---

## 🖥 Características de la app

- ✅ **100% standalone** — un solo archivo HTML, sin npm, sin build
- ✅ **Sin dependencias externas de datos** — todos los cálculos son locales
- ✅ **Responsive** — funciona en móvil y desktop
- ✅ **4 períodos de pago** — mensual, quincenal, semanal, diario
- ✅ **Jornada completa o parcial (50%)**
- ✅ **Vacaciones dinámicas** según años de antigüedad (reforma 2023)
- ✅ **Copiar resumen** al portapapeles
- ✅ **Imprimir / guardar PDF** (Ctrl+P)
- ✅ **Dark theme** profesional

---

## ⚠️ Aviso legal

> Los resultados de esta calculadora tienen **fines informativos y de referencia**.  
> Los cálculos reales de nómina pueden variar según:
> - Prima de riesgo de trabajo específica de la empresa (IMSS)
> - Beneficios adicionales por contrato colectivo o individual
> - Situación fiscal particular del trabajador
> - Actualizaciones de tasas y tarifas del DOF
>
> **Siempre verifica con tu contador certificado (C.P.) o área de Recursos Humanos.**

---

## 📄 Licencia

MIT © 2024 — [TiTi-Apps](https://titi-apps.com)

Libre para uso personal y comercial con atribución.

---

## 🤝 Contribuciones

¿Encontraste un error en los cálculos o las tasas? Abre un **Issue** o un **Pull Request**.

Áreas de mejora bienvenidas:
- Actualización automática de UMA/SMG vía API DOF
- Exportar a Excel / PDF
- Soporte para múltiples empleados
- Cálculo de PTU (Participación de Utilidades)
- Horas extras y cálculo de prima dominical

---

*Desarrollado con ❤️ por [TiTi-Apps](https://titi-apps.com) — Transformación Digital para PyMEs mexicanas*
