---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7190C668-6A0C-4E1D-9B5A-0CEEF53E3F85
online version: ''
schema: 2.0.0
ms.openlocfilehash: 93573caf43a6c711e1aa1308c851c82faaef5bcd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946389"
---
# Add-AzureNodeWorkerRole

## Sinopse
Cria os arquivos e pastas necessários para que um aplicativo Node.js seja hospedado na nuvem via node.exe

## SYNTAX

```
Add-AzureNodeWorkerRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.
Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .

O cmdlet **Add-AzureNodeWorkerRole** cria os arquivos e as pastas necessárias, às vezes chamados de scaffolding, para que um aplicativo Node.js seja hospedado na nuvem via node.exe.

## EXEMPLOS

### Exemplo 1: função de trabalho de instância única
```
PS C:\> Add-AzureWorkerRole MyWorkerRole
```

Este exemplo adiciona scaffolding para uma única função de trabalho chamada **MyWorkerRole** ao aplicativo atual.

### Exemplo 2: função de trabalho de várias instâncias
```
PS C:\> Add-AzureNodeWorkerRole MyWorkerRole -I 2
```

Este exemplo adiciona scaffolding para uma única função de trabalho chamada **MyWorkerRole** ao aplicativo atual, com uma contagem de instância de função 2.

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
O valor determina o nome da pasta que contém o scaffolding para o serviço de node.js hospedado na função de trabalho.
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

[Add-AzureNodeWebRole](./Add-AzureNodeWebRole.md)

[New-AzureServiceProject](./New-AzureServiceProject.md)


