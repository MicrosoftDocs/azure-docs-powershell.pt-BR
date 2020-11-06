---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 06a78584437021df570bc5ff2b6ec19e332bffd8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425918"
---
# Save-AzureRmProfile

## Sinopse
Salva as informações de autenticação atuais para usar em outras sessões do PowerShell.

## SYNTAX

```
Save-AzureRmProfile [[-Profile] <AzureRMProfile>] [-Path] <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet Save-AzureRmProfile salva as informações de autenticação atuais para uso em outras sessões do PowerShell.

## EXEMPLOS

### Exemplo 1: salvando o perfil da sessão atual
```
PS C:\> Add-AzureRmAccount
PS C:\> Save-AzureRmProfile -Path C:\test.json
```

Este exemplo salva o perfil do Azure da sessão atual no arquivo JSON fornecido.

### Exemplo 2: salvando um determinado perfil
```
PS C:\> Save-AzureRmProfile -Profile (Add-AzureRmAccount) -Path C:\test.json
```

Este exemplo salva o perfil do Azure que é passado para o cmdlet para o arquivo JSON fornecido.

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
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Perfil
Especifica o perfil do Azure do qual este cmdlet lê.
Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.

```yaml
Type: AzureRMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
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
Mostra o que aconteceria se o cmdlet fosse executado. O cmdlet não é executado.

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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

### PSAzureProfile

## INFORMA

## LINKS RELACIONADOS

[Select-AzureRMProfile]()

