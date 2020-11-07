---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: F9A06B8B-55DB-48A5-B246-53347E759E64
online version: ''
schema: 2.0.0
ms.openlocfilehash: 050c05f2cdad546388744bcebca4f28a12a03038
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946390"
---
# Add-AzurePHPWebRole

## Sinopse
Cria os arquivos necessários e a configuração para um aplicativo PHP.

## SYNTAX

```
Add-AzurePHPWebRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.
Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .

O cmdlet **Add-AzurePHPWebRole** cria os arquivos e a configuração, às vezes chamados de scaffolding, para um aplicativo PHP que será hospedado no Azure pelo IIS.

## EXEMPLOS

### Exemplo 1: adicionar uma função da Web usando valores padrão
```
PS C:\> Add-AzurePHPWebRole
```

Este exemplo adiciona os arquivos e a configuração necessários para a nova função da Web usando os valores padrão de um serviço chamado "WebRole1" com 1 instância.

### Exemplo 2: adicionar uma função da Web com várias instâncias
```
PS C:\> Add-AzurePHPWebRole MyWebRole -I 2
```

Este exemplo adiciona os arquivos e a configuração necessários para uma nova função da Web ao aplicativo atual, usando o nome "MyWebRole" e uma contagem de instâncias de função 2.

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
O nome determina o nome do diretório que contém os arquivos necessários e a configuração para o aplicativo PHP.
O padrão é WebRole #, em que # é o número de funções da Web no serviço.

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

[Add-AzurePHPWorkerRole](./Add-AzurePHPWorkerRole.md)

[New-AzureServiceProject](./New-AzureServiceProject.md)


