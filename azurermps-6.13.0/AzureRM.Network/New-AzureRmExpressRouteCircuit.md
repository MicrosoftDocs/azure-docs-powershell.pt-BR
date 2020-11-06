---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E40CAF2F-ED57-4AC1-8B9A-E48042DD8F91
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: cee0318367ad764a9cc9e37995f092462cd157a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430160"
---
# <span data-ttu-id="3597c-101">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3597c-101">New-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="3597c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3597c-102">SYNOPSIS</span></span>
<span data-ttu-id="3597c-103">Cria um circuito de rota do Azure Express.</span><span class="sxs-lookup"><span data-stu-id="3597c-103">Creates an Azure express route circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3597c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3597c-104">SYNTAX</span></span>

### <span data-ttu-id="3597c-105">ServiceProvider</span><span class="sxs-lookup"><span data-stu-id="3597c-105">ServiceProvider</span></span>
```
New-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 [-SkuTier <String>] [-SkuFamily <String>] [-ServiceProviderName <String>] [-PeeringLocation <String>]
 [-BandwidthInMbps <Int32>]
 [-Peering <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPeering]>]
 [-Authorization <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3597c-106">ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="3597c-106">ExpressRoutePort</span></span>
```
New-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 [-SkuTier <String>] [-SkuFamily <String>] [-ExpressRoutePort <PSExpressRoutePort>] [-BandwidthInGbps <Double>]
 [-Peering <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPeering]>]
 [-Authorization <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3597c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3597c-107">DESCRIPTION</span></span>
<span data-ttu-id="3597c-108">O cmdlet **New-AzureRmExpressRouteCircuit** cria um circuito de rota do Azure Express.</span><span class="sxs-lookup"><span data-stu-id="3597c-108">The **New-AzureRmExpressRouteCircuit** cmdlet creates an Azure express route circuit.</span></span>

## <span data-ttu-id="3597c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3597c-109">EXAMPLES</span></span>

### <span data-ttu-id="3597c-110">Exemplo 1: criar um novo circuito do ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="3597c-110">Example 1: Create a new ExpressRoute circuit</span></span>
```
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
New-AzureRmExpressRouteCircuit @parameters
```

### <span data-ttu-id="3597c-111">Exemplo 2: criar um novo circuito do ExpressRoute no ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="3597c-111">Example 2: Create a new ExpressRoute circuit on ExpressRoutePort</span></span>
```
$parameters = @{
    Name='ExpressRouteCircuit'
    ResourceGroupName='ExpressRouteResourceGroup'
    Location='West US'
    SkuTier='Standard'
    SkuFamily='MeteredData'
    ExpressRoutePort=$PSExpressRoutePort
    BandwidthInGbps=10.0
}
New-AzureRmExpressRouteCircuit @parameters
```

## <span data-ttu-id="3597c-112">OS</span><span class="sxs-lookup"><span data-stu-id="3597c-112">PARAMETERS</span></span>

### <span data-ttu-id="3597c-113">-AllowClassicOperations</span><span class="sxs-lookup"><span data-stu-id="3597c-113">-AllowClassicOperations</span></span>
<span data-ttu-id="3597c-114">O uso desse parâmetro permite que você use os cmdlets clássicos do PowerShell do PowerShell para gerenciar o circuito.</span><span class="sxs-lookup"><span data-stu-id="3597c-114">The use of this parameter allows you to use the classic Azure PowerShell cmdlets to manage the circuit.</span></span>

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

### <span data-ttu-id="3597c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3597c-115">-AsJob</span></span>
<span data-ttu-id="3597c-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="3597c-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3597c-117">-Authorization</span><span class="sxs-lookup"><span data-stu-id="3597c-117">-Authorization</span></span>
<span data-ttu-id="3597c-118">Uma lista de autorizações de circuito.</span><span class="sxs-lookup"><span data-stu-id="3597c-118">A list of circuit authorizations.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3597c-119">-BandwidthInGbps</span><span class="sxs-lookup"><span data-stu-id="3597c-119">-BandwidthInGbps</span></span>
<span data-ttu-id="3597c-120">A largura de banda do circuito quando o circuito é provisionado em um recurso ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="3597c-120">The bandwidth of the circuit when the circuit is provisioned on an ExpressRoutePort resource.</span></span>

```yaml
Type: Double
Parameter Sets: ExpressRoutePort
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3597c-121">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="3597c-121">-BandwidthInMbps</span></span>
<span data-ttu-id="3597c-122">A largura de banda do circuito.</span><span class="sxs-lookup"><span data-stu-id="3597c-122">The bandwidth of the circuit.</span></span> <span data-ttu-id="3597c-123">Deve ser um valor que seja compatível com o provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="3597c-123">This must be a value that is supported by the service provider.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ServiceProvider
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3597c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3597c-124">-DefaultProfile</span></span>
<span data-ttu-id="3597c-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3597c-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3597c-126">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="3597c-126">-ExpressRoutePort</span></span>
<span data-ttu-id="3597c-127">A referência ao recurso ExpressRoutePort quando o circuito é provisionado em um recurso ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="3597c-127">The reference to the ExpressRoutePort resource when the circuit is provisioned on an ExpressRoutePort resource.</span></span>

```yaml
Type: PSExpressRoutePort
Parameter Sets: ExpressRoutePort
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3597c-128">-Force</span><span class="sxs-lookup"><span data-stu-id="3597c-128">-Force</span></span>
<span data-ttu-id="3597c-129">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="3597c-129">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3597c-130">-Local</span><span class="sxs-lookup"><span data-stu-id="3597c-130">-Location</span></span>
<span data-ttu-id="3597c-131">O local do circuito.</span><span class="sxs-lookup"><span data-stu-id="3597c-131">The location of the circuit.</span></span>

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

### <span data-ttu-id="3597c-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="3597c-132">-Name</span></span>
<span data-ttu-id="3597c-133">O nome do circuito do ExpressRoute que está sendo criado.</span><span class="sxs-lookup"><span data-stu-id="3597c-133">The name of the ExpressRoute circuit being created.</span></span>

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

### <span data-ttu-id="3597c-134">Ponto-a-ponto</span><span class="sxs-lookup"><span data-stu-id="3597c-134">-Peering</span></span>
<span data-ttu-id="3597c-135">Configurações de pares de lista.</span><span class="sxs-lookup"><span data-stu-id="3597c-135">A list peer configurations.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPeering]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3597c-136">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="3597c-136">-PeeringLocation</span></span>
<span data-ttu-id="3597c-137">O nome do local de emparelhamento compatível com o provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="3597c-137">The name of the peering location supported by the service provider.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceProvider
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3597c-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3597c-138">-ResourceGroupName</span></span>
<span data-ttu-id="3597c-139">O grupo de recursos que conterá o circuito.</span><span class="sxs-lookup"><span data-stu-id="3597c-139">The resource group that will contain the circuit.</span></span>

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

