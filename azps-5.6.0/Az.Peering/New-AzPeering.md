---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/new-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeering.md
ms.openlocfilehash: d8ef4378ed0032012a64d015855ca0287d608a6a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890157"
---
# <span data-ttu-id="e8ba8-101">New-AzPeering</span><span class="sxs-lookup"><span data-stu-id="e8ba8-101">New-AzPeering</span></span>

## <span data-ttu-id="e8ba8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8ba8-102">SYNOPSIS</span></span>
<span data-ttu-id="e8ba8-103">Cria um novo recurso ARM Peering</span><span class="sxs-lookup"><span data-stu-id="e8ba8-103">Creates a new Peering ARM Resource</span></span>

## <span data-ttu-id="e8ba8-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e8ba8-104">SYNTAX</span></span>

### <span data-ttu-id="e8ba8-105">Exchange (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e8ba8-105">Exchange (Default)</span></span>
```
New-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-PeeringLocation] <String>
 [-PeerAsnResourceId] <String> -ExchangeConnection <PSExchangeConnection[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8ba8-106">ConvertLegacyPeering</span><span class="sxs-lookup"><span data-stu-id="e8ba8-106">ConvertLegacyPeering</span></span>
```
New-AzPeering -InputObject <PSPeering> [-ResourceGroupName] <String> [-Name] <String>
 [-PeerAsnResourceId] <String> [-ExchangeConnection <PSExchangeConnection[]>]
 [-DirectConnection <PSDirectConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8ba8-107">Direct</span><span class="sxs-lookup"><span data-stu-id="e8ba8-107">Direct</span></span>
```
New-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-PeeringLocation] <String>
 -MicrosoftNetwork <String> [-PeerAsnResourceId] <String> -DirectConnection <PSDirectConnection[]>
 -Sku <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e8ba8-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e8ba8-108">DESCRIPTION</span></span>
<span data-ttu-id="e8ba8-109">Cria um ARM de paração para a assinatura.</span><span class="sxs-lookup"><span data-stu-id="e8ba8-109">Creates an ARM Peering for the subscription.</span></span> <span data-ttu-id="e8ba8-110">Consulte [New-AzPeeringDirectConnectionObject](https://docs.microsoft.com/powershell/module/az.peering/new-azpeeringdirectconnectionobject) ou [New-AzPeeringExchangeConnectionObject](https://docs.microsoft.com/powershell/module/az.peering/new-azpeeringexchangeconnectionobject) para obter mais informações sobre como criar um objeto connection.</span><span class="sxs-lookup"><span data-stu-id="e8ba8-110">See [New-AzPeeringDirectConnectionObject](https://docs.microsoft.com/powershell/module/az.peering/new-azpeeringdirectconnectionobject) or [New-AzPeeringExchangeConnectionObject](https://docs.microsoft.com/powershell/module/az.peering/new-azpeeringexchangeconnectionobject) for more information on creating a connection object.</span></span>

## <span data-ttu-id="e8ba8-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e8ba8-111">EXAMPLES</span></span>

### <span data-ttu-id="e8ba8-112">Criar novo peering direto</span><span class="sxs-lookup"><span data-stu-id="e8ba8-112">Create New Direct Peering</span></span>
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

<span data-ttu-id="e8ba8-113">Criar um novo Direct Peering com uma única conexão nas instalações de Seattle usando PeerAsn 65000</span><span class="sxs-lookup"><span data-stu-id="e8ba8-113">Create a new Direct Peering with a single connection at the Seattle facility using PeerAsn 65000</span></span>

### <span data-ttu-id="e8ba8-114">Criar Novo Paring do Exchange</span><span class="sxs-lookup"><span data-stu-id="e8ba8-114">Create New Exchange Peering</span></span>
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

<span data-ttu-id="e8ba8-115">Criar um novo par de exchange</span><span class="sxs-lookup"><span data-stu-id="e8ba8-115">Create a new exchange peering</span></span>

### <span data-ttu-id="e8ba8-116">Converter o paramento herddo em ARM paração</span><span class="sxs-lookup"><span data-stu-id="e8ba8-116">Convert Legacy Peering to ARM Peering</span></span>
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

## <span data-ttu-id="e8ba8-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e8ba8-117">PARAMETERS</span></span>

### <span data-ttu-id="e8ba8-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e8ba8-118">-AsJob</span></span>
<span data-ttu-id="e8ba8-119">Execute em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="e8ba8-119">Run in the background.</span></span>

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

### <span data-ttu-id="e8ba8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8ba8-120">-DefaultProfile</span></span>
<span data-ttu-id="e8ba8-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e8ba8-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8ba8-122">-DirectConnection</span><span class="sxs-lookup"><span data-stu-id="e8ba8-122">-DirectConnection</span></span>
<span data-ttu-id="e8ba8-123">Crie uma nova conexão Direta usando o New-AzExchangePeeringConnection e canal para esse comando.</span><span class="sxs-lookup"><span data-stu-id="e8ba8-123">Create a new Direct connections using the New-AzExchangePeeringConnection and pipe to this command.</span></span>

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

### <span data-ttu-id="e8ba8-124">-ExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="e8ba8-124">-ExchangeConnection</span></span>
<span data-ttu-id="e8ba8-125">Crie uma nova conexão do Exchange usando o New-AzExchangePeeringConnection e canal para este comando.</span><span class="sxs-lookup"><span data-stu-id="e8ba8-125">Create a new Exchange connections using the New-AzExchangePeeringConnection and pipe to this command.</span></span>

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

### <span data-ttu-id="e8ba8-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e8ba8-126">-InputObject</span></span>
<span data-ttu-id="e8ba8-127">Use Get-AzLegacyPeering para recuperar esse objeto.</span><span class="sxs-lookup"><span data-stu-id="e8ba8-127">Use Get-AzLegacyPeering to retrieve this object.</span></span>

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

### <span data-ttu-id="e8ba8-128">-MicrosoftNetwork</span><span class="sxs-lookup"><span data-stu-id="e8ba8-128">-MicrosoftNetwork</span></span>
<span data-ttu-id="e8ba8-129">Selecione a rede da Microsoft com a que você deseja fazer par.</span><span class="sxs-lookup"><span data-stu-id="e8ba8-129">Select the Microsoft network you want to peer with.</span></span>

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

### <span data-ttu-id="e8ba8-130">-Name</span><span class="sxs-lookup"><span data-stu-id="e8ba8-130">-Name</span></span>
<span data-ttu-id="e8ba8-131">O nome exclusivo do PSPeering.</span><span class="sxs-lookup"><span data-stu-id="e8ba8-131">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="e8ba8-132">-PeerAsnResourceId</span><span class="sxs-lookup"><span data-stu-id="e8ba8-132">-PeerAsnResourceId</span></span>
<span data-ttu-id="e8ba8-133">A ID de Recurso de Asn Par. Use Get-AzPeerAsn recuperar a Id.</span><span class="sxs-lookup"><span data-stu-id="e8ba8-133">The Peer Asn Resource Id. Use Get-AzPeerAsn to retrieve the Id.</span></span>

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

### <span data-ttu-id="e8ba8-134">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="e8ba8-134">-PeeringLocation</span></span>
<span data-ttu-id="e8ba8-135">A localização física diferente da região do Azure.</span><span class="sxs-lookup"><span data-stu-id="e8ba8-135">The Physical Location Different from Azure Region.</span></span>
<span data-ttu-id="e8ba8-136">Use Get-AzPeeringLocation -Kind \<kind\> use City name como chave.</span><span class="sxs-lookup"><span data-stu-id="e8ba8-136">Use Get-AzPeeringLocation -Kind \<kind\> use City name as key.</span></span>

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

### <span data-ttu-id="e8ba8-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8ba8-137">-ResourceGroupName</span></span>
<span data-ttu-id="e8ba8-138">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e8ba8-138">The resource group name.</span></span>

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

### <span data-ttu-id="e8ba8-139">-Sku</span><span class="sxs-lookup"><span data-stu-id="e8ba8-139">-Sku</span></span>
<span data-ttu-id="e8ba8-140">Selecione Basic_Direct_Free ou Premium_Direct_Free, a menos que seja explicitamente dito para selecionar outra opção.</span><span class="sxs-lookup"><span data-stu-id="e8ba8-140">Select Basic_Direct_Free or Premium_Direct_Free unless explicitly told to select another option.</span></span>

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

### <span data-ttu-id="e8ba8-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="e8ba8-141">-Tag</span></span>
<span data-ttu-id="e8ba8-142">As marcas a ser associadas ao Serviço de Peering da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e8ba8-142">The tags to associate with the Microsoft Peering Service.</span></span>

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

### <span data-ttu-id="e8ba8-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e8ba8-143">-Confirm</span></span>
<span data-ttu-id="e8ba8-144">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8ba8-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8ba8-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8ba8-145">-WhatIf</span></span>
<span data-ttu-id="e8ba8-146">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e8ba8-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e8ba8-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e8ba8-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8ba8-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8ba8-148">CommonParameters</span></span>
<span data-ttu-id="e8ba8-149">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8ba8-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8ba8-150">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e8ba8-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8ba8-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e8ba8-151">INPUTS</span></span>

### <span data-ttu-id="e8ba8-152">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="e8ba8-152">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="e8ba8-153">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e8ba8-153">OUTPUTS</span></span>

### <span data-ttu-id="e8ba8-154">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="e8ba8-154">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="e8ba8-155">NOTES</span><span class="sxs-lookup"><span data-stu-id="e8ba8-155">NOTES</span></span>

## <span data-ttu-id="e8ba8-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e8ba8-156">RELATED LINKS</span></span>
