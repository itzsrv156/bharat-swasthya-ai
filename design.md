# Design — BharatSwasthyaAI 

## High-level flow
Client (Android PWA) -> API Gateway (Cognito auth) -> Lambda ingest -> S3 (audio) -> Transcribe Medical -> Transcript -> Bedrock (RAG + prompts) -> Structured JSON -> DynamoDB -> SageMaker risk scoring -> Notifications/TTS -> Client

## Key AWS services
- Amazon Transcribe Medical (ASR)
- Amazon Bedrock (LLM orchestration)
- Amazon SageMaker (train risk models)
- S3 (audio & artifacts), DynamoDB (records)
- API Gateway, Lambda, Cognito, CloudWatch

## RAG & knowledge
- Embeddings + OpenSearch/Kendra for local guidelines
- Bedrock synthesizes SOAP notes using retrieved passages for auditability

## Offline & low-bandwidth
- Client encrypts & caches audio, resumes uploads, simple local threshold alerts.

## Security
- Encryption in transit & at rest, IAM roles, CloudTrail logging, BAA before PHI processing.

## Demo plan
- 3 demo audio recordings (EN, HI, KN) -> show transcript, SOAP note, one risk flag, and patient TTS audio.
