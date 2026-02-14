# Requirements — BharatSwasthyaAI

## Project overview
BharatSwasthyaAI captures clinician–patient conversations at Primary Health Centers (PHCs) and converts them to structured medical records, clinical summaries, and follow‑up instructions in regional languages (Kannada, Hindi, English). Optimized for low‑connectivity rural India.

## Goals
- Convert voice consultations → clinical notes (ASR → normalization → summary).
- Produce structured problem list, medications, vitals, ICD-10 tags.
- Provide regional language discharge/care instructions (audio + text).
- Flag high‑risk patients (diabetes, hypertension, pregnancy risks).
- Offline-first with opportunistic sync.
- Ensure data privacy and HIPAA-style controls.

## Users
- PHC doctors, ASHA workers, district health admins, patients.

## Key requirements
1. Real-time/batch transcription (medical ASR).
2. Clinical summary generation (SOAP).
3. Structured extraction (meds, diagnosis, vitals).
4. Risk scoring & alerts.
5. Regional TTS for patient instructions.
6. Offline caching & secure sync.

## Data & compliance
- Use synthetic/anonymized demo audio for submission.
- Architect with HIPAA-eligible AWS services; BAA required for PHI.
