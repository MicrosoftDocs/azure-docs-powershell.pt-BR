---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: C2DAFB2C-A58B-406C-8349-8728771B279E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 59aef29c27d7eb96834d270c2fce48ff3acb9554
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946392"
---
# Add-AzureNodeWebRole

## Sinopse
Cria arquivos e pastas necessários para um aplicativo Node.js.

## SYNTAX

```
Add-AzureNodeWebRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.
Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .

O **Add-AzureNodeWebRole** cria arquivos e pastas necessários, às vezes chamados de scaffolding, para que um aplicativo Node.js seja hospedado na nuvem via IIS.

## EXEMPLOS

### Exemplo 1: função da Web de instância única
```
PS C:\> Add-AzureNodeWebRole -Name MyWebRole
```

Este exemplo adiciona scaffolding para uma única função da Web chamada **MyWebRole** ao aplicativo atual.

### Exemplo 2: função da Web com várias instâncias
```
PS C:\> Add-AzureNodeWebRole MyWebRole -I 2
```

Este exemplo adiciona scaffolding para uma nova função da Web chamada **MyWebRole** ao aplicativo atual, com uma contagem de instância de função 2.

## OS

### -Instâncias
Especifica o número de instâncias de função para esta função da Web.
O padrão é 1.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: i

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Especifica o nome da função da Web.
Ele também determina o nome do diretório que contém o scaffolding para o aplicativo node.js que será hospedado na função da Web.
O padrão é WebRole #, em que # indica o número de funções da Web no serviço.

```yaml
Type: String
Parameter Sets: (All)
Aliases: n

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

## INFORMA

## LINKS RELACIONADOS

[Add-AzureNodeWorkerRole](./Add-AzureNodeWorkerRole.md)

[New-AzureServiceProject](./New-AzureServiceProject.md)


