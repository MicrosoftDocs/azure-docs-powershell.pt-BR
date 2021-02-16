---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeering.md
ms.openlocfilehash: 41880f4d3e6a0f7cea67e60853d8309c9377d494
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113389"
---
# <span data-ttu-id="a8071-101">New-AzPeering</span><span class="sxs-lookup"><span data-stu-id="a8071-101">New-AzPeering</span></span>

## <span data-ttu-id="a8071-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a8071-102">SYNOPSIS</span></span>
<span data-ttu-id="a8071-103">Cria um novo Recurso ARM de Peering</span><span class="sxs-lookup"><span data-stu-id="a8071-103">Creates a new Peering ARM Resource</span></span>

## <span data-ttu-id="a8071-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a8071-104">SYNTAX</span></span>

### <span data-ttu-id="a8071-105">Exchange (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a8071-105">Exchange (Default)</span></span>
```
New-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-PeeringLocation] <String>
 [-PeerAsnResourceId] <String> -ExchangeConnection <PSExchangeConnection[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8071-106">ConvertLegacyPeering</span><span class="sxs-lookup"><span data-stu-id="a8071-106">ConvertLegacyPeering</span></span>
```
New-AzPeering -InputObject <PSPeering> [-ResourceGroupName] <String> [-Name] <String>
 [-PeerAsnResourceId] <String> [-ExchangeConnection <PSExchangeConnection[]>]
 [-DirectConnection <PSDirectConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8071-107">Direto</span><span class="sxs-lookup"><span data-stu-id="a8071-107">Direct</span></span>
```
New-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-PeeringLocation] <String>
 -MicrosoftNetwork <String> [-PeerAsnResourceId] <String> -DirectConnection <PSDirectConnection[]>
 -Sku <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a8071-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="a8071-108">DESCRIPTION</span></span>
<span data-ttu-id="a8071-109">Cria um Peering ARM para a assinatura.</span><span class="sxs-lookup"><span data-stu-id="a8071-109">Creates an ARM Peering for the subscription.</span></span> <span data-ttu-id="a8071-110">Consulte [New-AzPeeringDirectConnectionObject](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringdirectconnectionobject) [ou New-AzPeeringExchangeConnectionObject](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringexchangeconnectionobject) para obter mais informações sobre como criar um objeto de conexão.</span><span class="sxs-lookup"><span data-stu-id="a8071-110">See [New-AzPeeringDirectConnectionObject](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringdirectconnectionobject) or [New-AzPeeringExchangeConnectionObject](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringexchangeconnectionobject) for more information on creating a connection object.</span></span>

## <span data-ttu-id="a8071-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a8071-111">EXAMPLES</span></span>

### <span data-ttu-id="a8071-112">Criar novo peering direto</span><span class="sxs-lookup"><span data-stu-id="a8071-112">Create New Direct Peering</span></span>
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

<span data-ttu-id="a8071-113">Criar um novo Peering Direto com uma única conexão na instalação de Seattle usando o PeerAsn 65000</span><span class="sxs-lookup"><span data-stu-id="a8071-113">Create a new Direct Peering with a single connection at the Seattle facility using PeerAsn 65000</span></span>

### <span data-ttu-id="a8071-114">Criar novo paridade do Exchange</span><span class="sxs-lookup"><span data-stu-id="a8071-114">Create New Exchange Peering</span></span>
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

<span data-ttu-id="a8071-115">Criar um novo par de troca</span><span class="sxs-lookup"><span data-stu-id="a8071-115">Create a new exchange peering</span></span>

### <span data-ttu-id="a8071-116">Converter o Parênte Herdado em Parênte ARM</span><span class="sxs-lookup"><span data-stu-id="a8071-116">Convert Legacy Peering to ARM Peering</span></span>
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

## <span data-ttu-id="a8071-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a8071-117">PARAMETERS</span></span>

### <span data-ttu-id="a8071-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a8071-118">-AsJob</span></span>
<span data-ttu-id="a8071-119">Executar em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="a8071-119">Run in the background.</span></span>

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

### <span data-ttu-id="a8071-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8071-120">-DefaultProfile</span></span>
<span data-ttu-id="a8071-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a8071-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8071-122">-DirectConnection</span><span class="sxs-lookup"><span data-stu-id="a8071-122">-DirectConnection</span></span>
<span data-ttu-id="a8071-123">Crie uma nova conexão direta usando o New-AzExchangePeeringConnection e o cano para esse comando.</span><span class="sxs-lookup"><span data-stu-id="a8071-123">Create a new Direct connections using the New-AzExchangePeeringConnection and pipe to this command.</span></span>

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

### <span data-ttu-id="a8071-124">-ExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="a8071-124">-ExchangeConnection</span></span>
<span data-ttu-id="a8071-125">Crie uma nova conexões do Exchange usando o New-AzExchangePeeringConnection e o cano para esse comando.</span><span class="sxs-lookup"><span data-stu-id="a8071-125">Create a new Exchange connections using the New-AzExchangePeeringConnection and pipe to this command.</span></span>

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

### <span data-ttu-id="a8071-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a8071-126">-InputObject</span></span>
<span data-ttu-id="a8071-127">Use Get-AzLegacyPeering para recuperar este objeto.</span><span class="sxs-lookup"><span data-stu-id="a8071-127">Use Get-AzLegacyPeering to retrieve this object.</span></span>

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

### <span data-ttu-id="a8071-128">-MicrosoftNetwork</span><span class="sxs-lookup"><span data-stu-id="a8071-128">-MicrosoftNetwork</span></span>
<span data-ttu-id="a8071-129">Selecione a rede da Microsoft com a que você deseja fazer o mesmo.</span><span class="sxs-lookup"><span data-stu-id="a8071-129">Select the Microsoft network you want to peer with.</span></span>

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

### <span data-ttu-id="a8071-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="a8071-130">-Name</span></span>
<span data-ttu-id="a8071-131">O nome exclusivo do PSPeering.</span><span class="sxs-lookup"><span data-stu-id="a8071-131">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="a8071-132">-PeerAsnResourceId</span><span class="sxs-lookup"><span data-stu-id="a8071-132">-PeerAsnResourceId</span></span>
<span data-ttu-id="a8071-133">A ID do Recurso peer asn. Use Get-AzPeerAsn para recuperar a ID.</span><span class="sxs-lookup"><span data-stu-id="a8071-133">The Peer Asn Resource Id. Use Get-AzPeerAsn to retrieve the Id.</span></span>

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

### <span data-ttu-id="a8071-134">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="a8071-134">-PeeringLocation</span></span>
<span data-ttu-id="a8071-135">A Localização Física Diferente da Região do Azure.</span><span class="sxs-lookup"><span data-stu-id="a8071-135">The Physical Location Different from Azure Region.</span></span>
<span data-ttu-id="a8071-136">Use Get-AzPeeringLocation -Kind \<kind\> use o nome cidade como chave.</span><span class="sxs-lookup"><span data-stu-id="a8071-136">Use Get-AzPeeringLocation -Kind \<kind\> use City name as key.</span></span>

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

### <span data-ttu-id="a8071-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8071-137">-ResourceGroupName</span></span>
<span data-ttu-id="a8071-138">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a8071-138">The resource group name.</span></span>

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

### <span data-ttu-id="a8071-139">-SKU</span><span class="sxs-lookup"><span data-stu-id="a8071-139">-Sku</span></span>
<span data-ttu-id="a8071-140">Selecione Basic_Direct_Free ou Premium_Direct_Free, a menos que seja explicitamente dito para selecionar outra opção.</span><span class="sxs-lookup"><span data-stu-id="a8071-140">Select Basic_Direct_Free or Premium_Direct_Free unless explicitly told to select another option.</span></span>

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

### <span data-ttu-id="a8071-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="a8071-141">-Tag</span></span>
<span data-ttu-id="a8071-142">As marcas a associar ao Serviço de Peering da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a8071-142">The tags to associate with the Microsoft Peering Service.</span></span>

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

### <span data-ttu-id="a8071-143">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="a8071-143">-Confirm</span></span>
<span data-ttu-id="a8071-144">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8071-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8071-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8071-145">-WhatIf</span></span>
<span data-ttu-id="a8071-146">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="a8071-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a8071-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a8071-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8071-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8071-148">CommonParameters</span></span>
<span data-ttu-id="a8071-149">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8071-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8071-150">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a8071-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8071-151">Entradas</span><span class="sxs-lookup"><span data-stu-id="a8071-151">INPUTS</span></span>

### <span data-ttu-id="a8071-152">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="a8071-152">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="a8071-153">Saídas</span><span class="sxs-lookup"><span data-stu-id="a8071-153">OUTPUTS</span></span>

### <span data-ttu-id="a8071-154">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="a8071-154">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="a8071-155">Notas</span><span class="sxs-lookup"><span data-stu-id="a8071-155">NOTES</span></span>

## <span data-ttu-id="a8071-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a8071-156">RELATED LINKS</span></span>
