# openrouter-chat

Edge Function Supabase pour appeler OpenRouter sans exposer la cle API dans le navigateur.

## Secret requis

```bash
supabase secrets set OPENROUTER_API_KEY=sk-or-...
```

Optionnel :

```bash
supabase secrets set APP_PUBLIC_URL=https://patrickeudess.github.io/AfriData-Ready/
```

## Deploiement

```bash
supabase functions deploy openrouter-chat
```

## Test local

```bash
supabase functions serve openrouter-chat --env-file .env.local
```

Puis :

```bash
curl -i --location --request POST "http://127.0.0.1:54321/functions/v1/openrouter-chat" \
  --header "Content-Type: application/json" \
  --data "{\"prompt\":\"Explique AfriData Ready en une phrase.\"}"
```
