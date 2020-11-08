---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePort.md
ms.openlocfilehash: 54cdcbbd1d9564dde4fbe4a9aa0b0bea8a0325a3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114862"
---
# <span data-ttu-id="cb697-101">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="cb697-101">New-AzExpressRoutePort</span></span>

## <span data-ttu-id="cb697-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cb697-102">SYNOPSIS</span></span>
<span data-ttu-id="cb697-103">Cria um ExpressRoutePort do Azure.</span><span class="sxs-lookup"><span data-stu-id="cb697-103">Creates an Azure ExpressRoutePort.</span></span>

## <span data-ttu-id="cb697-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cb697-104">SYNTAX</span></span>

### <span data-ttu-id="cb697-105">ResourceNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="cb697-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzExpressRoutePort -ResourceGroupName <String> -Name <String> -PeeringLocation <String>
 -BandwidthInGbps <Int32> -Encapsulation <String> -Location <String> [-Tag <Hashtable>]
 [-Link <PSExpressRouteLink[]>] [-Force] [-AsJob] [-Identity <PSManagedServiceIdentity>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb697-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb697-106">ResourceIdParameterSet</span></span>
```
New-AzExpressRoutePort -ResourceId <String> -PeeringLocation <String> -BandwidthInGbps <Int32>
 -Encapsulation <String> -Location <String> [-Tag <Hashtable>] [-Link <PSExpressRouteLink[]>] [-Force] [-AsJob]
 [-Identity <PSManagedServiceIdentity>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cb697-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cb697-107">DESCRIPTION</span></span>
<span data-ttu-id="cb697-108">O cmdlet **New-AzExpressRoutePort** cria um Azure ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="cb697-108">The **New-AzExpressRoutePort** cmdlet creates an Azure ExpressRoutePort</span></span>

## <span data-ttu-id="cb697-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cb697-109">EXAMPLES</span></span>

### <span data-ttu-id="cb697-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cb697-110">Example 1</span></span>
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

### <span data-ttu-id="cb697-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="cb697-111">Example 2</span></span>
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

## <span data-ttu-id="cb697-112">OS</span><span class="sxs-lookup"><span data-stu-id="cb697-112">PARAMETERS</span></span>

### <span data-ttu-id="cb697-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cb697-113">-AsJob</span></span>
<span data-ttu-id="cb697-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="cb697-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cb697-115">-BandwidthInGbps</span><span class="sxs-lookup"><span data-stu-id="cb697-115">-BandwidthInGbps</span></span>
<span data-ttu-id="cb697-116">Largura de banda das portas adquiridas em Gbps</span><span class="sxs-lookup"><span data-stu-id="cb697-116">Bandwidth of procured ports in Gbps</span></span>

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

### <span data-ttu-id="cb697-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb697-117">-DefaultProfile</span></span>
<span data-ttu-id="cb697-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cb697-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb697-119">-Encapsulamento</span><span class="sxs-lookup"><span data-stu-id="cb697-119">-Encapsulation</span></span>
<span data-ttu-id="cb697-120">Método de encapsulamento em portas físicas.</span><span class="sxs-lookup"><span data-stu-id="cb697-120">Encapsulation method on physical ports.</span></span>

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

### <span data-ttu-id="cb697-121">-Force</span><span class="sxs-lookup"><span data-stu-id="cb697-121">-Force</span></span>
<span data-ttu-id="cb697-122">Não pedir confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="cb697-122">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="cb697-123">-Identidade</span><span class="sxs-lookup"><span data-stu-id="cb697-123">-Identity</span></span>
<span data-ttu-id="cb697-124">Identidade atribuída pelo usuário para ler a configuração do MacSec</span><span class="sxs-lookup"><span data-stu-id="cb697-124">User Assigned Identity for reading MacSec configuration</span></span>

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

### <span data-ttu-id="cb697-125">-Link</span><span class="sxs-lookup"><span data-stu-id="cb697-125">-Link</span></span>
<span data-ttu-id="cb697-126">O conjunto de links físicos do recurso ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="cb697-126">The set of physical links of the ExpressRoutePort resource</span></span>

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

### <span data-ttu-id="cb697-127">-Local</span><span class="sxs-lookup"><span data-stu-id="cb697-127">-Location</span></span>
<span data-ttu-id="cb697-128">O local.</span><span class="sxs-lookup"><span data-stu-id="cb697-128">The location.</span></span>

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

### <span data-ttu-id="cb697-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="cb697-129">-Name</span></span>
<span data-ttu-id="cb697-130">O nome do ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="cb697-130">The name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="cb697-131">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="cb697-131">-PeeringLocation</span></span>
<span data-ttu-id="cb697-132">O nome do local de emparelhamento ao qual o ExpressRoutePort está mapeado fisicamente.</span><span class="sxs-lookup"><span data-stu-id="cb697-132">The name of the peering location that the ExpressRoutePort is mapped to physically.</span></span>

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

### <span data-ttu-id="cb697-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb697-133">-ResourceGroupName</span></span>
<span data-ttu-id="cb697-134">O nome do grupo de recursos do ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="cb697-134">The resource group name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="cb697-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb697-135">-ResourceId</span></span>
<span data-ttu-id="cb697-136">ResourceId da porta de rota expressa.</span><span class="sxs-lookup"><span data-stu-id="cb697-136">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="cb697-137">-Marca</span><span class="sxs-lookup"><span data-stu-id="cb697-137">-Tag</span></span>
<span data-ttu-id="cb697-138">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="cb697-138">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="cb697-139">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cb697-139">-Confirm</span></span>
<span data-ttu-id="cb697-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb697-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb697-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb697-141">-WhatIf</span></span>
<span data-ttu-id="cb697-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cb697-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb697-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cb697-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb697-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb697-144">CommonParameters</span></span>
<span data-ttu-id="cb697-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb697-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb697-146">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb697-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb697-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cb697-147">INPUTS</span></span>

### <span data-ttu-id="cb697-148">System. String</span><span class="sxs-lookup"><span data-stu-id="cb697-148">System.String</span></span>

### <span data-ttu-id="cb697-149">System. Int32</span><span class="sxs-lookup"><span data-stu-id="cb697-149">System.Int32</span></span>

### <span data-ttu-id="cb697-150">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="cb697-150">System.Collections.Hashtable</span></span>

### <span data-ttu-id="cb697-151">Microsoft. Azure. Commands. Network. Models. PSExpressRouteLink []</span><span class="sxs-lookup"><span data-stu-id="cb697-151">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink[]</span></span>

## <span data-ttu-id="cb697-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cb697-152">OUTPUTS</span></span>

### <span data-ttu-id="cb697-153">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="cb697-153">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="cb697-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cb697-154">NOTES</span></span>

## <span data-ttu-id="cb697-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cb697-155">RELATED LINKS</span></span>

[<span data-ttu-id="cb697-156">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="cb697-156">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="cb697-157">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="cb697-157">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)

[<span data-ttu-id="cb697-158">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="cb697-158">Set-AzExpressRoutePort</span></span>](./Set-AzExpressRoutePort.md)
