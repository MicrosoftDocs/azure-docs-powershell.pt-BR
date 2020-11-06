---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: f3afbd9b96de51f754dd87dfa42ed6f71e5b3577
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "93425484"
---
# Save-AzureRmContext

## Sinopse
Salva as informações de autenticação atuais para usar em outras sessões do PowerShell.

## SYNTAX

```
Save-AzureRmContext [[-Profile] <AzureRmProfile>] [-Path] <String> [-Force] [-WhatIf] [-Confirm]
```

## DESCRITIVO
O cmdlet Save-AzureRmContext salva as informações de autenticação atuais para uso em outras sessões do PowerShell.

## EXEMPLOS

### Exemplo 1: salvando o contexto da sessão atual
```
PS C:\> Add-AzureRmAccount
PS C:\> Save-AzureRmContext -Path C:\test.json
```

Este exemplo salva o contexto do Azure da sessão atual no arquivo JSON fornecido.

### Exemplo 2: salvando um determinado contexto
```
PS C:\> Save-AzureRmContext -Profile (Add-AzureRmAccount) -Path C:\test.json
```

Este exemplo salva o contexto do Azure que é passado para o cmdlet para o arquivo JSON fornecido.

## OS

### -Force
Substituir o arquivo fornecido se ele existir

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Caminho
Especifica o caminho do arquivo no qual as informações de autenticação são salvas.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Perfil
Especifica o contexto do Azure do qual este cmdlet lê.
Se você não especificar um contexto, esse cmdlet lerá do contexto padrão local.

```yaml
Type: AzureRmProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Confirme
Solicita confirmação antes de executar o cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra o que aconteceria se o cmdlet fosse executado.
O cmdlet não é executado.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

## SENSORES

### Microsoft. Azure. Commands. Common. Authentication. Models. AzureRMProfile

## EXIBE

### Microsoft. Azure. Commands. Profile. Models. PSAzureProfile

## INFORMA

## LINKS RELACIONADOS

