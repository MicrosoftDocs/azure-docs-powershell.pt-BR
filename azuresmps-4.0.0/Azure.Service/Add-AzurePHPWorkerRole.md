---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: FEFBF1EF-FBCE-45D8-8455-F3F8662F1F36
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4ddf78f30cb6938571fc967d510e4ab99a0cfc80
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946387"
---
# Add-AzurePHPWorkerRole

## Sinopse
Cria os arquivos e a configuração necessários para um aplicativo PHP que será hospedado no Azure por meio de php.exe.

## SYNTAX

```
Add-AzurePHPWorkerRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.
Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .

Cria os arquivos e a configuração necessários, às vezes chamados de scaffolding, para um aplicativo PHP que será hospedado no Azure por meio de php.exe.

## EXEMPLOS

### Exemplo 1: criar uma função de trabalho com uma única instância
```
PS C:\> Add-AzurePHPWorkerRole MyWorkerRole
```

Este exemplo adiciona os arquivos e a configuração necessários para uma única função de trabalho chamada MyWorkerRole ao aplicativo atual.

### Exemplo 2: criar uma função de trabalho com várias instâncias
```
PS C:\> Add-AzurePHPWorkerRole MyWorkerRole -I 2
```

Este exemplo adiciona os arquivos e a configuração necessários para uma nova função de trabalho ao aplicativo atual, usando o nome MyWorkerRole com uma contagem de instâncias de função 2.

## OS

### -Instâncias
Especifica o número de instâncias de função para esta função de trabalho.
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
Especifica o nome da função de trabalho.
O nome determina o nome da pasta que contém os arquivos necessários e a configuração para o serviço PHP hospedado na função de trabalho.
O padrão é WorkerRole1.

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

[New-AzureServiceProject](./New-AzureServiceProject.md)

[Add-AzurePHPWebRole](./Add-AzurePHPWebRole.md)


