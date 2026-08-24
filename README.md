# 🏛️ Sistema de Resoluciones Electorales CNE & Suite LegalTech Ecuador

> **Ficha Técnica, Arquitectura y Presentación del Proyecto Institucional**  
> *Desarrollado para el Consejo Nacional Electoral (CNE) y las Juntas Provinciales Electorales (JPE) de Ecuador.*

---

## 📸 Presentación Visual de la Aplicación

![Interfaz del Sistema](https://raw.githubusercontent.com/JaBarrerar/DocsAutomat-Showcase/main/img/app_preview.png)

---

## 🎯 Resumen Ejecutivo

Este ecosistema tecnológico automatiza y audita el ciclo completo de calificación de candidaturas electorales y técnica legislativa en Ecuador. Resuelve la complejidad operativa de las 24 delegaciones provinciales electorales mediante una arquitectura híbrida de **Privacidad Absoluta (Zero-Cloud / 100% On-Premise)**.

---

## ⚖️ Los 5 Escenarios Oficiales de Calificación (Código de la Democracia)

El motor jurídico modela estrictamente las causales constitucionales y jurisprudenciales:

```text
 1. 🟢 CALIFICACIÓN FAVORABLE TOTAL (Arts. 61, 97, 99 Código de la Democracia)
    • Verificación del 100% de requisitos, paridad de género y certificación de no objeción.

 2. ⏳ SUBSANACIÓN DE REQUISITOS FORMALES (Art. 101 ibídem)
    • Concesión del término perentorio de 48 horas con notificación del informe técnico.

 3. ⚖️ TRÁMITE DE OBJECIÓN Y CALIFICACIÓN
    • Resolución en dos tiempos: desestimación de objeción por Art. 113 CRE + calificación de la lista.

 4. ⛔ RECHAZO DIRECTO DE PLANO (Art. 105 Numerales 1 y 2)
    • Insubsanable por falta de elecciones primarias o paridad absoluta (SIN 48 horas).

 5. 🚫 RECHAZO DEFINITIVO POR PRECLUSIÓN (Art. 105 ibídem)
    • Extinción de la oportunidad procesal por fenecimiento del término de 48 horas sin subsanar.
```

---

## 🏗️ Arquitectura del Sistema

```text
┌─────────────────────────────────────────────────────────────────────────────┐
│ 1. CAPA DE PRESENTACIÓN (UI)                                                │
│    • CustomTkinter Desktop GUI + Concurrencia Desacoplada (Threading)       │
├─────────────────────────────────────────────────────────────────────────────┤
│ 2. MOTOR RAG JURÍDICO & BASE NORMATIVA                                      │
│    • Base de datos de la CRE, Código de la Democracia y Reglamentos CNE     │
├─────────────────────────────────────────────────────────────────────────────┤
│ 3. ASESOR JURÍDICO IA (Ollama LLM)                                          │
│    • Diseñador dinámico de plantillas en lenguaje natural ante reformas     │
├─────────────────────────────────────────────────────────────────────────────┤
│ 4. MOTOR OPENXML & BATCH PROCESSOR                                          │
│    • Inyector de campos nativos MERGEFIELD (<w:fldSimple>)                  │
│    • Procesamiento de 50 resoluciones Word (.docx) en 0.8 segundos          │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## 💻 Requisitos de Hardware para el Motor de IA (Ollama)

| Nivel de Equipo | Hardware Recomendado | Modelos LLM | Rendimiento |
| :--- | :--- | :--- | :--- |
| **Óptimo** | GPU NVIDIA RTX 3060/4060 (6-12GB VRAM) + 16-32GB RAM | `llama3.1:8b`, `qwen2.5:7b` | **Ultra Rápido** (2 a 4s por resolución) |
| **Medio** | CPU Intel i5 / Ryzen 5 + 16GB RAM (Sin GPU dedicada) | `qwen2.5:3b`, `llama3.2:3b` | **Fluido** (8 a 15s) |
| **Delegaciones** | PC Estándar con Microsoft Office (Word/Excel) | Kit de Correspondencia | **Instantáneo** (Sin instalar IA) |

---

## 👤 Autor

**Josué Barrera**  
*Ingeniero en Computación / Sistemas — Universidad Central del Ecuador (UCE)*  
*Especialista en Arquitectura de Software, LegalTech e Inteligencia Artificial Aplicada*  
🐙 **GitHub:** [@JaBarrerar](https://github.com/JaBarrerar)
