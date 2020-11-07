---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E499868E-A745-4CA4-A717-C33C3B94A2C8
online version: ''
schema: 2.0.0
ms.openlocfilehash: b80071bb82ebbb960be5b5b4fcc854dc47c9ed9d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945992"
---
# New-AzureRoleTemplate

## Sinopse
Cria modelos de função de trabalho e Web.

## SYNTAX

### WebRole
```
New-AzureRoleTemplate [-Web] [-Output <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### WorkerRole
```
New-AzureRoleTemplate [-Worker] [-Output <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.
Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .

O cmdlet **New-AzureRoleTemplate** cria modelos de função de trabalho e Web.

## EXEMPLOS

### Exemplo 1: criar um modelo de função da Web
```
PS C:\> New-AzureRoleTemplate -Web
```

Este exemplo cria um novo modelo de função da Web em uma pasta chamada webroletemplate no diretório atual.

### Exemplo 2: criar um modelo de função de trabalhador
```
PS C:\> New-AzureRoleTemplate -Worker
```

Este exemplo cria um novo modelo de função de trabalho em uma pasta chamada webroletemplate no diretório atual.

### Exemplo 3: criar um modelo de função em um diretório personalizado
```
PS C:\> New-AzureRoleTemplate -Web -Output C:\MyWebRoleTemplate
```

Este exemplo cria um novo modelo de função da Web no diretório chamado MyWebRoleTemplate, em vez de no diretório atual.

## OS

### -Saída
Especifica o caminho de saída do modelo gerado.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Perfil
Especifica o perfil do Azure do qual este cmdlet lê.
Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Web
Especifica que você deseja criar um modelo de função da Web.

```yaml
Type: SwitchParameter
Parameter Sets: WebRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Trabalhador
Especifica que você deseja criar um modelo de função de trabalho.

```yaml
Type: SwitchParameter
Parameter Sets: WorkerRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

## INFORMA

## LINKS RELACIONADOS

[Add-AzureWebRole](./Add-AzureWebRole.md)

[Add-AzureWorkerRole](./Add-AzureWorkerRole.md)


