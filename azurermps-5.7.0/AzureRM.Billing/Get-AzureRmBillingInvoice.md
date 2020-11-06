---
external help file: Microsoft.Azure.Commands.Billing.dll-Help.xml
Module Name: AzureRM.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.billing/get-azurermbillinginvoice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingInvoice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingInvoice.md
ms.openlocfilehash: 5a6ccf36f8e7aecdca4d6560614e9185a5ca26b7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427669"
---
# Get-AzureRmBillingInvoice

## Sinopse
Obter faturas de cobrança da assinatura.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### Lista (padrão)
```
Get-AzureRmBillingInvoice [-MaxCount <Int32>] [-GenerateDownloadUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Novidades
```
Get-AzureRmBillingInvoice [-Latest] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Apenas
```
Get-AzureRmBillingInvoice -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmBillingInvoice** recebe faturas de cobrança da assinatura. 

## EXEMPLOS

### Exemplo 1
```
PS C:\> Get-AzureRmBillingInvoice -Latest
```

Obtenha a última fatura da assinatura.

### Exemplo 2
```
PS C:\> Get-AzureRmBillingInvoice -Name 2017-02-18-432543543
```

Obter a fatura da assinatura com o nome especificado.

### Exemplo 3
```
PS C:\> Get-AzureRmBillingInvoice
```

Obtenha todas as faturas disponíveis da assinatura em ordem cronológica inversa, começando com a fatura mais recente sem baixar a URL. 

### Exemplo 4
```
PS C:\> Get-AzureRmBillingInvoice -GenerateDownloadUrl -MaxCount 10
```

Obtenha 10 faturas mais recentes da assinatura e inclua a URL de download no resultado.

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GenerateDownloadUrl
Gerar a URL de download das faturas.

```yaml
Type: SwitchParameter
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Mais recente
Obtenha a última fatura.

```yaml
Type: SwitchParameter
Parameter Sets: Latest
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxCount
Determina o número máximo de registros a serem retornados.

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Nome de uma fatura específica a ser obtida ou a mais recente se não for especificada.

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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma

## EXIBE

### System. Collections. Generic. List ' 1 [Microsoft. Azure. Management. billing. Models. Invoice, Microsoft. Azure. Commands. Rebilling, Version = 0.14.0.0, Culture = neutral, PublicKeyToken = null]]
Microsoft. Azure. Management. cobrança. Models. revoice

## INFORMA

## LINKS RELACIONADOS

