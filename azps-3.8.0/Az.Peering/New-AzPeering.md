---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeering.md
ms.openlocfilehash: 9bbf7b8540de15f79b93cbb3a7fe90f5ad14ee18
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941859"
---
# <span data-ttu-id="e133f-101">New-AzPeering</span><span class="sxs-lookup"><span data-stu-id="e133f-101">New-AzPeering</span></span>

## <span data-ttu-id="e133f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e133f-102">SYNOPSIS</span></span>
<span data-ttu-id="e133f-103">Cria um novo recurso de emparelhamento em pontos</span><span class="sxs-lookup"><span data-stu-id="e133f-103">Creates a new Peering ARM Resource</span></span>

## <span data-ttu-id="e133f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e133f-104">SYNTAX</span></span>

### <span data-ttu-id="e133f-105">Exchange (padrão)</span><span class="sxs-lookup"><span data-stu-id="e133f-105">Exchange (Default)</span></span>
```
New-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-PeeringLocation] <String>
 [-PeerAsnResourceId] <String> -ExchangeConnection <PSExchangeConnection[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e133f-106">ConvertLegacyPeering</span><span class="sxs-lookup"><span data-stu-id="e133f-106">ConvertLegacyPeering</span></span>
```
New-AzPeering -InputObject <PSPeering> [-ResourceGroupName] <String> [-Name] <String>
 [-PeerAsnResourceId] <String> [-ExchangeConnection <PSExchangeConnection[]>]
 [-DirectConnection <PSDirectConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e133f-107">Orientar</span><span class="sxs-lookup"><span data-stu-id="e133f-107">Direct</span></span>
```
New-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-PeeringLocation] <String>
 [-PeerAsnResourceId] <String> -DirectConnection <PSDirectConnection[]> -Sku <String> [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e133f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e133f-108">DESCRIPTION</span></span>
<span data-ttu-id="e133f-109">Cria um emparelhamento de braço para a assinatura.</span><span class="sxs-lookup"><span data-stu-id="e133f-109">Creates an ARM Peering for the subscription.</span></span> <span data-ttu-id="e133f-110">Confira [New-AzPeeringDirectConnectionObject](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringdirectconnectionobject) ou [New-AzPeeringExchangeConnectionObject](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringexchangeconnectionobject) para obter mais informações sobre como criar um objeto de conexão.</span><span class="sxs-lookup"><span data-stu-id="e133f-110">See [New-AzPeeringDirectConnectionObject](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringdirectconnectionobject) or [New-AzPeeringExchangeConnectionObject](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringexchangeconnectionobject) for more information on creating a connection object.</span></span>

## <span data-ttu-id="e133f-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e133f-111">EXAMPLES</span></span>

### <span data-ttu-id="e133f-112">Criar uma nova correspondência direta</span><span class="sxs-lookup"><span data-stu-id="e133f-112">Create New Direct Peering</span></span>
```powershell
#Gets the ASN
PS C:> $asn = Get-AzPeerAsn -PeerName Contoso
#Gets the Direct Peering Location
PS C:> $location = Get-AzPeeringLocation Direct -PeeringLocation Seattle
#Creates the ARM Resource
PS C:> New-AzPeering -Name ContosoSeattlePeering -ResourceGroupName testCarrier -PeeringLocation $location.PeeringLocation -PeerAsnResourceId $asn.Id -DirectConnection $connection

Name                 : ContosoSeattlePeering
Sku.Name             : Basic_Direct_Free
Kind                 : Direct
Connections          : {99999}
PeerAsn.Id           : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
UseForPeeringService : False
PeeringLocation      : Seattle
ProvisioningState    : Succeeded
Location             : centralus
Id                   : /subscriptions//resourceGroups/testCarrier/providers/Microsoft.Peering/peerings/ContosoSeattlePeering
Type                 : Microsoft.Peering/peerings
Tags                 : {}
```

<span data-ttu-id="e133f-113">Crie uma nova correspondência direta com uma única conexão na instalação de Seattle usando o PeerAsn 65000</span><span class="sxs-lookup"><span data-stu-id="e133f-113">Create a new Direct Peering with a single connection at the Seattle facility using PeerAsn 65000</span></span>

### <span data-ttu-id="e133f-114">Criar nova troca de tráfego do Exchange</span><span class="sxs-lookup"><span data-stu-id="e133f-114">Create New Exchange Peering</span></span>
```powershell
#Gets the ASN
PS C:> $asn = Get-AzPeerAsn -PeerName Contoso
#Gets the Exchange Peering Location
PS C:> $location = Get-AzPeeringLocation Exchange -PeeringLocation Seattle
#Creates the ARM Resource
PS C:> New-AzPeering -Name ContosoSeattlePeering -ResourceGroupName testCarrier -PeeringLocation $location.PeeringLocation -PeerAsnResourceId $asn.Id -ExchangeConnection $connection

Name              : myExchangePeering1
Sku.Name          : Basic_Exchange_Free
Kind              : Exchange
Connections       : {99999}
PeerAsn.Id        : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
PeeringLocation   : Seattle
ProvisioningState : Succeeded
Location          : centralus
Id                : /subscriptions//resourceGroups/test/providers/Microsoft.Peering/peerings/myExchangePeering1
Type              : Microsoft.Peering/peerings
Tags              : {}
```

<span data-ttu-id="e133f-115">Criar um novo emparelhamento do Exchange</span><span class="sxs-lookup"><span data-stu-id="e133f-115">Create a new exchange peering</span></span>

### <span data-ttu-id="e133f-116">Converter emparelhamento herdado para emparelhamento por braço</span><span class="sxs-lookup"><span data-stu-id="e133f-116">Convert Legacy Peering to ARM Peering</span></span>
```powershell
#Gets the ASN
PS C:> $asn = Get-AzPeerAsn -PeerName Contoso
#Gets the legacy Peering
PS C:> $legacy = Get-AzLegacyPeering -PeeringLocation Amsterdam -Kind Direct | New-AzPeering -Name ContosoAmsterdamPeering -ResourceGroupName testCarrier -PeeringLocation $location.PeeringLocation -PeerAsnResourceId $asn.Id

Name              : ContosoAmsterdamPeering
Sku.Name          : Basic_Direct_Free
Kind              : Direct
Connections       : {64}
PeerAsn.Id        : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
PeeringLocation   : Seattle
ProvisioningState : Succeeded
Location          : centralus
Id                : /subscriptions//resourceGroups/test/providers/Microsoft.Peering/peerings/ContosoAmsterdamPeering
Type              : Microsoft.Peering/peerings
Tags              : {}
```

## <span data-ttu-id="e133f-117">OS</span><span class="sxs-lookup"><span data-stu-id="e133f-117">PARAMETERS</span></span>

### <span data-ttu-id="e133f-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e133f-118">-AsJob</span></span>
<span data-ttu-id="e133f-119">Executar em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="e133f-119">Run in the background.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e133f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e133f-120">-DefaultProfile</span></span>
<span data-ttu-id="e133f-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e133f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e133f-122">-DirectConnection</span><span class="sxs-lookup"><span data-stu-id="e133f-122">-DirectConnection</span></span>
<span data-ttu-id="e133f-123">Crie uma nova conexão direta usando o New-AzExchangePeeringConnection e o pipe para esse comando.</span><span class="sxs-lookup"><span data-stu-id="e133f-123">Create a new Direct connections using the New-AzExchangePeeringConnection and pipe to this command.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection[]
Parameter Sets: ConvertLegacyPeering
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection[]
Parameter Sets: Direct
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e133f-124">-ExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="e133f-124">-ExchangeConnection</span></span>
<span data-ttu-id="e133f-125">Crie uma nova conexão do Exchange usando o New-AzExchangePeeringConnection e o pipe para esse comando.</span><span class="sxs-lookup"><span data-stu-id="e133f-125">Create a new Exchange connections using the New-AzExchangePeeringConnection and pipe to this command.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection[]
Parameter Sets: Exchange
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection[]
Parameter Sets: ConvertLegacyPeering
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e133f-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e133f-126">-InputObject</span></span>
<span data-ttu-id="e133f-127">Use Get-AzLegacyPeering para recuperar esse objeto.</span><span class="sxs-lookup"><span data-stu-id="e133f-127">Use Get-AzLegacyPeering to retrieve this object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: ConvertLegacyPeering
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e133f-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="e133f-128">-Name</span></span>
<span data-ttu-id="e133f-129">O nome exclusivo da PSPeering.</span><span class="sxs-lookup"><span data-stu-id="e133f-129">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e133f-130">-PeerAsnResourceId</span><span class="sxs-lookup"><span data-stu-id="e133f-130">-PeerAsnResourceId</span></span>
<span data-ttu-id="e133f-131">A ID do recurso ASN de par. Use Get-AzPeerAsn para recuperar a ID.</span><span class="sxs-lookup"><span data-stu-id="e133f-131">The Peer Asn Resource Id. Use Get-AzPeerAsn to retrieve the Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e133f-132">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="e133f-132">-PeeringLocation</span></span>
<span data-ttu-id="e133f-133">A localização física é diferente da região do Azure.</span><span class="sxs-lookup"><span data-stu-id="e133f-133">The Physical Location Different from Azure Region.</span></span>
<span data-ttu-id="e133f-134">Use o tipo de Get-AzPeeringLocation de tipo \< \> usar nome da cidade como chave.</span><span class="sxs-lookup"><span data-stu-id="e133f-134">Use Get-AzPeeringLocation -Kind \<kind\> use City name as key.</span></span>

```yaml
Type: System.String
Parameter Sets: Exchange, Direct
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e133f-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e133f-135">-ResourceGroupName</span></span>
<span data-ttu-id="e133f-136">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e133f-136">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e133f-137">-SKU</span><span class="sxs-lookup"><span data-stu-id="e133f-137">-Sku</span></span>
<span data-ttu-id="e133f-138">Selecione Basic_Direct_Free ou Premium_Direct_Free, a menos que explicitamente solicitado a selecionar outra opção.</span><span class="sxs-lookup"><span data-stu-id="e133f-138">Select Basic_Direct_Free or Premium_Direct_Free unless explicitly told to select another option.</span></span>

```yaml
Type: System.String
Parameter Sets: Direct
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e133f-139">-Marca</span><span class="sxs-lookup"><span data-stu-id="e133f-139">-Tag</span></span>
<span data-ttu-id="e133f-140">As marcas a serem associadas ao serviço de emparelhamento da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e133f-140">The tags to associate with the Microsoft Peering Service.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e133f-141">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e133f-141">-Confirm</span></span>
<span data-ttu-id="e133f-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e133f-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e133f-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e133f-143">-WhatIf</span></span>
<span data-ttu-id="e133f-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e133f-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e133f-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e133f-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e133f-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e133f-146">CommonParameters</span></span>
<span data-ttu-id="e133f-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e133f-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e133f-148">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e133f-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e133f-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e133f-149">INPUTS</span></span>

### <span data-ttu-id="e133f-150">Microsoft. Azure. PowerShell. cmdlets. peering. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="e133f-150">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="e133f-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e133f-151">OUTPUTS</span></span>

### <span data-ttu-id="e133f-152">Microsoft. Azure. PowerShell. cmdlets. peering. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="e133f-152">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="e133f-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e133f-153">NOTES</span></span>

## <span data-ttu-id="e133f-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e133f-154">RELATED LINKS</span></span>
