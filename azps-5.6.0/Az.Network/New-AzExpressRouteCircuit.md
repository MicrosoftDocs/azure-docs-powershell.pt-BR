---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E40CAF2F-ED57-4AC1-8B9A-E48042DD8F91
online version: https://docs.microsoft.com/powershell/module/az.network/new-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuit.md
ms.openlocfilehash: af552e1320d9a935255d3649648ac103cfc08756
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890242"
---
# <span data-ttu-id="3c6dc-101">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3c6dc-101">New-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="3c6dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c6dc-102">SYNOPSIS</span></span>
<span data-ttu-id="3c6dc-103">Cria um circuito de rota expressa do Azure.</span><span class="sxs-lookup"><span data-stu-id="3c6dc-103">Creates an Azure express route circuit.</span></span>

## <span data-ttu-id="3c6dc-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3c6dc-104">SYNTAX</span></span>

### <span data-ttu-id="3c6dc-105">ServiceProvider (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3c6dc-105">ServiceProvider (Default)</span></span>
```
New-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String> [-SkuTier <String>]
 [-SkuFamily <String>] -ServiceProviderName <String> -PeeringLocation <String> -BandwidthInMbps <Int32>
 [-Peering <PSPeering[]>] [-Authorization <PSExpressRouteCircuitAuthorization[]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c6dc-106">ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="3c6dc-106">ExpressRoutePort</span></span>
```
New-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String> [-SkuTier <String>]
 [-SkuFamily <String>] -ExpressRoutePort <PSExpressRoutePort> -BandwidthInGbps <Double>
 [-Peering <PSPeering[]>] [-Authorization <PSExpressRouteCircuitAuthorization[]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c6dc-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3c6dc-107">DESCRIPTION</span></span>
<span data-ttu-id="3c6dc-108">O cmdlet **New-AzExpressRouteCircuit** cria um circuito de rota expressa do Azure.</span><span class="sxs-lookup"><span data-stu-id="3c6dc-108">The **New-AzExpressRouteCircuit** cmdlet creates an Azure express route circuit.</span></span>

## <span data-ttu-id="3c6dc-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3c6dc-109">EXAMPLES</span></span>

### <span data-ttu-id="3c6dc-110">Exemplo 1: Criar um novo circuito ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="3c6dc-110">Example 1: Create a new ExpressRoute circuit</span></span>
```powershell
$parameters = @{
    Name='ExpressRouteCircuit'
    ResourceGroupName='ExpressRouteResourceGroup'
    Location='West US'
    SkuTier='Standard'
    SkuFamily='MeteredData'
    ServiceProviderName='Equinix'
    PeeringLocation='Silicon Valley'
    BandwidthInMbps=200
}
New-AzExpressRouteCircuit @parameters
```

### <span data-ttu-id="3c6dc-111">Exemplo 2: Criar um novo circuito ExpressRoute no ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="3c6dc-111">Example 2: Create a new ExpressRoute circuit on ExpressRoutePort</span></span>
```powershell
$parameters = @{
    Name='ExpressRouteCircuit'
    ResourceGroupName='ExpressRouteResourceGroup'
    Location='West US'
    SkuTier='Standard'
    SkuFamily='MeteredData'
    ExpressRoutePort=$PSExpressRoutePort
    BandwidthInGbps=10.0
}
New-AzExpressRouteCircuit @parameters
```

## <span data-ttu-id="3c6dc-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3c6dc-112">PARAMETERS</span></span>

### <span data-ttu-id="3c6dc-113">-AllowClassicOperations</span><span class="sxs-lookup"><span data-stu-id="3c6dc-113">-AllowClassicOperations</span></span>
<span data-ttu-id="3c6dc-114">O uso desse parâmetro permite que você use os cmdlets clássicos do Azure PowerShell para gerenciar o circuito.</span><span class="sxs-lookup"><span data-stu-id="3c6dc-114">The use of this parameter allows you to use the classic Azure PowerShell cmdlets to manage the circuit.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c6dc-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3c6dc-115">-AsJob</span></span>
<span data-ttu-id="3c6dc-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="3c6dc-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3c6dc-117">-Authorization</span><span class="sxs-lookup"><span data-stu-id="3c6dc-117">-Authorization</span></span>
<span data-ttu-id="3c6dc-118">Uma lista de autorizações de circuitos.</span><span class="sxs-lookup"><span data-stu-id="3c6dc-118">A list of circuit authorizations.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c6dc-119">-BandwidthInGbps</span><span class="sxs-lookup"><span data-stu-id="3c6dc-119">-BandwidthInGbps</span></span>
<span data-ttu-id="3c6dc-120">A largura de banda do circuito quando o circuito é provisionado em um recurso ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="3c6dc-120">The bandwidth of the circuit when the circuit is provisioned on an ExpressRoutePort resource.</span></span>

```yaml
Type: System.Double
Parameter Sets: ExpressRoutePort
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c6dc-121">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="3c6dc-121">-BandwidthInMbps</span></span>
<span data-ttu-id="3c6dc-122">A largura de banda do circuito.</span><span class="sxs-lookup"><span data-stu-id="3c6dc-122">The bandwidth of the circuit.</span></span> <span data-ttu-id="3c6dc-123">Esse deve ser um valor suportado pelo provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="3c6dc-123">This must be a value that is supported by the service provider.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ServiceProvider
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c6dc-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c6dc-124">-DefaultProfile</span></span>
<span data-ttu-id="3c6dc-125">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="3c6dc-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c6dc-126">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="3c6dc-126">-ExpressRoutePort</span></span>
<span data-ttu-id="3c6dc-127">A referência ao recurso ExpressRoutePort quando o circuito é provisionado em um recurso ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="3c6dc-127">The reference to the ExpressRoutePort resource when the circuit is provisioned on an ExpressRoutePort resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: ExpressRoutePort
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c6dc-128">-Force</span><span class="sxs-lookup"><span data-stu-id="3c6dc-128">-Force</span></span>
<span data-ttu-id="3c6dc-129">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="3c6dc-129">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3c6dc-130">-Location</span><span class="sxs-lookup"><span data-stu-id="3c6dc-130">-Location</span></span>
<span data-ttu-id="3c6dc-131">O local do circuito.</span><span class="sxs-lookup"><span data-stu-id="3c6dc-131">The location of the circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c6dc-132">-Name</span><span class="sxs-lookup"><span data-stu-id="3c6dc-132">-Name</span></span>
<span data-ttu-id="3c6dc-133">O nome do circuito ExpressRoute que está sendo criado.</span><span class="sxs-lookup"><span data-stu-id="3c6dc-133">The name of the ExpressRoute circuit being created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c6dc-134">-Peering</span><span class="sxs-lookup"><span data-stu-id="3c6dc-134">-Peering</span></span>
<span data-ttu-id="3c6dc-135">Configurações de par de lista.</span><span class="sxs-lookup"><span data-stu-id="3c6dc-135">A list peer configurations.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPeering[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c6dc-136">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="3c6dc-136">-PeeringLocation</span></span>
<span data-ttu-id="3c6dc-137">O nome do local de paração suportado pelo provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="3c6dc-137">The name of the peering location supported by the service provider.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceProvider
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c6dc-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c6dc-138">-ResourceGroupName</span></span>
<span data-ttu-id="3c6dc-139">O grupo de recursos que conterá o circuito.</span><span class="sxs-lookup"><span data-stu-id="3c6dc-139">The resource group that will contain the circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c6dc-140">-ServiceProviderName</span><span class="sxs-lookup"><span data-stu-id="3c6dc-140">-ServiceProviderName</span></span>
<span data-ttu-id="3c6dc-141">O nome do provedor de serviços de circuito.</span><span class="sxs-lookup"><span data-stu-id="3c6dc-141">The name of the circuit service provider.</span></span> <span data-ttu-id="3c6dc-142">Isso deve corresponder a um nome listado pelo cmdlet Get-AzExpressRouteServiceProvider.</span><span class="sxs-lookup"><span data-stu-id="3c6dc-142">This must match a name listed by the Get-AzExpressRouteServiceProvider cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceProvider
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c6dc-143">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="3c6dc-143">-SkuFamily</span></span>
<span data-ttu-id="3c6dc-144">A família SKU determina o tipo de cobrança.</span><span class="sxs-lookup"><span data-stu-id="3c6dc-144">SKU family determines the billing type.</span></span> <span data-ttu-id="3c6dc-145">Os valores possíveis para esse parâmetro são: `MeteredData` ou `UnlimitedData` .</span><span class="sxs-lookup"><span data-stu-id="3c6dc-145">Possible values for this parameter are: `MeteredData` or `UnlimitedData`.</span></span> <span data-ttu-id="3c6dc-146">Observe que você pode alterar o tipo de cobrança de MeteredData para UnlimitedData, mas não é possível alterar o tipo de UnlimitedData para MeteredData.</span><span class="sxs-lookup"><span data-stu-id="3c6dc-146">Note that you can change the billing type from MeteredData to UnlimitedData, but you can't change the type from UnlimitedData to MeteredData.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: MeteredData, UnlimitedData

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c6dc-147">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="3c6dc-147">-SkuTier</span></span>
<span data-ttu-id="3c6dc-148">A camada de serviço do circuito.</span><span class="sxs-lookup"><span data-stu-id="3c6dc-148">The tier of service for the circuit.</span></span> <span data-ttu-id="3c6dc-149">Os valores possíveis para esse parâmetro são: `Standard` , `Premium` ou `Local` .</span><span class="sxs-lookup"><span data-stu-id="3c6dc-149">Possible values for this parameter are: `Standard`, `Premium` or `Local`.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium, Local

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c6dc-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="3c6dc-150">-Tag</span></span>
<span data-ttu-id="3c6dc-151">Pares de valores-chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="3c6dc-151">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3c6dc-152">Por exemplo: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="3c6dc-152">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c6dc-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3c6dc-153">-Confirm</span></span>
<span data-ttu-id="3c6dc-154">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c6dc-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c6dc-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c6dc-155">-WhatIf</span></span>
<span data-ttu-id="3c6dc-156">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3c6dc-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c6dc-157">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3c6dc-157">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c6dc-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c6dc-158">CommonParameters</span></span>
<span data-ttu-id="3c6dc-159">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c6dc-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c6dc-160">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c6dc-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c6dc-161">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3c6dc-161">INPUTS</span></span>

### <span data-ttu-id="3c6dc-162">System.String</span><span class="sxs-lookup"><span data-stu-id="3c6dc-162">System.String</span></span>

### <span data-ttu-id="3c6dc-163">System.Int32</span><span class="sxs-lookup"><span data-stu-id="3c6dc-163">System.Int32</span></span>

### <span data-ttu-id="3c6dc-164">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="3c6dc-164">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

### <span data-ttu-id="3c6dc-165">System.Double</span><span class="sxs-lookup"><span data-stu-id="3c6dc-165">System.Double</span></span>

### <span data-ttu-id="3c6dc-166">Microsoft.Azure.Commands.Network.Models.PSPeering[]</span><span class="sxs-lookup"><span data-stu-id="3c6dc-166">Microsoft.Azure.Commands.Network.Models.PSPeering[]</span></span>

### <span data-ttu-id="3c6dc-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization[]</span><span class="sxs-lookup"><span data-stu-id="3c6dc-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization[]</span></span>

### <span data-ttu-id="3c6dc-168">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="3c6dc-168">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="3c6dc-169">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="3c6dc-169">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3c6dc-170">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3c6dc-170">OUTPUTS</span></span>

### <span data-ttu-id="3c6dc-171">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3c6dc-171">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="3c6dc-172">NOTES</span><span class="sxs-lookup"><span data-stu-id="3c6dc-172">NOTES</span></span>

## <span data-ttu-id="3c6dc-173">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3c6dc-173">RELATED LINKS</span></span>

[<span data-ttu-id="3c6dc-174">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3c6dc-174">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="3c6dc-175">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3c6dc-175">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="3c6dc-176">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3c6dc-176">Remove-AzExpressRouteCircuit</span></span>](Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="3c6dc-177">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3c6dc-177">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
