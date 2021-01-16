---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateEndpoint.md
ms.openlocfilehash: df298b41ea1efa4915cb7556b9fd07b1d8f3e2de
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429557"
---
# <span data-ttu-id="373d2-101">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="373d2-101">New-AzPrivateEndpoint</span></span>

## <span data-ttu-id="373d2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="373d2-102">SYNOPSIS</span></span>
<span data-ttu-id="373d2-103">Cria um ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="373d2-103">Creates a private endpoint.</span></span>

## <span data-ttu-id="373d2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="373d2-104">SYNTAX</span></span>

### <span data-ttu-id="373d2-105">Todo</span><span class="sxs-lookup"><span data-stu-id="373d2-105">All</span></span>

```
New-AzPrivateEndpoint -Name <String> -ResourceGroupName <String> -Location <String> -Subnet <PSSubnet>
 -PrivateLinkServiceConnection <PSPrivateLinkServiceConnection[]> [-ByManualRequest] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="373d2-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="373d2-106">DESCRIPTION</span></span>

<span data-ttu-id="373d2-107">O cmdlet **New-AzPrivateEndpoint** cria um ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="373d2-107">The **New-AzPrivateEndpoint** cmdlet creates a private endpoint.</span></span>

## <span data-ttu-id="373d2-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="373d2-108">EXAMPLES</span></span>

### <span data-ttu-id="373d2-109">Exemplo 1: criar um ponto de extremidade privado</span><span class="sxs-lookup"><span data-stu-id="373d2-109">Example 1: Create a private endpoint</span></span>

<span data-ttu-id="373d2-110">O exemplo a seguir cria um ponto de extremidade particular com uma ID de serviço de link particular específico na sub-rede especificada em uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="373d2-110">The following example creates a private endpoint with a specific private link service ID in the specified subnet in a virtual network.</span></span>

```powershell
$virtualNetwork = Get-AzVirtualNetwork -ResourceName 'myVirtualNetwork' -ResourceGroupName 'myResourceGroup'
$subnet = $virtualNetwork | Select-Object -ExpandProperty subnets | Where-Object Name -eq 'mySubnet'
$plsConnection= New-AzPrivateLinkServiceConnection -Name 'MyPLSConnections' -PrivateLinkServiceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup/providers/Microsoft.Network/privateLinkServices/privateLinkService' -RequestMessage 'Please Approve my request'
New-AzPrivateEndpoint -Name 'MyPrivateEndpoint' -ResourceGroup 'myResourceGroup' -Location 'centralus' -PrivateLinkServiceConnection $plsConnection -Subnet $subnet
```

## <span data-ttu-id="373d2-111">OS</span><span class="sxs-lookup"><span data-stu-id="373d2-111">PARAMETERS</span></span>

### <span data-ttu-id="373d2-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="373d2-112">-AsJob</span></span>

<span data-ttu-id="373d2-113">Executar o cmdlet como um trabalho em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="373d2-113">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="373d2-114">-ByManualRequest</span><span class="sxs-lookup"><span data-stu-id="373d2-114">-ByManualRequest</span></span>

<span data-ttu-id="373d2-115">Use a solicitação manual para estabelecer a conexão.</span><span class="sxs-lookup"><span data-stu-id="373d2-115">Use manual request to establish the connection.</span></span>

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

### <span data-ttu-id="373d2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="373d2-116">-DefaultProfile</span></span>

<span data-ttu-id="373d2-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="373d2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="373d2-118">-Force</span><span class="sxs-lookup"><span data-stu-id="373d2-118">-Force</span></span>

<span data-ttu-id="373d2-119">Não peça confirmação para substituir um recurso.</span><span class="sxs-lookup"><span data-stu-id="373d2-119">Do not ask for confirmation to overwrite a resource.</span></span>

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

### <span data-ttu-id="373d2-120">-Local</span><span class="sxs-lookup"><span data-stu-id="373d2-120">-Location</span></span>

<span data-ttu-id="373d2-121">Especifica um local para o ponto de extremidade privado.</span><span class="sxs-lookup"><span data-stu-id="373d2-121">Specifies a location for the private endpoint.</span></span> <span data-ttu-id="373d2-122">Use [Get-AzLocation](/powershell/module/az.resources/get-azlocation) para determinar valores válidos para esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="373d2-122">Use [Get-AzLocation](/powershell/module/az.resources/get-azlocation) to determine valid values for this parameter.</span></span>

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

### <span data-ttu-id="373d2-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="373d2-123">-Name</span></span>

<span data-ttu-id="373d2-124">Nome do ponto de extremidade privado.</span><span class="sxs-lookup"><span data-stu-id="373d2-124">Name of the private endpoint.</span></span>

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

### <span data-ttu-id="373d2-125">-PrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="373d2-125">-PrivateLinkServiceConnection</span></span>

<span data-ttu-id="373d2-126">A ID do recurso para conectar o ponto de extremidade privado.</span><span class="sxs-lookup"><span data-stu-id="373d2-126">The resource ID to connect the private endpoint.</span></span>

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

### <span data-ttu-id="373d2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="373d2-127">-ResourceGroupName</span></span>

<span data-ttu-id="373d2-128">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="373d2-128">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="373d2-129">-Subnet</span><span class="sxs-lookup"><span data-stu-id="373d2-129">-Subnet</span></span>

<span data-ttu-id="373d2-130">A sub-rede do ponto de extremidade privado.</span><span class="sxs-lookup"><span data-stu-id="373d2-130">The subnet of the private endpoint.</span></span>

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

### <span data-ttu-id="373d2-131">-Marca</span><span class="sxs-lookup"><span data-stu-id="373d2-131">-Tag</span></span>

<span data-ttu-id="373d2-132">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="373d2-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="373d2-133">Por exemplo: @ {Key0 = ' value0 '; key1 = $null; Key2 = ' value2 '}</span><span class="sxs-lookup"><span data-stu-id="373d2-133">For example: @{key0='value0';key1=$null;key2='value2'}</span></span>

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

### <span data-ttu-id="373d2-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="373d2-134">-Confirm</span></span>

<span data-ttu-id="373d2-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="373d2-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="373d2-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="373d2-136">-WhatIf</span></span>

<span data-ttu-id="373d2-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="373d2-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="373d2-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="373d2-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="373d2-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="373d2-139">CommonParameters</span></span>

<span data-ttu-id="373d2-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="373d2-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="373d2-141">Para obter mais informações, consulte [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span><span class="sxs-lookup"><span data-stu-id="373d2-141">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>

## <span data-ttu-id="373d2-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="373d2-142">INPUTS</span></span>

### <span data-ttu-id="373d2-143">System. String</span><span class="sxs-lookup"><span data-stu-id="373d2-143">System.String</span></span>

### <span data-ttu-id="373d2-144">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="373d2-144">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="373d2-145">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkServiceConnection []</span><span class="sxs-lookup"><span data-stu-id="373d2-145">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceConnection[]</span></span>

## <span data-ttu-id="373d2-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="373d2-146">OUTPUTS</span></span>

### <span data-ttu-id="373d2-147">Microsoft. Azure. Commands. Network. Models. PSPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="373d2-147">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="373d2-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="373d2-148">NOTES</span></span>

## <span data-ttu-id="373d2-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="373d2-149">RELATED LINKS</span></span>

[<span data-ttu-id="373d2-150">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="373d2-150">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="373d2-151">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="373d2-151">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)

[<span data-ttu-id="373d2-152">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="373d2-152">New-AzPrivateLinkServiceConnection</span></span>](./New-AzPrivateLinkServiceConnection.md)