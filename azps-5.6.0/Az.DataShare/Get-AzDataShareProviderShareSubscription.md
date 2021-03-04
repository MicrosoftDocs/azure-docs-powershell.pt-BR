---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/get-azdatashareprovidersharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareProviderShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareProviderShareSubscription.md
ms.openlocfilehash: b28182a5593454b110b2fe4036b022a8d74c33d0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893180"
---
# Get-AzDataShareProviderShareSubscription

## SYNOPSIS
Obtém informações sobre assinaturas de compartilhamento de consumidor no lado do provedor.

## SINTAXE

### ByFieldsParameterSet (Padrão)
```
Get-AzDataShareProviderShareSubscription -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-ShareSubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByProviderShareSubscriptionIdParameterSet
```
Get-AzDataShareProviderShareSubscription [-ShareSubscriptionId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIPTION
O cmdlet **Get-AzDataShareProviderSubscription** obtém informações sobre assinaturas de compartilhamento de consumidor no lado do provedor. Se você especificar a id de subscrption do compartilhamento, este cmdlet obtém informações sobre a assinatura de compartilhamento. Se você não especificar a id de assinatura de compartilhamento, este cmdlet obterá informações sobre todas as assinaturas de compartilhamento de consumidor associadas ao compartilhamento.

## EXEMPLOS

### Exemplo 1
```
PS C:\> Get-AzDataShareProviderShareSubscription -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -ShareSubscriptionId "/subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shares/AdsShare/shareSubscriptions/505c3500-b2ff-46ab-96bf-50f5ec89d75a"

Company                   : ADS Test
CreatedAt                 : 6/30/2019 12:42:12 AM
CreatedBy                 : adstest@microsoft.com
SharedAt                  : 6/30/2019 12:41:37 AM
SharedBy                  : adsprovider@microsoft.com
ShareSubscriptionObjectId : 505c3500-b2ff-46ab-96bf-50f5ec89d75a
ShareSubscriptionStatus   : Active
Id                        : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shares/AdsShare/shareSubscriptions/505c3500-b2ff-46ab-96bf-50f5ec89d75a
Name                      : AdsShareSubscription
Type                      : Microsoft.DataShare/ShareSubscriptions
```

Esses comandos fornece informações sobre a assinatura de compartilhamento de consumidor associada ao compartilhamento AdsShare na conta de compartilhamento de dados WikiAds.

## PARÂMETROS

### -AccountName
Nome da conta do Azure DataShare.

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.

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

### -ResourceGroupName
O grupo de recursos da Conta do Azure DataShare.

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
A id de recurso do compartilhamento

```yaml
Type: System.String
Parameter Sets: ByProviderShareSubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ShareName
Nome do Azure DataShare.

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ShareSubscriptionId
A id da assinatura de compartilhamento de consumidor

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String

## SAÍDAS

### Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription

## NOTES

## LINKS RELACIONADOS
