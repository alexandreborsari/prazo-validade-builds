# Prazo & Validade — builds de teste

Aqui ficam apenas os APKs de teste do **Prazo & Validade**. O código-fonte continua no
repositório privado: https://github.com/alexandreborsari/prazo-validade

## Como instalar

1. Abra a [última release](../../releases/latest) e baixe o arquivo
   `prazo-validade-<versao>-<versionCode>.apk`.
2. No celular, abra o arquivo baixado. Quando o Android perguntar, permita a origem usada
   (navegador, Gmail, app de arquivos etc.) em **Instalar apps desconhecidos**.
3. Toque em **Instalar**. O app aparece na gaveta como **Prazo & Validade**.

Requisito: Android 8.0 (API 26) ou superior. O AAB não é instalável; use somente os APKs
desta página.

## Conferindo o arquivo

Cada release traz um arquivo `.sha256`. No Windows:

```powershell
Get-FileHash ".\prazo-validade-0.14.0-21.apk" -Algorithm SHA256
```

O resultado deve ser igual ao conteúdo do `.sha256` publicado na release.

## Dados e atualizações

- O APK é assinado com a chave definitiva do app (a mesma usada no AAB da Play).
  Portanto, instalar uma versão nova preserva os itens da sua despensa.
- O pacote é `com.prazovalidade`. O build de depuração usa `com.prazovalidade.debug`
  e pode conviver com este no mesmo aparelho.
- Política de privacidade: https://alexandreborsari.github.io/prazo-validade-privacy/

## Como uma nova versão é publicada

No repositório privado, `.\gradlew.bat prepareGithubRelease` copia o APK assinado para
`dist\` com nome versionado e gera o `.sha256`. Em seguida, os dois arquivos são anexados
a uma nova release aqui.
