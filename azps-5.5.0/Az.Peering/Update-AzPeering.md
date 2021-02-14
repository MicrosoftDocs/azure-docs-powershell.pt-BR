---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/update-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Update-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Update-AzPeering.md
ms.openlocfilehash: 0f757c6bbde541876a3b4889f300a8d18e1cf113
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117275"
---
# <span data-ttu-id="2d072-101">Update-AzPeering</span><span class="sxs-lookup"><span data-stu-id="2d072-101">Update-AzPeering</span></span>

## <span data-ttu-id="2d072-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2d072-102">SYNOPSIS</span></span>
<span data-ttu-id="2d072-103">Define o Peering.</span><span class="sxs-lookup"><span data-stu-id="2d072-103">Sets the Peering.</span></span> <span data-ttu-id="2d072-104">Use este Comando em conjunto com `Set-AzDirectPeeringConnectionObject` ou `Set-AzExchangePeeringConnectionObject` .</span><span class="sxs-lookup"><span data-stu-id="2d072-104">Use this Command in conjunction with `Set-AzDirectPeeringConnectionObject` or `Set-AzExchangePeeringConnectionObject`.</span></span>

## <span data-ttu-id="2d072-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2d072-105">SYNTAX</span></span>

### <span data-ttu-id="2d072-106">DefaultExchange (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2d072-106">DefaultExchange (Default)</span></span>
```
Update-AzPeering -InputObject <PSPeering> [[-ExchangeConnection] <PSExchangeConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d072-107">DefaultDirect</span><span class="sxs-lookup"><span data-stu-id="2d072-107">DefaultDirect</span></span>
```
Update-AzPeering -InputObject <PSPeering> [-DirectConnection <PSDirectConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d072-108">ByResourceIdDirect</span><span class="sxs-lookup"><span data-stu-id="2d072-108">ByResourceIdDirect</span></span>
```
Update-AzPeering -ResourceId <String> [-DirectConnection <PSDirectConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d072-109">ByResourceIdExchange</span><span class="sxs-lookup"><span data-stu-id="2d072-109">ByResourceIdExchange</span></span>
```
Update-AzPeering -ResourceId <String> [-ExchangeConnection] <PSExchangeConnection[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d072-110">Direto</span><span class="sxs-lookup"><span data-stu-id="2d072-110">Direct</span></span>
```
Update-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-DirectConnection <PSDirectConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d072-111">Exchange</span><span class="sxs-lookup"><span data-stu-id="2d072-111">Exchange</span></span>
```
Update-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-ExchangeConnection] <PSExchangeConnection[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d072-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="2d072-112">DESCRIPTION</span></span>
<span data-ttu-id="2d072-113">Define o Objeto PSPeering</span><span class="sxs-lookup"><span data-stu-id="2d072-113">Sets the PSPeering Object</span></span>

## <span data-ttu-id="2d072-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2d072-114">EXAMPLES</span></span>

### <span data-ttu-id="2d072-115">Atualizar chave de autenticação Md5</span><span class="sxs-lookup"><span data-stu-id="2d072-115">Update Md5 Authentication Key</span></span>
```powershell
PS C:> $peering = Get-AzPeering -ResourceGroupName rg1 -PeerName "ContosoPeering"  
PS C:> $peering.Connections[0] = $peering.Connections[0] | Set-AzPeeringDirectConnectionObject -MD5AuthenticationKey $hash
PS C:> $peering | Update-AzPeering
```

<span data-ttu-id="2d072-116">Define a Chave de Autenticação Md5</span><span class="sxs-lookup"><span data-stu-id="2d072-116">Sets the Md5 Authentication Key</span></span>

### <span data-ttu-id="2d072-117">Atualizar UseForPeeringService</span><span class="sxs-lookup"><span data-stu-id="2d072-117">Update UseForPeeringService</span></span>
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

<span data-ttu-id="2d072-118">Define o Sinalizador de Serviço de Uso para Pares</span><span class="sxs-lookup"><span data-stu-id="2d072-118">Sets the Use for Peering Service Flag</span></span>

### <span data-ttu-id="2d072-119">Atualizar Endereço IPv4 para o Peering do Exchange</span><span class="sxs-lookup"><span data-stu-id="2d072-119">Update IPv4 Address for Exchange Peering</span></span>
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

<span data-ttu-id="2d072-120">Define o Endereço Ipv4 para um Peering do Exchange usando ResourceId</span><span class="sxs-lookup"><span data-stu-id="2d072-120">Sets the Ipv4 Address for an Exchange Peering using ResourceId</span></span>

## <span data-ttu-id="2d072-121">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2d072-121">PARAMETERS</span></span>

### <span data-ttu-id="2d072-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d072-122">-DefaultProfile</span></span>
<span data-ttu-id="2d072-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2d072-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d072-124">-DirectConnection</span><span class="sxs-lookup"><span data-stu-id="2d072-124">-DirectConnection</span></span>
<span data-ttu-id="2d072-125">Crie uma nova conexão direta usando o New-AzDirectPeeringConnectionObject e o cano para esse comando.</span><span class="sxs-lookup"><span data-stu-id="2d072-125">Create a new Direct connections using the New-AzDirectPeeringConnectionObject and pipe to this command.</span></span>

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

### <span data-ttu-id="2d072-126">-ExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="2d072-126">-ExchangeConnection</span></span>
<span data-ttu-id="2d072-127">Crie uma nova conexão do Exchange usando o New-AzExchangePeeringConnectionObject e o cano para esse comando.</span><span class="sxs-lookup"><span data-stu-id="2d072-127">Create a new Exchange connection using the New-AzExchangePeeringConnectionObject and pipe to this command.</span></span>

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

### <span data-ttu-id="2d072-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2d072-128">-InputObject</span></span>
<span data-ttu-id="2d072-129">O objeto Peering</span><span class="sxs-lookup"><span data-stu-id="2d072-129">The Peering object</span></span> 

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

### <span data-ttu-id="2d072-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="2d072-130">-Name</span></span>
<span data-ttu-id="2d072-131">O nome exclusivo do PSPeering.</span><span class="sxs-lookup"><span data-stu-id="2d072-131">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="2d072-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d072-132">-ResourceGroupName</span></span>
<span data-ttu-id="2d072-133">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2d072-133">The resource group name.</span></span>

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

### <span data-ttu-id="2d072-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2d072-134">-ResourceId</span></span>
<span data-ttu-id="2d072-135">O nome da cadeia de caracteres de ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="2d072-135">The resource id string name.</span></span>

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

### <span data-ttu-id="2d072-136">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="2d072-136">-Confirm</span></span>
<span data-ttu-id="2d072-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d072-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d072-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d072-138">-WhatIf</span></span>
<span data-ttu-id="2d072-139">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="2d072-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d072-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2d072-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d072-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d072-141">CommonParameters</span></span>
<span data-ttu-id="2d072-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d072-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d072-143">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2d072-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d072-144">Entradas</span><span class="sxs-lookup"><span data-stu-id="2d072-144">INPUTS</span></span>

### <span data-ttu-id="2d072-145">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="2d072-145">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="2d072-146">System.String</span><span class="sxs-lookup"><span data-stu-id="2d072-146">System.String</span></span>

## <span data-ttu-id="2d072-147">Saídas</span><span class="sxs-lookup"><span data-stu-id="2d072-147">OUTPUTS</span></span>

### <span data-ttu-id="2d072-148">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="2d072-148">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="2d072-149">Notas</span><span class="sxs-lookup"><span data-stu-id="2d072-149">NOTES</span></span>

## <span data-ttu-id="2d072-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2d072-150">RELATED LINKS</span></span>
