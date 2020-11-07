---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
ms.openlocfilehash: 75c8f7b52fec0e429820d43f86a8a41798b1d5f7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771600"
---
# <span data-ttu-id="d3715-101">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d3715-101">New-AzPrivateLinkService</span></span>

## <span data-ttu-id="d3715-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d3715-102">SYNOPSIS</span></span>
<span data-ttu-id="d3715-103">Cria um serviço de link privado</span><span class="sxs-lookup"><span data-stu-id="d3715-103">Creates a private link service</span></span>

## <span data-ttu-id="d3715-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d3715-104">SYNTAX</span></span>

```
New-AzPrivateLinkService -Name <String> -ResourceGroupName <String> -Location <String>
 -LoadBalancerFrontendIpConfiguration <PSFrontendIPConfiguration[]>
 -IpConfiguration <PSPrivateLinkServiceIpConfiguration[]> [-Visibility <String[]>] [-AutoApproval <String[]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d3715-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d3715-105">DESCRIPTION</span></span>
<span data-ttu-id="d3715-106">O cmdlet **New-AzPrivateLinkService** cria um serviço de link privado</span><span class="sxs-lookup"><span data-stu-id="d3715-106">The **New-AzPrivateLinkService** cmdlet creates a private link service</span></span>

## <span data-ttu-id="d3715-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d3715-107">EXAMPLES</span></span>

### <span data-ttu-id="d3715-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d3715-108">Example 1</span></span>
```
$vnet = Get-AzVirtualNetwork -ResourceName "myvnet" -ResourceGroupName "myresourcegroup"
$IPConfig = New-AzPrivateLinkServiceIpConfig -Name "IP-Config" -Subnet $vnet.subnets[1] -PrivateIpAddress "10.0.0.5"
$publicip = Get-AzPublicIpAddress -ResourceGroupName "myresourcegroup"
$frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
$lb = New-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myresourcegroup" -Location "West US" -FrontendIpConfiguration $frontend  
New-AzPrivateLinkService -Name "mypls" -ResourceGroupName myresourcegroup -Location "West US" -LoadBalancerFrontendIpConfiguration $frontend -IpConfiguration $IPConfig
```

<span data-ttu-id="d3715-109">Este exemplo cria um serviço de link particular.</span><span class="sxs-lookup"><span data-stu-id="d3715-109">This example creates a private link service.</span></span>

## <span data-ttu-id="d3715-110">OS</span><span class="sxs-lookup"><span data-stu-id="d3715-110">PARAMETERS</span></span>

### <span data-ttu-id="d3715-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d3715-111">-AsJob</span></span>
<span data-ttu-id="d3715-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="d3715-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d3715-113">-Aprovação automática</span><span class="sxs-lookup"><span data-stu-id="d3715-113">-AutoApproval</span></span>
<span data-ttu-id="d3715-114">Assinaturas de aprovação automática do serviço de link privado</span><span class="sxs-lookup"><span data-stu-id="d3715-114">The auto approval subscriptions of private link service</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3715-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3715-115">-DefaultProfile</span></span>
<span data-ttu-id="d3715-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d3715-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3715-117">-Force</span><span class="sxs-lookup"><span data-stu-id="d3715-117">-Force</span></span>
<span data-ttu-id="d3715-118">Não pedir confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="d3715-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="d3715-119">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="d3715-119">-IpConfiguration</span></span>
<span data-ttu-id="d3715-120">As configurações de IP</span><span class="sxs-lookup"><span data-stu-id="d3715-120">The ip configurations</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3715-121">-LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="d3715-121">-LoadBalancerFrontendIpConfiguration</span></span>
<span data-ttu-id="d3715-122">As configurações de front-end de IP</span><span class="sxs-lookup"><span data-stu-id="d3715-122">The front end ip configurations</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3715-123">-Local</span><span class="sxs-lookup"><span data-stu-id="d3715-123">-Location</span></span>
<span data-ttu-id="d3715-124">ponto.</span><span class="sxs-lookup"><span data-stu-id="d3715-124">location.</span></span>

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

### <span data-ttu-id="d3715-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="d3715-125">-Name</span></span>
<span data-ttu-id="d3715-126">O nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="d3715-126">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3715-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3715-127">-ResourceGroupName</span></span>
<span data-ttu-id="d3715-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d3715-128">The resource group name.</span></span>

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

### <span data-ttu-id="d3715-129">-Marca</span><span class="sxs-lookup"><span data-stu-id="d3715-129">-Tag</span></span>
<span data-ttu-id="d3715-130">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="d3715-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d3715-131">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="d3715-131">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="d3715-132">-Visibilidade</span><span class="sxs-lookup"><span data-stu-id="d3715-132">-Visibility</span></span>
<span data-ttu-id="d3715-133">As assinaturas de visibilidade do serviço de link privado</span><span class="sxs-lookup"><span data-stu-id="d3715-133">The visibility subscriptions of private link service</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3715-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d3715-134">-Confirm</span></span>
<span data-ttu-id="d3715-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3715-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3715-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3715-136">-WhatIf</span></span>
<span data-ttu-id="d3715-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d3715-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3715-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d3715-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3715-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3715-139">CommonParameters</span></span>
<span data-ttu-id="d3715-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3715-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3715-141">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d3715-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3715-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d3715-142">INPUTS</span></span>

### <span data-ttu-id="d3715-143">System. String</span><span class="sxs-lookup"><span data-stu-id="d3715-143">System.String</span></span>

### <span data-ttu-id="d3715-144">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="d3715-144">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="d3715-145">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkServiceIpConfiguration []</span><span class="sxs-lookup"><span data-stu-id="d3715-145">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration[]</span></span>

## <span data-ttu-id="d3715-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d3715-146">OUTPUTS</span></span>

### <span data-ttu-id="d3715-147">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d3715-147">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="d3715-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d3715-148">NOTES</span></span>

## <span data-ttu-id="d3715-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d3715-149">RELATED LINKS</span></span>

[<span data-ttu-id="d3715-150">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d3715-150">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="d3715-151">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d3715-151">Remove-AzPrivateLinkService</span></span>](./Remove-AzPrivateLinkService.md)

[<span data-ttu-id="d3715-152">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="d3715-152">New-AzPrivateLinkServiceIpConfig</span></span>](./New-AzPrivateLinkServiceIpConfig.md)
