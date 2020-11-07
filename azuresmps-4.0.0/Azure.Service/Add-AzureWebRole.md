---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: FB5CD696-108D-4A3E-8983-1C6562E8795A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25ade8ccf395d37ab0856742fe473a6508c9d63b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945711"
---
# Add-AzureWebRole

## Sinopse
Adiciona uma função de trabalho da Web.

## SYNTAX

```
Add-AzureWebRole [-TemplateFolder <String>] [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## DESCRITIVO
Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.
Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .

O cmdlet **Add-AzureWebRole** adiciona uma função de trabalho da Web.

## EXEMPLOS

### Exemplo 1: adicionar uma função padrão
```
PS C:\> Add-AzureWebRole
```

Esse comando adiciona a função da Web que tem a configuração padrão de Webrole1 como o nome e uma única instância.

### Exemplo 2: adicionar uma função com um nome
```
PS C:\> Add-AzureWebRole -Name "MyWebRole"
```

Esse comando adiciona uma única função da Web chamada MyWebRole ao aplicativo atual.

### Exemplo 3: adicionar uma função com um nome e uma contagem de instâncias
```
PS C:\> Add-AzureWebRole -Name "MyWebRole" -Instance 2
```

Esse comando adiciona uma função da Web chamada MyWebRole ao aplicativo atual.
O cmdlet tem uma contagem de instâncias de função 2.

### Exemplo 4: adicionar uma função com um nome e um modelo
```
PS C:\> Add-AzureWebRole -Name "MyWebRole" -TemplateFolder ".\MyWebTemplateFolder"
```

Esse comando adiciona uma única função da Web chamada MyWebRole ao aplicativo atual.
O comando especifica uma pasta chamada MyWebTemplateFolder como um modelo scaffolding.

## OS

### -Instâncias
Especifica o número de instâncias.

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
Especifica a pasta do modelo.

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

[Add-AzureWorkerRole](./Add-AzureWorkerRole.md)

[New-AzureRoleTemplate](./New-AzureRoleTemplate.md)


