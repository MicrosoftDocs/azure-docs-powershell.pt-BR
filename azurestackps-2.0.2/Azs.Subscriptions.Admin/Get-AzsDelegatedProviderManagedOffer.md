---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsdelegatedprovidermanagedoffer
schema: 2.0.0
ms.openlocfilehash: 238fe2a9c3f0cf1d4fdefc5a09231066152cfe60
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93947153"
---
# Get-AzsDelegatedProviderManagedOffer

## Sinopse
Obter a oferta do provedor delegado especificado.

## SYNTAX

### Lista (padrão)
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProviderSubscriptionId <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### Obter
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProviderSubscriptionId <String> -Name <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzsDelegatedProviderManagedOffer -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## DESCRITIVO
Obter a oferta do provedor delegado especificado.

## EXEMPLOS

### Exemplo 1
```powershell
PS C:\> Get-AzsDelegatedProviderManagedOffer -DelegatedProviderSubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"

{{ Add output here }}
```

Obter a lista de ofertas de provedor delegado.

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -DelegatedProviderSubscriptionId
Identificador de assinatura de provedor delegado.

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases: DelegatedProviderId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -InputObject
Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### -Nome
Nome de uma oferta.

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -SubscriptionId
Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure. A ID da assinatura forma a parte do URI para cada chamada de serviço.

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

### Microsoft. Azure. PowerShell. cmdlets. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity

## EXIBE

### Microsoft. Azure. PowerShell. cmdlets. SubscriptionsAdmin. Models. Api20151101. IDelegatedProviderOffer

ALIASES

## INFORMA

Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas. Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.

INPUTobject <ISubscriptionsAdminIdentity> : parâmetro de identidade
  - `[DelegatedProvider <String>]`: Identificador DelegatedProvider.
  - `[DelegatedProviderSubscriptionId <String>]`: Identificador de assinatura de provedor delegado.
  - `[Id <String>]`: Caminho de identidade do recurso
  - `[Location <String>]`: O local do AzureStack.
  - `[ManifestName <String>]`: O nome do manifesto.
  - `[Offer <String>]`: Nome de uma oferta.
  - `[OfferDelegationName <String>]`: Nome de uma delegação de oferta.
  - `[OperationsStatusName <String>]`: O nome do status da operação.
  - `[Plan <String>]`: Nome do plano.
  - `[PlanAcquisitionId <String>]`: O identificador de aquisição do plano
  - `[Quota <String>]`: Nome da cota.
  - `[ResourceGroupName <String>]`: O grupo de recursos no qual o recurso está localizado.
  - `[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure. A ID da assinatura forma a parte do URI para cada chamada de serviço.
  - `[TargetSubscriptionId <String>]`: A ID da assinatura de destino.
  - `[Tenant <String>]`: Nome do locatário do diretório.

## LINKS RELACIONADOS

