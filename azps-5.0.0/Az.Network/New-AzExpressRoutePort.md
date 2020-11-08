---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePort.md
ms.openlocfilehash: 54cdcbbd1d9564dde4fbe4a9aa0b0bea8a0325a3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125606"
---
# <span data-ttu-id="ffbee-101">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="ffbee-101">New-AzExpressRoutePort</span></span>

## <span data-ttu-id="ffbee-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ffbee-102">SYNOPSIS</span></span>
<span data-ttu-id="ffbee-103">Cria um ExpressRoutePort do Azure.</span><span class="sxs-lookup"><span data-stu-id="ffbee-103">Creates an Azure ExpressRoutePort.</span></span>

## <span data-ttu-id="ffbee-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ffbee-104">SYNTAX</span></span>

### <span data-ttu-id="ffbee-105">ResourceNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="ffbee-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzExpressRoutePort -ResourceGroupName <String> -Name <String> -PeeringLocation <String>
 -BandwidthInGbps <Int32> -Encapsulation <String> -Location <String> [-Tag <Hashtable>]
 [-Link <PSExpressRouteLink[]>] [-Force] [-AsJob] [-Identity <PSManagedServiceIdentity>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ffbee-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ffbee-106">ResourceIdParameterSet</span></span>
```
New-AzExpressRoutePort -ResourceId <String> -PeeringLocation <String> -BandwidthInGbps <Int32>
 -Encapsulation <String> -Location <String> [-Tag <Hashtable>] [-Link <PSExpressRouteLink[]>] [-Force] [-AsJob]
 [-Identity <PSManagedServiceIdentity>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ffbee-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ffbee-107">DESCRIPTION</span></span>
<span data-ttu-id="ffbee-108">O cmdlet **New-AzExpressRoutePort** cria um Azure ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="ffbee-108">The **New-AzExpressRoutePort** cmdlet creates an Azure ExpressRoutePort</span></span>

## <span data-ttu-id="ffbee-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ffbee-109">EXAMPLES</span></span>

### <span data-ttu-id="ffbee-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ffbee-110">Example 1</span></span>
```powershell
PS C:\> $parameters = @{
    Name='ExpressRoutePort'
    ResourceGroupName='ExpressRouteResourceGroup'
    Location='West US'
    PeeringLocation='Silicon Valley'
    BandwidthInGbps=100
    Encapsulation='QinQ'
}
PS C:\> New-AzExpressRoutePort @parameters
```

### <span data-ttu-id="ffbee-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ffbee-111">Example 2</span></span>
```powershell
PS C:\> $parameters = @{
    ResourceId='/subscriptions/<SubId>/resourceGroups/<ResourceGroupName>/providers/Microsoft.Network/expressRoutePorts/<PortName>'
    Location='West US'
    PeeringLocation='Silicon Valley'
    BandwidthInGbps=100
    Encapsulation='QinQ'
}
PS C:\> New-AzExpressRoutePort @parameters
```

## <span data-ttu-id="ffbee-112">OS</span><span class="sxs-lookup"><span data-stu-id="ffbee-112">PARAMETERS</span></span>

### <span data-ttu-id="ffbee-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ffbee-113">-AsJob</span></span>
<span data-ttu-id="ffbee-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="ffbee-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ffbee-115">-BandwidthInGbps</span><span class="sxs-lookup"><span data-stu-id="ffbee-115">-BandwidthInGbps</span></span>
<span data-ttu-id="ffbee-116">Largura de banda das portas adquiridas em Gbps</span><span class="sxs-lookup"><span data-stu-id="ffbee-116">Bandwidth of procured ports in Gbps</span></span>

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

### <span data-ttu-id="ffbee-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffbee-117">-DefaultProfile</span></span>
<span data-ttu-id="ffbee-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ffbee-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ffbee-119">-Encapsulamento</span><span class="sxs-lookup"><span data-stu-id="ffbee-119">-Encapsulation</span></span>
<span data-ttu-id="ffbee-120">Método de encapsulamento em portas físicas.</span><span class="sxs-lookup"><span data-stu-id="ffbee-120">Encapsulation method on physical ports.</span></span>

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

### <span data-ttu-id="ffbee-121">-Force</span><span class="sxs-lookup"><span data-stu-id="ffbee-121">-Force</span></span>
<span data-ttu-id="ffbee-122">Não pedir confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="ffbee-122">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="ffbee-123">-Identidade</span><span class="sxs-lookup"><span data-stu-id="ffbee-123">-Identity</span></span>
<span data-ttu-id="ffbee-124">Identidade atribuída pelo usuário para ler a configuração do MacSec</span><span class="sxs-lookup"><span data-stu-id="ffbee-124">User Assigned Identity for reading MacSec configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffbee-125">-Link</span><span class="sxs-lookup"><span data-stu-id="ffbee-125">-Link</span></span>
<span data-ttu-id="ffbee-126">O conjunto de links físicos do recurso ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="ffbee-126">The set of physical links of the ExpressRoutePort resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffbee-127">-Local</span><span class="sxs-lookup"><span data-stu-id="ffbee-127">-Location</span></span>
<span data-ttu-id="ffbee-128">O local.</span><span class="sxs-lookup"><span data-stu-id="ffbee-128">The location.</span></span>

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

### <span data-ttu-id="ffbee-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="ffbee-129">-Name</span></span>
<span data-ttu-id="ffbee-130">O nome do ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="ffbee-130">The name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="ffbee-131">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="ffbee-131">-PeeringLocation</span></span>
<span data-ttu-id="ffbee-132">O nome do local de emparelhamento ao qual o ExpressRoutePort está mapeado fisicamente.</span><span class="sxs-lookup"><span data-stu-id="ffbee-132">The name of the peering location that the ExpressRoutePort is mapped to physically.</span></span>

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

### <span data-ttu-id="ffbee-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffbee-133">-ResourceGroupName</span></span>
<span data-ttu-id="ffbee-134">O nome do grupo de recursos do ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="ffbee-134">The resource group name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="ffbee-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ffbee-135">-ResourceId</span></span>
<span data-ttu-id="ffbee-136">ResourceId da porta de rota expressa.</span><span class="sxs-lookup"><span data-stu-id="ffbee-136">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="ffbee-137">-Marca</span><span class="sxs-lookup"><span data-stu-id="ffbee-137">-Tag</span></span>
<span data-ttu-id="ffbee-138">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="ffbee-138">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="ffbee-139">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ffbee-139">-Confirm</span></span>
<span data-ttu-id="ffbee-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ffbee-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffbee-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffbee-141">-WhatIf</span></span>
<span data-ttu-id="ffbee-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ffbee-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffbee-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ffbee-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffbee-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffbee-144">CommonParameters</span></span>
<span data-ttu-id="ffbee-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffbee-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffbee-146">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffbee-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffbee-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ffbee-147">INPUTS</span></span>

### <span data-ttu-id="ffbee-148">System. String</span><span class="sxs-lookup"><span data-stu-id="ffbee-148">System.String</span></span>

### <span data-ttu-id="ffbee-149">System. Int32</span><span class="sxs-lookup"><span data-stu-id="ffbee-149">System.Int32</span></span>

### <span data-ttu-id="ffbee-150">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ffbee-150">System.Collections.Hashtable</span></span>

### <span data-ttu-id="ffbee-151">Microsoft. Azure. Commands. Network. Models. PSExpressRouteLink []</span><span class="sxs-lookup"><span data-stu-id="ffbee-151">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink[]</span></span>

## <span data-ttu-id="ffbee-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ffbee-152">OUTPUTS</span></span>

### <span data-ttu-id="ffbee-153">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="ffbee-153">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="ffbee-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ffbee-154">NOTES</span></span>

## <span data-ttu-id="ffbee-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ffbee-155">RELATED LINKS</span></span>

[<span data-ttu-id="ffbee-156">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="ffbee-156">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="ffbee-157">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="ffbee-157">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)

[<span data-ttu-id="ffbee-158">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="ffbee-158">Set-AzExpressRoutePort</span></span>](./Set-AzExpressRoutePort.md)
