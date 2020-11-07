---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 3B3F1870-348D-4303-9520-FD81D4650F5F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2103a155b12fdf1e481173d529ff3308a3b2200b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946512"
---
# Get-AzureWebHostingPlan

## Sinopse
Obtém os planos de hospedagem da Web do Azure na assinatura atual.

## SYNTAX

```
Get-AzureWebHostingPlan [-WebSpaceName <String>] [-Name <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## DESCRITIVO
Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.
Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .

O cmdlet **Get-AzureWebHostingPlan** Obtém os planos de hospedagem da Web do Azure na assinatura atual.

Por padrão, **Get-AzureWebHostingPlan** Obtém todos os planos de hospedagem do Azure na assinatura atual e retorna um objeto que fornece informações básicas sobre os planos.
Quando você usa os parâmetros *espaço* de *nomes e nome* , **Get-AzureWebHostingPlan** retorna um objeto de plano de hospedagem específico.

Para localizar a assinatura atual, use o parâmetro *atual* do cmdlet **Get-AzureSubscription** .
Para alterar a assinatura atual, use o cmdlet **Select-AzureSubscription** .

## EXEMPLOS

### Exemplo 1: obter todos os planos de hospedagem na Web em uma assinatura
```
PS C:\> Get-AzureWebHostingPlan 

Name : Default1 
SKU : Basic 
WorkerSize : Small 
NumberOfWorkers : 1 
CurrentWorkerSize : Small 
CurrentNumberOfWorkers : 1 
Status : Ready 
WebSpace : eastuswebspace 
Name : Default0 
SKU : Free 
WorkerSize : Small 
NumberOfWorkers : 0 
CurrentWorkerSize : Small 
CurrentNumberOfWorkers : 0 
Status : Ready
```

Este comando obtém todos os planos de hospedagem da Web do Azure na assinatura atual.

### Exemplo 2: obter um plano de hospedagem da Web específico em uma assinatura
```
PS C:\> Get-AzureWebHostingPlan -WebSpaceName "westeuropewebspace" -Name "Default0" 

Name : Default0 
SKU : Free 
WorkerSize : Small 
NumberOfWorkers : 0 
CurrentWorkerSize : Small 
CurrentNumberOfWorkers : 0 
Status : Ready 
WebSpace : westeuropewebspace
```

Esse comando obtém o plano de hospedagem na Web chamado Default0 no espaço de nomes westeuropewebspace na assinatura atual.

## OS

### -Nome
Especifica o nome de um plano na assinatura.
Por padrão, esse cmdlet obtém todos os planos na assinatura atual.
Esse parâmetro não oferece suporte a caracteres curinga.

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

### -Webspacename
Especifica o nome de um espaço da Web na assinatura.
Por padrão, esse cmdlet obtém todos os sites no espaço Web especificado.
Esse parâmetro não oferece suporte a caracteres curinga.

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebSpace

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

###  
Você pode passar a entrada para esse cmdlet pelo nome da propriedade, mas não por valor.

## EXIBE

### Microsoft. WindowsAzure. Commands. Utilities. sites. Services. webentities. WebHostingPlan
Por padrão, **Get-AzureWebHostingPlan** retorna uma matriz de objetos **WebHostingPlan** .

## INFORMA

## LINKS RELACIONADOS

