---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/get-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverMoveCollection.md
ms.openlocfilehash: a10ac77515b225c5e5ef06335f9cee1e99ecd3b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891657"
---
# Get-AzResourceMoverMoveCollection

## SYNOPSIS
Obtém a coleção move.

## SINTAXE

### Lista (Padrão)
```
Get-AzResourceMoverMoveCollection [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### Obter
```
Get-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### List1
```
Get-AzResourceMoverMoveCollection -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## DESCRIPTION
Obtém a coleção move.

## EXEMPLOS

### Exemplo 1: Obter detalhes de todas as coleções Move na assinatura
```powershell
PS C:\>Get-AzResourceMoverMoveCollection  -SubscriptionId "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"

Etag                                   Location      Name                                Type                             
----                                   --------      ----                                ----                             
"270119e0-0000-0c00-0000-5f5c94940000" centraluseuap PS-centralus-westcentralus-demoRMS  Microsoft.Migrate/moveCollections
"39015ed4-0000-0c00-0000-5f5ce2760000" centraluseuap PS-centralus-westcentralus-demo2RMS Microsoft.Migrate/moveCollections
"1000b505-0000-0c00-0000-5f69db6e0000" centraluseuap MoveCollection-cus-eus-ccy         Microsoft.Migrate/moveCollections


```

Obter detalhes de todas as coleções Move na assinatura.

### Exemplo 2: Obter detalhes da coleção Move com um nome de coleção de movimentação especificado na assinatura
```powershell
PS C:\>Get-AzResourceMoverMoveCollection -ResourceGroupName "RG-MoveCollection-demoRMS" -Name "PS-centralus-westcentralus-demoRMS"

Etag                                   Location      Name                               Type                             
----                                   --------      ----                               ----                             
"22006609-0000-3300-0000-602169590000" centraluseuap PS-centralus-westcentralus-demoRMS Microsoft.Migrate/moveCollections

```

Obter detalhes da coleção Move com um nome de coleção de movimentação especificado na assinatura.

### Exemplo 3: Obter detalhes da coleção Move com um nome de grupo de recursos especificado na assinatura
```powershell
PS C:\> Get-AzResourceMoverMoveCollection -ResourceGroupName "RG-MoveCollection-demoRMS" 

Location    Name                               Type
--------    ----                               ----
eastus2     PS-centralus-westcentralus-demoRM  Microsoft.Migrate/moveCollections
Etag                                   Location      Name                                Type                             
----                                   --------      ----                                ----                             
"22006609-0000-3300-0000-602169590000" centraluseuap PS-centralus-westcentralus-demoRMS  Microsoft.Migrate/moveCollections
"4e02b0a9-0000-0c00-0000-5fd101cc0000" centraluseuap PS-centralus-westcentralus-demo2RMS Microsoft.Migrate/moveCollections

```

Obter detalhes da Coleção Move com um nome de grupo de recursos especificado na assinatura.

## PARÂMETROS

### -DefaultProfile
As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.

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

### -Name
O nome da coleção Move.

```yaml
Type: System.String
Parameter Sets: Get
Aliases: MoveCollectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
O Nome do Grupo de Recursos.

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
A ID da Assinatura.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## SAÍDAS

### Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IMoveCollection

## NOTES

ALIASES

## LINKS RELACIONADOS

