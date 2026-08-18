# ❄️ **TIDS JSON Schema — Snowflake Domain v1.0**  
### *NDH‑TIDS • Comparative Geometry Schema Documentation*  
### *Altitude: A4 — Comparative Geometry • Non‑Operational*

---

## ⭐ **0 — Schema Identity**

```
Schema: TIDS-JSON-Schema-SnowflakeDomain
Version: v1.0
Altitude: A4 — Comparative Geometry
Lane: NDH-TIDS • Schema Documentation
Status: Canonical, Non-Operational
```

---

## ⭐ **1 — Schema Overview**

This schema defines the **machine‑readable structure** TIDS expects when ingesting the Snowflake Diagnostic Substrate.  
It documents:

- required fields  
- allowed values  
- invariant boundaries  
- membrane flags  
- drift signature arrays  
- stability envelope objects  
- anchor lattice definitions  

This schema is **documented in Markdown**, but represents the internal JSON structure TIDS uses.

---

## ⭐ **2 — JSON Schema (Documented in Markdown)**

```
{
  "title": "Snowflake Domain — TIDS Ingestion Schema v1.0",
  "type": "object",

  "required": [
    "anchors",
    "layers",
    "invariants",
    "membranes",
    "drift_signatures",
    "stability_envelopes",
    "ingestion_constraints"
  ],

  "properties": {

    "anchors": {
      "type": "object",
      "properties": {
        "structural": { "type": "string", "enum": ["crystallography"] },
        "environmental": { "type": "string", "enum": ["atmospheric_microphysics"] },
        "geometric": { "type": "string", "enum": ["fractal_geometry"] },
        "dynamical": { "type": "string", "enum": ["particle_drift_modeling"] },
        "probabilistic": { "type": "string", "enum": ["environmental_stochastic_modeling"] },
        "categorical": { "type": "string", "enum": ["snowflake_classification_systems"] }
      },
      "required": [
        "structural",
        "environmental",
        "geometric",
        "dynamical",
        "probabilistic",
        "categorical"
      ]
    },

    "layers": {
      "type": "array",
      "items": {
        "type": "string",
        "enum": [
          "structural",
          "environmental",
          "dynamical",
          "hazard",
          "stability",
          "temporal"
        ]
      }
    },

    "invariants": {
      "type": "object",
      "properties": {
        "structural": { "type": "array", "items": { "type": "string" } },
        "environmental": { "type": "array", "items": { "type": "string" } },
        "dynamical": { "type": "array", "items": { "type": "string" } },
        "categorical": { "type": "array", "items": { "type": "string" } },
        "harmony": { "type": "array", "items": { "type": "string" } }
      }
    },

    "membranes": {
      "type": "object",
      "properties": {
        "clarity": { "type": "string", "enum": ["active"] },
        "diagnostic": { "type": "string", "enum": ["active"] },
        "comparative": { "type": "string", "enum": ["active"] },
        "governance": { "type": "string", "enum": ["active"] }
      }
    },

    "drift_signatures": {
      "type": "object",
      "properties": {
        "structural": { "type": "array", "items": { "type": "string" } },
        "environmental": { "type": "array", "items": { "type": "string" } },
        "dynamical": { "type": "array", "items": { "type": "string" } },
        "representational": { "type": "array", "items": { "type": "string" } }
      }
    },

    "stability_envelopes": {
      "type": "object",
      "properties": {
        "structural": { "type": "array", "items": { "type": "string" } },
        "environmental": { "type": "array", "items": { "type": "string" } },
        "dynamical": { "type": "array", "items": { "type": "string" } },
        "hazard": { "type": "array", "items": { "type": "string" } }
      }
    },

    "ingestion_constraints": {
      "type": "object",
      "properties": {
        "allowed_layers": {
          "type": "array",
          "items": { "type": "string" }
        },
        "forbidden": {
          "type": "array",
          "items": { "type": "string" }
        }
      }
    }
  }
}
```

---

## ⭐ **3 — Schema Notes (RP → TIDS Compliance)**

- Harmony is **never** an operand.  
- NDH geometry is **excluded**.  
- Membranes are **documented**, not activated.  
- Altitude routing is **forbidden**.  
- SID primitives are **forbidden**.  
- All drift signatures must be **stabilized at RP altitude** before ingestion.  
- All anchors must match the **scientific lattice** defined in the substrate.

This schema is **non‑operational** and **non‑activating**.

---

