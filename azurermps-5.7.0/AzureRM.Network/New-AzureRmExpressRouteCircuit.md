---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E40CAF2F-ED57-4AC1-8B9A-E48042DD8F91
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: 0c611edc0ef8cb117e556a19e22f93d1f8db96ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432079"
---
# <span data-ttu-id="3117b-101">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3117b-101">New-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="3117b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3117b-102">SYNOPSIS</span></span>
<span data-ttu-id="3117b-103">Cria um circuito de rota do Azure Express.</span><span class="sxs-lookup"><span data-stu-id="3117b-103">Creates an Azure express route circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3117b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3117b-104">SYNTAX</span></span>

```
New-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 [-SkuTier <String>] [-SkuFamily <String>] -ServiceProviderName <String> -PeeringLocation <String>
 -BandwidthInMbps <Int32>
 [-Peering <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPeering]>]
 [-Authorization <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3117b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3117b-105">DESCRIPTION</span></span>
<span data-ttu-id="3117b-106">O cmdlet **New-AzureRmExpressRouteCircuit** cria um circuito de rota do Azure Express.</span><span class="sxs-lookup"><span data-stu-id="3117b-106">The **New-AzureRmExpressRouteCircuit** cmdlet creates an Azure express route circuit.</span></span>

## <span data-ttu-id="3117b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3117b-107">EXAMPLES</span></span>

### <span data-ttu-id="3117b-108">Exemplo 1: criar um novo circuito do ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="3117b-108">Example 1: Create a new ExpressRoute circuit</span></span>
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

## <span data-ttu-id="3117b-109">OS</span><span class="sxs-lookup"><span data-stu-id="3117b-109">PARAMETERS</span></span>

### <span data-ttu-id="3117b-110">-AllowClassicOperations</span><span class="sxs-lookup"><span data-stu-id="3117b-110">-AllowClassicOperations</span></span>
<span data-ttu-id="3117b-111">O uso desse parâmetro permite que você use os cmdlets clássicos do PowerShell do PowerShell para gerenciar o circuito.</span><span class="sxs-lookup"><span data-stu-id="3117b-111">The use of this parameter allows you to use the classic Azure PowerShell cmdlets to manage the circuit.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3117b-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3117b-112">-AsJob</span></span>
<span data-ttu-id="3117b-113">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="3117b-113">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3117b-114">-Authorization</span><span class="sxs-lookup"><span data-stu-id="3117b-114">-Authorization</span></span>
<span data-ttu-id="3117b-115">Uma lista de autorizações de circuito.</span><span class="sxs-lookup"><span data-stu-id="3117b-115">A list of circuit authorizations.</span></span>

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

### <span data-ttu-id="3117b-116">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="3117b-116">-BandwidthInMbps</span></span>
<span data-ttu-id="3117b-117">A largura de banda do circuito.</span><span class="sxs-lookup"><span data-stu-id="3117b-117">The bandwidth of the circuit.</span></span> <span data-ttu-id="3117b-118">Deve ser um valor que seja compatível com o provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="3117b-118">This must be a value that is supported by the service provider.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3117b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3117b-119">-DefaultProfile</span></span>
<span data-ttu-id="3117b-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3117b-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3117b-121">-Force</span><span class="sxs-lookup"><span data-stu-id="3117b-121">-Force</span></span>
<span data-ttu-id="3117b-122">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="3117b-122">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3117b-123">-Local</span><span class="sxs-lookup"><span data-stu-id="3117b-123">-Location</span></span>
<span data-ttu-id="3117b-124">O local do circuito.</span><span class="sxs-lookup"><span data-stu-id="3117b-124">The location of the circuit.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3117b-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="3117b-125">-Name</span></span>
<span data-ttu-id="3117b-126">O nome do circuito do ExpressRoute que está sendo criado.</span><span class="sxs-lookup"><span data-stu-id="3117b-126">The name of the ExpressRoute circuit being created.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3117b-127">Ponto-a-ponto</span><span class="sxs-lookup"><span data-stu-id="3117b-127">-Peering</span></span>
<span data-ttu-id="3117b-128">Configurações de pares de lista.</span><span class="sxs-lookup"><span data-stu-id="3117b-128">A list peer configurations.</span></span>

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

### <span data-ttu-id="3117b-129">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="3117b-129">-PeeringLocation</span></span>
<span data-ttu-id="3117b-130">O nome do local de emparelhamento compatível com o provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="3117b-130">The name of the peering location supported by the service provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3117b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3117b-131">-ResourceGroupName</span></span>
<span data-ttu-id="3117b-132">O grupo de recursos que conterá o circuito.</span><span class="sxs-lookup"><span data-stu-id="3117b-132">The resource group that will contain the circuit.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3117b-133">-Inprovidername</span><span class="sxs-lookup"><span data-stu-id="3117b-133">-ServiceProviderName</span></span>
<span data-ttu-id="3117b-134">O nome do provedor de serviços de circuito.</span><span class="sxs-lookup"><span data-stu-id="3117b-134">The name of the circuit service provider.</span></span> <span data-ttu-id="3117b-135">Isso deve corresponder a um nome listado pelo cmdlet Get-AzureRmExpressRouteServiceProvider.</span><span class="sxs-lookup"><span data-stu-id="3117b-135">This must match a name listed by the Get-AzureRmExpressRouteServiceProvider cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3117b-136">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="3117b-136">-SkuFamily</span></span>
<span data-ttu-id="3117b-137">A família SKU determina o tipo de cobrança.</span><span class="sxs-lookup"><span data-stu-id="3117b-137">SKU family determines the billing type.</span></span> <span data-ttu-id="3117b-138">Os valores possíveis para esse parâmetro são: `MeteredData` ou `UnlimitedData` .</span><span class="sxs-lookup"><span data-stu-id="3117b-138">Possible values for this parameter are: `MeteredData` or `UnlimitedData`.</span></span> <span data-ttu-id="3117b-139">Observe que você pode alterar o tipo de cobrança de MeteredData para UnlimitedData, mas não pode alterar o tipo de UnlimitedData para MeteredData.</span><span class="sxs-lookup"><span data-stu-id="3117b-139">Note that you can change the billing type from MeteredData to UnlimitedData, but you can't change the type from UnlimitedData to MeteredData.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: MeteredData, UnlimitedData

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3117b-140">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="3117b-140">-SkuTier</span></span>
<span data-ttu-id="3117b-141">O nível de serviço para o circuito.</span><span class="sxs-lookup"><span data-stu-id="3117b-141">The tier of service for the circuit.</span></span> <span data-ttu-id="3117b-142">Os valores possíveis para esse parâmetro são: `Standard` ou `Premium` .</span><span class="sxs-lookup"><span data-stu-id="3117b-142">Possible values for this parameter are: `Standard` or `Premium`.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3117b-143">-Marca</span><span class="sxs-lookup"><span data-stu-id="3117b-143">-Tag</span></span>
<span data-ttu-id="3117b-144">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="3117b-144">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3117b-145">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="3117b-145">For example:</span></span>

<span data-ttu-id="3117b-146">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="3117b-146">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3117b-147">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3117b-147">-Confirm</span></span>
<span data-ttu-id="3117b-148">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3117b-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3117b-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3117b-149">-WhatIf</span></span>
<span data-ttu-id="3117b-150">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3117b-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3117b-151">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3117b-151">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3117b-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3117b-152">CommonParameters</span></span>
<span data-ttu-id="3117b-153">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3117b-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3117b-154">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3117b-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3117b-155">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3117b-155">INPUTS</span></span>

### <span data-ttu-id="3117b-156">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="3117b-156">None</span></span>
<span data-ttu-id="3117b-157">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="3117b-157">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3117b-158">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3117b-158">OUTPUTS</span></span>

### <span data-ttu-id="3117b-159">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3117b-159">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="3117b-160">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3117b-160">NOTES</span></span>

## <span data-ttu-id="3117b-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3117b-161">RELATED LINKS</span></span>

[<span data-ttu-id="3117b-162">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3117b-162">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="3117b-163">Mover-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3117b-163">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="3117b-164">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3117b-164">Remove-AzureRmExpressRouteCircuit</span></span>](Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="3117b-165">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3117b-165">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
