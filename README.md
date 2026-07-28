# somosum-updates

Canal **público** de atualizações delta do [SOMOSUM](https://github.com/RabbitVisual/SOMOSUM) — sem código-fonte.

## Estrutura

```
channel/
  latest.json       # versão alvo + URL do pacote delta
  notes/X.Y.Z.md    # notas da versão
```

ZIPs delta: GitHub Release `app-X.Y.Z` → `update-X.Y.Z.zip`

## App

O SOMOSUM verifica `latest.json` (jsDelivr). Se `version` > versão local, o operador pode optar por atualizar.

Dados da igreja (`model/data`) **nunca** entram no pacote.

## Publicar (repo privado SOMOSUM)

```powershell
node scripts/build-app-update.mjs
.\scripts\publish-app-update.ps1
```
