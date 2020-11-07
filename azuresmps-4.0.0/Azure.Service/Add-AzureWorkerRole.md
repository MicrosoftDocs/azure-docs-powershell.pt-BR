---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 8632A865-D4CC-4AE5-8307-055CDD776D26
online version: ''
schema: 2.0.0
ms.openlocfilehash: a2b79ee50bb5097896c2a120a9b7316adb2146b5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945710"
---
# Add-AzureWorkerRole

## Sinopse
Cria arquivos obrigatórios e configuração para uma função de trabalhador personalizada.

## SYNTAX

```
Add-AzureWorkerRole [-TemplateFolder <String>] [-Name <String>] [-Instances <Int32>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.
Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .

O cmdlet **Add-AzureWorkerRole** cria arquivos e configurações necessários, às vezes chamados de scaffolding, para uma função de trabalhador personalizada.

## EXEMPLOS

### Exemplo 1: criar uma única função de trabalho de instância
```
PS C:\> Add-AzureWorkerRole -Name MyWorkerRole
```

Este exemplo adiciona scaffolding para uma única função de trabalho chamada MyWorkerRole ao aplicativo atual.

### Exemplo 2: criar uma função de trabalho de várias instâncias
```
PS C:\> Add-AzureWorkerRole MyWorkerRole -I 2
```

Este exemplo adiciona scaffolding para uma nova função de trabalho chamada MyWorkerRole ao aplicativo atual, com uma contagem de instância de função 2.

### Exemplo 3: criar função de trabalho com o scaffolding personalizado
```
PS C:\> Add-AzureWorkerRole MyWorkerRole -TemplateFoldr .\MyWorkerRoleTemplate
```

Este exemplo cria uma função de trabalho com scaffolding personalizado.

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
Esse valor determina o nome da pasta que contém o scaffolding para o aplicativo personalizado que será hospedado na função de trabalho.
O padrão é WorkerRolenumber, em que núm é o número de funções de trabalho no serviço.

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

### -TemplateFolder
Especifica a pasta de modelos do scaffolding a ser usada para criar a função de trabalho.

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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

## INFORMA

## LINKS RELACIONADOS

[Add-AzureWebRole](./Add-AzureWebRole.md)

[New-AzureRoleTemplate](./New-AzureRoleTemplate.md)


