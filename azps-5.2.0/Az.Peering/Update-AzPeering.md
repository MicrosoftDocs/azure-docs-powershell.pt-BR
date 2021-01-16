---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/update-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Update-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Update-AzPeering.md
ms.openlocfilehash: 0f757c6bbde541876a3b4889f300a8d18e1cf113
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261402"
---
# <span data-ttu-id="96018-101">Update-AzPeering</span><span class="sxs-lookup"><span data-stu-id="96018-101">Update-AzPeering</span></span>

## <span data-ttu-id="96018-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="96018-102">SYNOPSIS</span></span>
<span data-ttu-id="96018-103">Define o emparelhamento.</span><span class="sxs-lookup"><span data-stu-id="96018-103">Sets the Peering.</span></span> <span data-ttu-id="96018-104">Use este comando em conjunto com `Set-AzDirectPeeringConnectionObject` ou `Set-AzExchangePeeringConnectionObject` .</span><span class="sxs-lookup"><span data-stu-id="96018-104">Use this Command in conjunction with `Set-AzDirectPeeringConnectionObject` or `Set-AzExchangePeeringConnectionObject`.</span></span>

## <span data-ttu-id="96018-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="96018-105">SYNTAX</span></span>

### <span data-ttu-id="96018-106">Defaultexchange (padrão)</span><span class="sxs-lookup"><span data-stu-id="96018-106">DefaultExchange (Default)</span></span>
```
Update-AzPeering -InputObject <PSPeering> [[-ExchangeConnection] <PSExchangeConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96018-107">Defaultdirect</span><span class="sxs-lookup"><span data-stu-id="96018-107">DefaultDirect</span></span>
```
Update-AzPeering -InputObject <PSPeering> [-DirectConnection <PSDirectConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96018-108">ByResourceIdDirect</span><span class="sxs-lookup"><span data-stu-id="96018-108">ByResourceIdDirect</span></span>
```
Update-AzPeering -ResourceId <String> [-DirectConnection <PSDirectConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96018-109">ByResourceIdExchange</span><span class="sxs-lookup"><span data-stu-id="96018-109">ByResourceIdExchange</span></span>
```
Update-AzPeering -ResourceId <String> [-ExchangeConnection] <PSExchangeConnection[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96018-110">Orientar</span><span class="sxs-lookup"><span data-stu-id="96018-110">Direct</span></span>
```
Update-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-DirectConnection <PSDirectConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96018-111">Cambia</span><span class="sxs-lookup"><span data-stu-id="96018-111">Exchange</span></span>
```
Update-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-ExchangeConnection] <PSExchangeConnection[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96018-112">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="96018-112">DESCRIPTION</span></span>
<span data-ttu-id="96018-113">Define o objeto PSPeering</span><span class="sxs-lookup"><span data-stu-id="96018-113">Sets the PSPeering Object</span></span>

## <span data-ttu-id="96018-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="96018-114">EXAMPLES</span></span>

### <span data-ttu-id="96018-115">Atualize a chave de autenticação MD5</span><span class="sxs-lookup"><span data-stu-id="96018-115">Update Md5 Authentication Key</span></span>
```powershell
PS C:> $peering = Get-AzPeering -ResourceGroupName rg1 -PeerName "ContosoPeering"  
PS C:> $peering.Connections[0] = $peering.Connections[0] | Set-AzPeeringDirectConnectionObject -MD5AuthenticationKey $hash
PS C:> $peering | Update-AzPeering
```

<span data-ttu-id="96018-116">Define a chave de autenticação MD5</span><span class="sxs-lookup"><span data-stu-id="96018-116">Sets the Md5 Authentication Key</span></span>

### <span data-ttu-id="96018-117">Atualizar UseForPeeringService</span><span class="sxs-lookup"><span data-stu-id="96018-117">Update UseForPeeringService</span></span>
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

<span data-ttu-id="96018-118">Define o sinalizador de uso para serviço de emparelhamento</span><span class="sxs-lookup"><span data-stu-id="96018-118">Sets the Use for Peering Service Flag</span></span>

### <span data-ttu-id="96018-119">Atualize o endereço IPv4 da troca de tráfego do Exchange</span><span class="sxs-lookup"><span data-stu-id="96018-119">Update IPv4 Address for Exchange Peering</span></span>
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

<span data-ttu-id="96018-120">Define o endereço IPv4 para um emparelhamento do Exchange usando ResourceId</span><span class="sxs-lookup"><span data-stu-id="96018-120">Sets the Ipv4 Address for an Exchange Peering using ResourceId</span></span>

## <span data-ttu-id="96018-121">OS</span><span class="sxs-lookup"><span data-stu-id="96018-121">PARAMETERS</span></span>

### <span data-ttu-id="96018-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96018-122">-DefaultProfile</span></span>
<span data-ttu-id="96018-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="96018-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96018-124">-DirectConnection</span><span class="sxs-lookup"><span data-stu-id="96018-124">-DirectConnection</span></span>
<span data-ttu-id="96018-125">Crie uma nova conexão direta usando o New-AzDirectPeeringConnectionObject e o pipe para esse comando.</span><span class="sxs-lookup"><span data-stu-id="96018-125">Create a new Direct connections using the New-AzDirectPeeringConnectionObject and pipe to this command.</span></span>

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

### <span data-ttu-id="96018-126">-ExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="96018-126">-ExchangeConnection</span></span>
<span data-ttu-id="96018-127">Crie uma nova conexão do Exchange usando o New-AzExchangePeeringConnectionObject e o pipe para esse comando.</span><span class="sxs-lookup"><span data-stu-id="96018-127">Create a new Exchange connection using the New-AzExchangePeeringConnectionObject and pipe to this command.</span></span>

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

### <span data-ttu-id="96018-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="96018-128">-InputObject</span></span>
<span data-ttu-id="96018-129">O objeto de emparelhamento</span><span class="sxs-lookup"><span data-stu-id="96018-129">The Peering object</span></span> 

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

### <span data-ttu-id="96018-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="96018-130">-Name</span></span>
<span data-ttu-id="96018-131">O nome exclusivo da PSPeering.</span><span class="sxs-lookup"><span data-stu-id="96018-131">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="96018-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96018-132">-ResourceGroupName</span></span>
<span data-ttu-id="96018-133">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="96018-133">The resource group name.</span></span>

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

### <span data-ttu-id="96018-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="96018-134">-ResourceId</span></span>
<span data-ttu-id="96018-135">O nome da cadeia de caracteres da ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="96018-135">The resource id string name.</span></span>

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

### <span data-ttu-id="96018-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="96018-136">-Confirm</span></span>
<span data-ttu-id="96018-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96018-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96018-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96018-138">-WhatIf</span></span>
<span data-ttu-id="96018-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="96018-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96018-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="96018-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96018-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96018-141">CommonParameters</span></span>
<span data-ttu-id="96018-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96018-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96018-143">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="96018-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96018-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="96018-144">INPUTS</span></span>

### <span data-ttu-id="96018-145">Microsoft. Azure. PowerShell. cmdlets. peering. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="96018-145">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="96018-146">System. String</span><span class="sxs-lookup"><span data-stu-id="96018-146">System.String</span></span>

## <span data-ttu-id="96018-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="96018-147">OUTPUTS</span></span>

### <span data-ttu-id="96018-148">Microsoft. Azure. PowerShell. cmdlets. peering. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="96018-148">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="96018-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="96018-149">NOTES</span></span>

## <span data-ttu-id="96018-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="96018-150">RELATED LINKS</span></span>
