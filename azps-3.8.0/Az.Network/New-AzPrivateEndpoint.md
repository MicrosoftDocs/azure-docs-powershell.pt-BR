---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateEndpoint.md
ms.openlocfilehash: 6e83def7c4956e4936e8e3c55f96aab1da0d451d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941770"
---
# <span data-ttu-id="b7cdd-101">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="b7cdd-101">New-AzPrivateEndpoint</span></span>

## <span data-ttu-id="b7cdd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b7cdd-102">SYNOPSIS</span></span>
<span data-ttu-id="b7cdd-103">Cria um ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="b7cdd-103">Creates a private endpoint.</span></span>

## <span data-ttu-id="b7cdd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b7cdd-104">SYNTAX</span></span>

```
New-AzPrivateEndpoint -Name <String> -ResourceGroupName <String> -Location <String> -Subnet <PSSubnet>
 -PrivateLinkServiceConnection <PSPrivateLinkServiceConnection[]> [-ByManualRequest] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7cdd-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b7cdd-105">DESCRIPTION</span></span>
<span data-ttu-id="b7cdd-106">O cmdlet **New-AzPrivateEndpoint** cria um ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="b7cdd-106">The **New-AzPrivateEndpoint** cmdlet creates a private endpoint.</span></span>

## <span data-ttu-id="b7cdd-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b7cdd-107">EXAMPLES</span></span>

### <span data-ttu-id="b7cdd-108">1: criar um ponto de extremidade privado</span><span class="sxs-lookup"><span data-stu-id="b7cdd-108">1: Create a private endpoint</span></span>
```
$virtualNetwork = Get-AzVirtualNetwork -ResourceName MyVirtualNetwork -ResourceGroupName TestResourceGroup
$plsConnection= New-AzPrivateLinkServiceConnection -Name MyPLSConnections -PrivateLinkServiceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/privateLinkServices/privateLinkService" -RequestMessage "Please Approve my request"
New-AzPrivateEndpoint -Name MyPrivateEndpoint -ResourceGroup TestResourceGroup -Location centralus -PrivateLinkServiceConnection $plsConnection -Subnet $virtualNetwork.Subnets[0]
```

<span data-ttu-id="b7cdd-109">Este exemplo cria um ponto de extremidade particular com ID de serviço de link particular específico em uma sub-rede específica em uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="b7cdd-109">This example creates a private endpoint with specific private link service id in a specific subnet in a virtual network.</span></span>

## <span data-ttu-id="b7cdd-110">OS</span><span class="sxs-lookup"><span data-stu-id="b7cdd-110">PARAMETERS</span></span>

### <span data-ttu-id="b7cdd-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b7cdd-111">-AsJob</span></span>
<span data-ttu-id="b7cdd-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="b7cdd-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b7cdd-113">-ByManualRequest</span><span class="sxs-lookup"><span data-stu-id="b7cdd-113">-ByManualRequest</span></span>
<span data-ttu-id="b7cdd-114">Usando a solicitação manual.</span><span class="sxs-lookup"><span data-stu-id="b7cdd-114">Using manual request.</span></span>

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

### <span data-ttu-id="b7cdd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7cdd-115">-DefaultProfile</span></span>
<span data-ttu-id="b7cdd-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b7cdd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7cdd-117">-Force</span><span class="sxs-lookup"><span data-stu-id="b7cdd-117">-Force</span></span>
<span data-ttu-id="b7cdd-118">Não pedir confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="b7cdd-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="b7cdd-119">-Local</span><span class="sxs-lookup"><span data-stu-id="b7cdd-119">-Location</span></span>
<span data-ttu-id="b7cdd-120">ponto.</span><span class="sxs-lookup"><span data-stu-id="b7cdd-120">location.</span></span>

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

### <span data-ttu-id="b7cdd-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="b7cdd-121">-Name</span></span>
<span data-ttu-id="b7cdd-122">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="b7cdd-122">The resource name.</span></span>

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

### <span data-ttu-id="b7cdd-123">-PrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="b7cdd-123">-PrivateLinkServiceConnection</span></span>
<span data-ttu-id="b7cdd-124">A conexão do serviço de link privado.</span><span class="sxs-lookup"><span data-stu-id="b7cdd-124">The private link service connection.</span></span>

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

### <span data-ttu-id="b7cdd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7cdd-125">-ResourceGroupName</span></span>
<span data-ttu-id="b7cdd-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b7cdd-126">The resource group name.</span></span>

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

### <span data-ttu-id="b7cdd-127">-Subnet</span><span class="sxs-lookup"><span data-stu-id="b7cdd-127">-Subnet</span></span>
<span data-ttu-id="b7cdd-128">A sub-rede do ponto de extremidade privado</span><span class="sxs-lookup"><span data-stu-id="b7cdd-128">The subnet of the private endpoint</span></span>

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

### <span data-ttu-id="b7cdd-129">-Marca</span><span class="sxs-lookup"><span data-stu-id="b7cdd-129">-Tag</span></span>
<span data-ttu-id="b7cdd-130">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="b7cdd-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b7cdd-131">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="b7cdd-131">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="b7cdd-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b7cdd-132">-Confirm</span></span>
<span data-ttu-id="b7cdd-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7cdd-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7cdd-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7cdd-134">-WhatIf</span></span>
<span data-ttu-id="b7cdd-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b7cdd-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7cdd-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b7cdd-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7cdd-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7cdd-137">CommonParameters</span></span>
<span data-ttu-id="b7cdd-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7cdd-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7cdd-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b7cdd-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7cdd-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b7cdd-140">INPUTS</span></span>

### <span data-ttu-id="b7cdd-141">System. String</span><span class="sxs-lookup"><span data-stu-id="b7cdd-141">System.String</span></span>

### <span data-ttu-id="b7cdd-142">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="b7cdd-142">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="b7cdd-143">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkServiceConnection []</span><span class="sxs-lookup"><span data-stu-id="b7cdd-143">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceConnection[]</span></span>

## <span data-ttu-id="b7cdd-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b7cdd-144">OUTPUTS</span></span>

### <span data-ttu-id="b7cdd-145">Microsoft. Azure. Commands. Network. Models. PSPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="b7cdd-145">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="b7cdd-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b7cdd-146">NOTES</span></span>

## <span data-ttu-id="b7cdd-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b7cdd-147">RELATED LINKS</span></span>

[<span data-ttu-id="b7cdd-148">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="b7cdd-148">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="b7cdd-149">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="b7cdd-149">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)

[<span data-ttu-id="b7cdd-150">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="b7cdd-150">New-AzPrivateLinkServiceConnection</span></span>](./New-AzPrivateLinkServiceConnection.md)