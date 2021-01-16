---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillingperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingPeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingPeriod.md
ms.openlocfilehash: 6a7f7d47976608b521e69e7aaf926a9600b35382
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261691"
---
# Get-AzBillingPeriod

## Sinopse
Obter períodos de cobrança da assinatura.

## SYNTAX

### Lista (padrão)
```
Get-AzBillingPeriod [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Apenas
```
Get-AzBillingPeriod -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzBillingPeriod** Obtém períodos de cobrança da assinatura.

## EXEMPLOS

### Exemplo 1
```
PS C:\> Get-AzBillingPeriod
```

Obtenha todos os períodos de cobrança disponíveis da assinatura.

### Exemplo 2
```
PS C:\> Get-AzBillingPeriod -Name 201704-1
```

Obter o período de cobrança da assinatura com o nome especificado.

### Exemplo 3
```
PS C:\> Get-AzBillingPeriod -MaxCount 2
```

Obter no máximo 2 períodos de cobrança da assinatura.

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma

## EXIBE

### Microsoft. Azure. Commands. billing. Models. PSBillingPeriod

## INFORMA

## LINKS RELACIONADOS
