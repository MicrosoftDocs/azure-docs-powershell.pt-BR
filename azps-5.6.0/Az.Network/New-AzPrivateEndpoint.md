---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateEndpoint.md
ms.openlocfilehash: f7ec596a73c3659584d1e0b80c899b4bf9aad8d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889180"
---
# <span data-ttu-id="aa3ce-101">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="aa3ce-101">New-AzPrivateEndpoint</span></span>

## <span data-ttu-id="aa3ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa3ce-102">SYNOPSIS</span></span>
<span data-ttu-id="aa3ce-103">Cria um ponto de extremidade privado.</span><span class="sxs-lookup"><span data-stu-id="aa3ce-103">Creates a private endpoint.</span></span>

## <span data-ttu-id="aa3ce-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="aa3ce-104">SYNTAX</span></span>

### <span data-ttu-id="aa3ce-105">All</span><span class="sxs-lookup"><span data-stu-id="aa3ce-105">All</span></span>

```
New-AzPrivateEndpoint -Name <String> -ResourceGroupName <String> -Location <String> -Subnet <PSSubnet>
 -PrivateLinkServiceConnection <PSPrivateLinkServiceConnection[]> [-ByManualRequest] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa3ce-106">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="aa3ce-106">DESCRIPTION</span></span>

<span data-ttu-id="aa3ce-107">O cmdlet **New-AzPrivateEndpoint** cria um ponto de extremidade privado.</span><span class="sxs-lookup"><span data-stu-id="aa3ce-107">The **New-AzPrivateEndpoint** cmdlet creates a private endpoint.</span></span>

## <span data-ttu-id="aa3ce-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="aa3ce-108">EXAMPLES</span></span>

### <span data-ttu-id="aa3ce-109">Exemplo 1: Criar um ponto de extremidade privado</span><span class="sxs-lookup"><span data-stu-id="aa3ce-109">Example 1: Create a private endpoint</span></span>

<span data-ttu-id="aa3ce-110">O exemplo a seguir cria um ponto de extremidade privado com uma ID de serviço de link particular específica na sub-rede especificada em uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="aa3ce-110">The following example creates a private endpoint with a specific private link service ID in the specified subnet in a virtual network.</span></span>

```powershell
$virtualNetwork = Get-AzVirtualNetwork -ResourceName 'myVirtualNetwork' -ResourceGroupName 'myResourceGroup'
$subnet = $virtualNetwork | Select-Object -ExpandProperty subnets | Where-Object Name -eq 'mySubnet'
$plsConnection= New-AzPrivateLinkServiceConnection -Name 'MyPLSConnections' -PrivateLinkServiceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup/providers/Microsoft.Network/privateLinkServices/privateLinkService' -RequestMessage 'Please Approve my request'
New-AzPrivateEndpoint -Name 'MyPrivateEndpoint' -ResourceGroup 'myResourceGroup' -Location 'centralus' -PrivateLinkServiceConnection $plsConnection -Subnet $subnet
```

## <span data-ttu-id="aa3ce-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="aa3ce-111">PARAMETERS</span></span>

### <span data-ttu-id="aa3ce-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aa3ce-112">-AsJob</span></span>

<span data-ttu-id="aa3ce-113">Execute o cmdlet como um trabalho em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="aa3ce-113">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="aa3ce-114">-ByManualRequest</span><span class="sxs-lookup"><span data-stu-id="aa3ce-114">-ByManualRequest</span></span>

<span data-ttu-id="aa3ce-115">Use a solicitação manual para estabelecer a conexão.</span><span class="sxs-lookup"><span data-stu-id="aa3ce-115">Use manual request to establish the connection.</span></span>

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

### <span data-ttu-id="aa3ce-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa3ce-116">-DefaultProfile</span></span>

<span data-ttu-id="aa3ce-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="aa3ce-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa3ce-118">-Force</span><span class="sxs-lookup"><span data-stu-id="aa3ce-118">-Force</span></span>

<span data-ttu-id="aa3ce-119">Não peça confirmação para substituir um recurso.</span><span class="sxs-lookup"><span data-stu-id="aa3ce-119">Do not ask for confirmation to overwrite a resource.</span></span>

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

### <span data-ttu-id="aa3ce-120">-Location</span><span class="sxs-lookup"><span data-stu-id="aa3ce-120">-Location</span></span>

<span data-ttu-id="aa3ce-121">Especifica um local para o ponto de extremidade privado.</span><span class="sxs-lookup"><span data-stu-id="aa3ce-121">Specifies a location for the private endpoint.</span></span> <span data-ttu-id="aa3ce-122">Use [Get-AzLocation](/powershell/module/az.resources/get-azlocation) para determinar valores válidos para este parâmetro.</span><span class="sxs-lookup"><span data-stu-id="aa3ce-122">Use [Get-AzLocation](/powershell/module/az.resources/get-azlocation) to determine valid values for this parameter.</span></span>

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

### <span data-ttu-id="aa3ce-123">-Name</span><span class="sxs-lookup"><span data-stu-id="aa3ce-123">-Name</span></span>

<span data-ttu-id="aa3ce-124">Nome do ponto de extremidade privado.</span><span class="sxs-lookup"><span data-stu-id="aa3ce-124">Name of the private endpoint.</span></span>

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

### <span data-ttu-id="aa3ce-125">-PrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="aa3ce-125">-PrivateLinkServiceConnection</span></span>

<span data-ttu-id="aa3ce-126">A ID do recurso para conectar o ponto de extremidade privado.</span><span class="sxs-lookup"><span data-stu-id="aa3ce-126">The resource ID to connect the private endpoint.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceConnection[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa3ce-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa3ce-127">-ResourceGroupName</span></span>

<span data-ttu-id="aa3ce-128">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="aa3ce-128">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="aa3ce-129">-Sub-rede</span><span class="sxs-lookup"><span data-stu-id="aa3ce-129">-Subnet</span></span>

<span data-ttu-id="aa3ce-130">A sub-rede do ponto de extremidade privado.</span><span class="sxs-lookup"><span data-stu-id="aa3ce-130">The subnet of the private endpoint.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa3ce-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="aa3ce-131">-Tag</span></span>

<span data-ttu-id="aa3ce-132">Pares de valores-chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="aa3ce-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="aa3ce-133">Por exemplo: @{key0='value0';key1=$null;key2='value2'}</span><span class="sxs-lookup"><span data-stu-id="aa3ce-133">For example: @{key0='value0';key1=$null;key2='value2'}</span></span>

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

### <span data-ttu-id="aa3ce-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aa3ce-134">-Confirm</span></span>

<span data-ttu-id="aa3ce-135">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa3ce-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa3ce-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa3ce-136">-WhatIf</span></span>

<span data-ttu-id="aa3ce-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="aa3ce-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa3ce-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="aa3ce-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa3ce-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa3ce-139">CommonParameters</span></span>

<span data-ttu-id="aa3ce-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa3ce-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa3ce-141">Para obter mais informações, [consulte about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span><span class="sxs-lookup"><span data-stu-id="aa3ce-141">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>

## <span data-ttu-id="aa3ce-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aa3ce-142">INPUTS</span></span>

### <span data-ttu-id="aa3ce-143">System.String</span><span class="sxs-lookup"><span data-stu-id="aa3ce-143">System.String</span></span>

### <span data-ttu-id="aa3ce-144">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="aa3ce-144">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="aa3ce-145">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceConnection[]</span><span class="sxs-lookup"><span data-stu-id="aa3ce-145">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceConnection[]</span></span>

## <span data-ttu-id="aa3ce-146">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="aa3ce-146">OUTPUTS</span></span>

### <span data-ttu-id="aa3ce-147">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="aa3ce-147">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="aa3ce-148">NOTES</span><span class="sxs-lookup"><span data-stu-id="aa3ce-148">NOTES</span></span>

## <span data-ttu-id="aa3ce-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aa3ce-149">RELATED LINKS</span></span>

[<span data-ttu-id="aa3ce-150">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="aa3ce-150">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="aa3ce-151">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="aa3ce-151">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)

[<span data-ttu-id="aa3ce-152">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="aa3ce-152">New-AzPrivateLinkServiceConnection</span></span>](./New-AzPrivateLinkServiceConnection.md)