### <span data-ttu-id="3597c-140">-Inprovidername</span><span class="sxs-lookup"><span data-stu-id="3597c-140">-ServiceProviderName</span></span>
<span data-ttu-id="3597c-141">O nome do provedor de serviços de circuito.</span><span class="sxs-lookup"><span data-stu-id="3597c-141">The name of the circuit service provider.</span></span> <span data-ttu-id="3597c-142">Isso deve corresponder a um nome listado pelo cmdlet Get-AzureRmExpressRouteServiceProvider.</span><span class="sxs-lookup"><span data-stu-id="3597c-142">This must match a name listed by the Get-AzureRmExpressRouteServiceProvider cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceProvider
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3597c-143">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="3597c-143">-SkuFamily</span></span>
<span data-ttu-id="3597c-144">A família SKU determina o tipo de cobrança.</span><span class="sxs-lookup"><span data-stu-id="3597c-144">SKU family determines the billing type.</span></span> <span data-ttu-id="3597c-145">Os valores possíveis para esse parâmetro são: `MeteredData` ou `UnlimitedData` .</span><span class="sxs-lookup"><span data-stu-id="3597c-145">Possible values for this parameter are: `MeteredData` or `UnlimitedData`.</span></span> <span data-ttu-id="3597c-146">Observe que você pode alterar o tipo de cobrança de MeteredData para UnlimitedData, mas não pode alterar o tipo de UnlimitedData para MeteredData.</span><span class="sxs-lookup"><span data-stu-id="3597c-146">Note that you can change the billing type from MeteredData to UnlimitedData, but you can't change the type from UnlimitedData to MeteredData.</span></span>

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

### <span data-ttu-id="3597c-147">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="3597c-147">-SkuTier</span></span>
<span data-ttu-id="3597c-148">O nível de serviço para o circuito.</span><span class="sxs-lookup"><span data-stu-id="3597c-148">The tier of service for the circuit.</span></span> <span data-ttu-id="3597c-149">Os valores possíveis para esse parâmetro são: `Standard` ou `Premium` .</span><span class="sxs-lookup"><span data-stu-id="3597c-149">Possible values for this parameter are: `Standard` or `Premium`.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3597c-150">-Marca</span><span class="sxs-lookup"><span data-stu-id="3597c-150">-Tag</span></span>
<span data-ttu-id="3597c-151">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="3597c-151">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3597c-152">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="3597c-152">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="3597c-153">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3597c-153">-Confirm</span></span>
<span data-ttu-id="3597c-154">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3597c-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3597c-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3597c-155">-WhatIf</span></span>
<span data-ttu-id="3597c-156">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3597c-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3597c-157">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3597c-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3597c-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3597c-158">CommonParameters</span></span>
<span data-ttu-id="3597c-159">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3597c-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3597c-160">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3597c-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3597c-161">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3597c-161">INPUTS</span></span>

### <span data-ttu-id="3597c-162">System. String</span><span class="sxs-lookup"><span data-stu-id="3597c-162">System.String</span></span>

### <span data-ttu-id="3597c-163">System. Int32</span><span class="sxs-lookup"><span data-stu-id="3597c-163">System.Int32</span></span>

### <span data-ttu-id="3597c-164">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSPeering, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="3597c-164">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSPeering, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="3597c-165">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitAuthorization, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="3597c-165">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="3597c-166">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="3597c-166">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="3597c-167">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="3597c-167">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3597c-168">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3597c-168">OUTPUTS</span></span>

### <span data-ttu-id="3597c-169">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3597c-169">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="3597c-170">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3597c-170">NOTES</span></span>

## <span data-ttu-id="3597c-171">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3597c-171">RELATED LINKS</span></span>

[<span data-ttu-id="3597c-172">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3597c-172">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="3597c-173">Mover-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3597c-173">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="3597c-174">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3597c-174">Remove-AzureRmExpressRouteCircuit</span></span>](Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="3597c-175">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3597c-175">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
