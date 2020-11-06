---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRoutePort.md
ms.openlocfilehash: 8d3b204815fc273f97a549582a193002f5f4a48d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429465"
---
# <span data-ttu-id="bf598-101">New-AzureRmExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="bf598-101">New-AzureRmExpressRoutePort</span></span>

## <span data-ttu-id="bf598-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bf598-102">SYNOPSIS</span></span>
<span data-ttu-id="bf598-103">Cria um ExpressRoutePort do Azure.</span><span class="sxs-lookup"><span data-stu-id="bf598-103">Creates an Azure ExpressRoutePort.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf598-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bf598-104">SYNTAX</span></span>

### <span data-ttu-id="bf598-105">ResourceNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="bf598-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzureRmExpressRoutePort -ResourceGroupName <String> -Name <String> -PeeringLocation <String>
 -BandwidthInGbps <Int32> -Encapsulation <String> -Location <String> [-Tag <Hashtable>]
 [-Link <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink]>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf598-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf598-106">ResourceIdParameterSet</span></span>
```
New-AzureRmExpressRoutePort -ResourceId <String> -PeeringLocation <String> -BandwidthInGbps <Int32>
 -Encapsulation <String> -Location <String> [-Tag <Hashtable>]
 [-Link <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink]>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf598-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bf598-107">DESCRIPTION</span></span>
<span data-ttu-id="bf598-108">O cmdlet **New-AzureRmExpressRoutePort** cria um Azure ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="bf598-108">The **New-AzureRmExpressRoutePort** cmdlet creates an Azure ExpressRoutePort</span></span>

## <span data-ttu-id="bf598-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bf598-109">EXAMPLES</span></span>

### <span data-ttu-id="bf598-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bf598-110">Example 1</span></span>
```powershell
PS C:\> $parameters = @{
    Name='ExpressRoutePort'
    ResourceGroupName='ExpressRouteResourceGroup'
    Location='West US'
    PeeringLocation='Silicon Valley'
    BandwidthInGbps=100
    Encapsulation='QinQ'
}
PS C:\> New-AzureRmExpressRoutePort @parameters
```

### <span data-ttu-id="bf598-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="bf598-111">Example 2</span></span>
```powershell
PS C:\> $parameters = @{
    ResourceId='/subscriptions/<SubId>/resourceGroups/<ResourceGroupName>/providers/Microsoft.Network/expressRoutePorts/<PortName>'
    Location='West US'
    PeeringLocation='Silicon Valley'
    BandwidthInGbps=100
    Encapsulation='QinQ'
}
PS C:\> New-AzureRmExpressRoutePort @parameters
```

## <span data-ttu-id="bf598-112">OS</span><span class="sxs-lookup"><span data-stu-id="bf598-112">PARAMETERS</span></span>

### <span data-ttu-id="bf598-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bf598-113">-AsJob</span></span>
<span data-ttu-id="bf598-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="bf598-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bf598-115">-BandwidthInGbps</span><span class="sxs-lookup"><span data-stu-id="bf598-115">-BandwidthInGbps</span></span>
<span data-ttu-id="bf598-116">Largura de banda das portas adquiridas em Gbps</span><span class="sxs-lookup"><span data-stu-id="bf598-116">Bandwidth of procured ports in Gbps</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf598-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf598-117">-DefaultProfile</span></span>
<span data-ttu-id="bf598-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bf598-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf598-119">-Encapsulamento</span><span class="sxs-lookup"><span data-stu-id="bf598-119">-Encapsulation</span></span>
<span data-ttu-id="bf598-120">Método de encapsulamento em portas físicas.</span><span class="sxs-lookup"><span data-stu-id="bf598-120">Encapsulation method on physical ports.</span></span>

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

### <span data-ttu-id="bf598-121">-Force</span><span class="sxs-lookup"><span data-stu-id="bf598-121">-Force</span></span>
<span data-ttu-id="bf598-122">Não pedir confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="bf598-122">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="bf598-123">-Link</span><span class="sxs-lookup"><span data-stu-id="bf598-123">-Link</span></span>
<span data-ttu-id="bf598-124">O conjunto de links físicos do recurso ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="bf598-124">The set of physical links of the ExpressRoutePort resource</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf598-125">-Local</span><span class="sxs-lookup"><span data-stu-id="bf598-125">-Location</span></span>
<span data-ttu-id="bf598-126">O local.</span><span class="sxs-lookup"><span data-stu-id="bf598-126">The location.</span></span>

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

### <span data-ttu-id="bf598-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="bf598-127">-Name</span></span>
<span data-ttu-id="bf598-128">O nome do ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="bf598-128">The name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf598-129">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="bf598-129">-PeeringLocation</span></span>
<span data-ttu-id="bf598-130">O nome do local de emparelhamento ao qual o ExpressRoutePort está mapeado fisicamente.</span><span class="sxs-lookup"><span data-stu-id="bf598-130">The name of the peering location that the ExpressRoutePort is mapped to physically.</span></span>

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

### <span data-ttu-id="bf598-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf598-131">-ResourceGroupName</span></span>
<span data-ttu-id="bf598-132">O nome do grupo de recursos do ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="bf598-132">The resource group name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf598-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bf598-133">-ResourceId</span></span>
<span data-ttu-id="bf598-134">ResourceId da porta de rota expressa.</span><span class="sxs-lookup"><span data-stu-id="bf598-134">ResourceId of the express route port.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf598-135">-Marca</span><span class="sxs-lookup"><span data-stu-id="bf598-135">-Tag</span></span>
<span data-ttu-id="bf598-136">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="bf598-136">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="bf598-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bf598-137">-Confirm</span></span>
<span data-ttu-id="bf598-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf598-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf598-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf598-139">-WhatIf</span></span>
<span data-ttu-id="bf598-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bf598-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf598-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bf598-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf598-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf598-142">CommonParameters</span></span>
<span data-ttu-id="bf598-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf598-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf598-144">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf598-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf598-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bf598-145">INPUTS</span></span>

### <span data-ttu-id="bf598-146">System. String</span><span class="sxs-lookup"><span data-stu-id="bf598-146">System.String</span></span>

### <span data-ttu-id="bf598-147">System. Int32</span><span class="sxs-lookup"><span data-stu-id="bf598-147">System.Int32</span></span>

### <span data-ttu-id="bf598-148">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="bf598-148">System.Collections.Hashtable</span></span>

### <span data-ttu-id="bf598-149">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSExpressRouteLink, Microsoft. Azure. Commands. Network, Version = 6.3.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="bf598-149">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink, Microsoft.Azure.Commands.Network, Version=6.3.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="bf598-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bf598-150">OUTPUTS</span></span>

### <span data-ttu-id="bf598-151">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="bf598-151">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="bf598-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bf598-152">NOTES</span></span>

## <span data-ttu-id="bf598-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bf598-153">RELATED LINKS</span></span>
