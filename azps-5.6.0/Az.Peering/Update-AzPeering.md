---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/update-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Update-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Update-AzPeering.md
ms.openlocfilehash: 0824693c2d9f849b80f36065814f8dc57209a2a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890120"
---
# <span data-ttu-id="bbc80-101">Update-AzPeering</span><span class="sxs-lookup"><span data-stu-id="bbc80-101">Update-AzPeering</span></span>

## <span data-ttu-id="bbc80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bbc80-102">SYNOPSIS</span></span>
<span data-ttu-id="bbc80-103">Define o Paring.</span><span class="sxs-lookup"><span data-stu-id="bbc80-103">Sets the Peering.</span></span> <span data-ttu-id="bbc80-104">Use este Comando em conjunto com `Set-AzDirectPeeringConnectionObject` ou `Set-AzExchangePeeringConnectionObject` .</span><span class="sxs-lookup"><span data-stu-id="bbc80-104">Use this Command in conjunction with `Set-AzDirectPeeringConnectionObject` or `Set-AzExchangePeeringConnectionObject`.</span></span>

## <span data-ttu-id="bbc80-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="bbc80-105">SYNTAX</span></span>

### <span data-ttu-id="bbc80-106">DefaultExchange (Padrão)</span><span class="sxs-lookup"><span data-stu-id="bbc80-106">DefaultExchange (Default)</span></span>
```
Update-AzPeering -InputObject <PSPeering> [[-ExchangeConnection] <PSExchangeConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bbc80-107">DefaultDirect</span><span class="sxs-lookup"><span data-stu-id="bbc80-107">DefaultDirect</span></span>
```
Update-AzPeering -InputObject <PSPeering> [-DirectConnection <PSDirectConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bbc80-108">ByResourceIdDirect</span><span class="sxs-lookup"><span data-stu-id="bbc80-108">ByResourceIdDirect</span></span>
```
Update-AzPeering -ResourceId <String> [-DirectConnection <PSDirectConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bbc80-109">ByResourceIdExchange</span><span class="sxs-lookup"><span data-stu-id="bbc80-109">ByResourceIdExchange</span></span>
```
Update-AzPeering -ResourceId <String> [-ExchangeConnection] <PSExchangeConnection[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bbc80-110">Direct</span><span class="sxs-lookup"><span data-stu-id="bbc80-110">Direct</span></span>
```
Update-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-DirectConnection <PSDirectConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bbc80-111">Exchange</span><span class="sxs-lookup"><span data-stu-id="bbc80-111">Exchange</span></span>
```
Update-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-ExchangeConnection] <PSExchangeConnection[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bbc80-112">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="bbc80-112">DESCRIPTION</span></span>
<span data-ttu-id="bbc80-113">Define o objeto PSPeering</span><span class="sxs-lookup"><span data-stu-id="bbc80-113">Sets the PSPeering Object</span></span>

## <span data-ttu-id="bbc80-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bbc80-114">EXAMPLES</span></span>

### <span data-ttu-id="bbc80-115">Atualizar chave de autenticação Md5</span><span class="sxs-lookup"><span data-stu-id="bbc80-115">Update Md5 Authentication Key</span></span>
```powershell
PS C:> $peering = Get-AzPeering -ResourceGroupName rg1 -PeerName "ContosoPeering"  
PS C:> $peering.Connections[0] = $peering.Connections[0] | Set-AzPeeringDirectConnectionObject -MD5AuthenticationKey $hash
PS C:> $peering | Update-AzPeering
```

<span data-ttu-id="bbc80-116">Define a chave de autenticação Md5</span><span class="sxs-lookup"><span data-stu-id="bbc80-116">Sets the Md5 Authentication Key</span></span>

### <span data-ttu-id="bbc80-117">Atualizar UseForPeeringService</span><span class="sxs-lookup"><span data-stu-id="bbc80-117">Update UseForPeeringService</span></span>
```powershell
PS C:> Update-AzPeering -ResourceGroupName rg1 -Name ContosoPeering -UseForPeeringService $true

Name                 : ContosoPeering
Sku.Name             : Premium_Direct_Free
Kind                 : Direct
Connections          : {71}
PeerAsn.Id           : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
UseForPeeringService : True
PeeringLocation      : Seattle
ProvisioningState    : Succeeded
Location             : West US 2
Id                   : /subscriptions//resourceGroups/rg1/providers/Microsoft.Peering/peerings/ContosoPeering
Type                 : Microsoft.Peering/peerings
Tags                 : {[tag2, value2], [tag1, value1]}
```

<span data-ttu-id="bbc80-118">Define o sinalizador Usar para o Serviço de Paração</span><span class="sxs-lookup"><span data-stu-id="bbc80-118">Sets the Use for Peering Service Flag</span></span>

### <span data-ttu-id="bbc80-119">Atualizar Endereço IPv4 para Peering do Exchange</span><span class="sxs-lookup"><span data-stu-id="bbc80-119">Update IPv4 Address for Exchange Peering</span></span>
```powershell
PS C:> $peering = Get-AzPeering -ResourceGroupName rg1  -PeerName "ContosoExchangePeering" 
PS C:> $peering.Connections[0] = $peering.Connections[0] | Set-AzPeeringExchangeConnectionObject -PeerSessionIPv4Address $ipv4Address
PS C:> Update-AzPeering -ResourceId $peering.Id $peering.Connections

Name              : ContosoExchangePeering
Sku.Name          : Basic_Exchange_Free
Kind              : Exchange
Connections       : {13, 13}
PeerAsn.Id        : /subscriptions//providers/Microsoft.Peering/peerAsns/PeerName6935
PeeringLocation   : Seattle
ProvisioningState : Succeeded
Location          : West US 2
Id                : /subscriptions//resourceGroups/rg1/providers/Microsoft.Peering/peerings/ContosoExchangePeering
Type              : Microsoft.Peering/peerings
Tags              : {}
```

<span data-ttu-id="bbc80-120">Define o Endereço Ipv4 para um Peering do Exchange usando ResourceId</span><span class="sxs-lookup"><span data-stu-id="bbc80-120">Sets the Ipv4 Address for an Exchange Peering using ResourceId</span></span>

## <span data-ttu-id="bbc80-121">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="bbc80-121">PARAMETERS</span></span>

### <span data-ttu-id="bbc80-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbc80-122">-DefaultProfile</span></span>
<span data-ttu-id="bbc80-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bbc80-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bbc80-124">-DirectConnection</span><span class="sxs-lookup"><span data-stu-id="bbc80-124">-DirectConnection</span></span>
<span data-ttu-id="bbc80-125">Crie uma nova conexão Direta usando o New-AzDirectPeeringConnectionObject e canal para esse comando.</span><span class="sxs-lookup"><span data-stu-id="bbc80-125">Create a new Direct connections using the New-AzDirectPeeringConnectionObject and pipe to this command.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection[]
Parameter Sets: DefaultDirect, ByResourceIdDirect, Direct
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbc80-126">-ExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="bbc80-126">-ExchangeConnection</span></span>
<span data-ttu-id="bbc80-127">Crie uma nova conexão do Exchange usando o New-AzExchangePeeringConnectionObject e canal para este comando.</span><span class="sxs-lookup"><span data-stu-id="bbc80-127">Create a new Exchange connection using the New-AzExchangePeeringConnectionObject and pipe to this command.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection[]
Parameter Sets: DefaultExchange
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection[]
Parameter Sets: ByResourceIdExchange, Exchange
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbc80-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bbc80-128">-InputObject</span></span>
<span data-ttu-id="bbc80-129">O objeto Peering</span><span class="sxs-lookup"><span data-stu-id="bbc80-129">The Peering object</span></span> 

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: DefaultExchange, DefaultDirect
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bbc80-130">-Name</span><span class="sxs-lookup"><span data-stu-id="bbc80-130">-Name</span></span>
<span data-ttu-id="bbc80-131">O nome exclusivo do PSPeering.</span><span class="sxs-lookup"><span data-stu-id="bbc80-131">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: Direct, Exchange
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbc80-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbc80-132">-ResourceGroupName</span></span>
<span data-ttu-id="bbc80-133">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bbc80-133">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Direct, Exchange
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbc80-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bbc80-134">-ResourceId</span></span>
<span data-ttu-id="bbc80-135">O nome da cadeia de caracteres de id de recurso.</span><span class="sxs-lookup"><span data-stu-id="bbc80-135">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdDirect, ByResourceIdExchange
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbc80-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bbc80-136">-Confirm</span></span>
<span data-ttu-id="bbc80-137">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbc80-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbc80-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbc80-138">-WhatIf</span></span>
<span data-ttu-id="bbc80-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bbc80-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbc80-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bbc80-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbc80-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbc80-141">CommonParameters</span></span>
<span data-ttu-id="bbc80-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbc80-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbc80-143">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bbc80-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbc80-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bbc80-144">INPUTS</span></span>

### <span data-ttu-id="bbc80-145">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="bbc80-145">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="bbc80-146">System.String</span><span class="sxs-lookup"><span data-stu-id="bbc80-146">System.String</span></span>

## <span data-ttu-id="bbc80-147">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="bbc80-147">OUTPUTS</span></span>

### <span data-ttu-id="bbc80-148">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="bbc80-148">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="bbc80-149">NOTES</span><span class="sxs-lookup"><span data-stu-id="bbc80-149">NOTES</span></span>

## <span data-ttu-id="bbc80-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bbc80-150">RELATED LINKS</span></span>
