---
external help file: Microsoft.Azure.Commands.Billing.dll-Help.xml
Module Name: AzureRM.Billing
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingPeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingPeriod.md
ms.openlocfilehash: f6b75a1c161515ee45571ba3db6d2f84b95af967
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428276"
---
# Get-AzureRmBillingPeriod

## Sinopse
Obter períodos de cobrança da assinatura.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### Lista (padrão)
```
Get-AzureRmBillingPeriod [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Apenas
```
Get-AzureRmBillingPeriod -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmBillingPeriod** Obtém períodos de cobrança da assinatura.

## EXEMPLOS

### Exemplo 1
```
PS C:\> Get-AzureRmBillingPeriod
```

Obtenha todos os períodos de cobrança disponíveis da assinatura.

### Exemplo 2
```
PS C:\> Get-AzureRmBillingPeriod -Name 201704-1
```

Obter o período de cobrança da assinatura com o nome especificado.

### Exemplo 3
```
PS C:\> Get-AzureRmBillingPeriod -MaxCount 2
```

Obter no máximo 2 períodos de cobrança da assinatura.

## OS

### -MaxCount
Determine o número máximo de registros a serem retornados.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Nome de um período de cobrança específico para obter.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Single
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma

## EXIBE

### System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. billing. Models. PSBillingPeriod, Microsoft. Azure. Commands. Billing, Version = 0.12.0.0, Culture = neutral, PublicKeyToken = null]]
Microsoft. Azure. Commands. billing. Models. PSBillingPeriod

## INFORMA

## LINKS RELACIONADOS

