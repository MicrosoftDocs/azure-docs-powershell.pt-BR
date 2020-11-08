---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
ms.openlocfilehash: 2723ca0f5bebfbf65fefbfbd94fa995d544d9f71
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114364"
---
# <span data-ttu-id="4a8db-101">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="4a8db-101">New-AzPrivateLinkService</span></span>

## <span data-ttu-id="4a8db-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4a8db-102">SYNOPSIS</span></span>
<span data-ttu-id="4a8db-103">Cria um serviço de link privado</span><span class="sxs-lookup"><span data-stu-id="4a8db-103">Creates a private link service</span></span>

## <span data-ttu-id="4a8db-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4a8db-104">SYNTAX</span></span>

```
New-AzPrivateLinkService -Name <String> -ResourceGroupName <String> -Location <String>
 -LoadBalancerFrontendIpConfiguration <PSFrontendIPConfiguration[]>
 -IpConfiguration <PSPrivateLinkServiceIpConfiguration[]> [-Visibility <String[]>] [-AutoApproval <String[]>] [-EnableProxyProtocol]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4a8db-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4a8db-105">DESCRIPTION</span></span>
<span data-ttu-id="4a8db-106">O cmdlet **New-AzPrivateLinkService** cria um serviço de link privado</span><span class="sxs-lookup"><span data-stu-id="4a8db-106">The **New-AzPrivateLinkService** cmdlet creates a private link service</span></span>

## <span data-ttu-id="4a8db-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4a8db-107">EXAMPLES</span></span>

### <span data-ttu-id="4a8db-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4a8db-108">Example 1</span></span>

<span data-ttu-id="4a8db-109">O exemplo a seguir cria um serviço de link particular.</span><span class="sxs-lookup"><span data-stu-id="4a8db-109">The following example creates a private link service.</span></span>

```powershell
$vnet = Get-AzVirtualNetwork -ResourceName 'myvnet' -ResourceGroupName 'myresourcegroup'
# View the results of $vnet and change 'mysubnet' in the following line to the appropriate subnet name.
$subnet = $vnet | Select-Object -ExpandProperty subnets | Where-Object Name -eq 'mysubnet'
$IPConfig = New-AzPrivateLinkServiceIpConfig -Name 'IP-Config' -Subnet $subnet -PrivateIpAddress '10.0.0.5'
$publicip = Get-AzPublicIpAddress -ResourceGroupName 'myresourcegroup'
$frontend = New-AzLoadBalancerFrontendIpConfig -Name 'FrontendIpConfig01' -PublicIpAddress $publicip
$lb = New-AzLoadBalancer -Name 'MyLoadBalancer' -ResourceGroupName 'myresourcegroup' -Location 'West US' -FrontendIpConfiguration $frontend
New-AzPrivateLinkService -Name 'mypls' -ResourceGroupName myresourcegroup -Location "West US" -LoadBalancerFrontendIpConfiguration $frontend -IpConfiguration $IPConfig
```

## <span data-ttu-id="4a8db-110">OS</span><span class="sxs-lookup"><span data-stu-id="4a8db-110">PARAMETERS</span></span>

### <span data-ttu-id="4a8db-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4a8db-111">-AsJob</span></span>
<span data-ttu-id="4a8db-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="4a8db-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4a8db-113">-Aprovação automática</span><span class="sxs-lookup"><span data-stu-id="4a8db-113">-AutoApproval</span></span>
<span data-ttu-id="4a8db-114">Assinaturas de aprovação automática do serviço de link privado</span><span class="sxs-lookup"><span data-stu-id="4a8db-114">The auto approval subscriptions of private link service</span></span>

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

### <span data-ttu-id="4a8db-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a8db-115">-DefaultProfile</span></span>
<span data-ttu-id="4a8db-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4a8db-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a8db-117">-EnableProxyProtocol</span><span class="sxs-lookup"><span data-stu-id="4a8db-117">-EnableProxyProtocol</span></span>
<span data-ttu-id="4a8db-118">Habilite o protocolo proxy para o serviço de link privado.</span><span class="sxs-lookup"><span data-stu-id="4a8db-118">Enable proxy protocol for the private link service.</span></span>

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

### <span data-ttu-id="4a8db-119">-Force</span><span class="sxs-lookup"><span data-stu-id="4a8db-119">-Force</span></span>
<span data-ttu-id="4a8db-120">Não pedir confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="4a8db-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="4a8db-121">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="4a8db-121">-IpConfiguration</span></span>
<span data-ttu-id="4a8db-122">As configurações de IP</span><span class="sxs-lookup"><span data-stu-id="4a8db-122">The ip configurations</span></span>

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

### <span data-ttu-id="4a8db-123">-LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="4a8db-123">-LoadBalancerFrontendIpConfiguration</span></span>
<span data-ttu-id="4a8db-124">As configurações de front-end de IP</span><span class="sxs-lookup"><span data-stu-id="4a8db-124">The front end ip configurations</span></span>

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

### <span data-ttu-id="4a8db-125">-Local</span><span class="sxs-lookup"><span data-stu-id="4a8db-125">-Location</span></span>
<span data-ttu-id="4a8db-126">ponto.</span><span class="sxs-lookup"><span data-stu-id="4a8db-126">location.</span></span>

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

### <span data-ttu-id="4a8db-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="4a8db-127">-Name</span></span>
<span data-ttu-id="4a8db-128">O nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="4a8db-128">The name of the service.</span></span>

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

### <span data-ttu-id="4a8db-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a8db-129">-ResourceGroupName</span></span>
<span data-ttu-id="4a8db-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4a8db-130">The resource group name.</span></span>

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

### <span data-ttu-id="4a8db-131">-Marca</span><span class="sxs-lookup"><span data-stu-id="4a8db-131">-Tag</span></span>
<span data-ttu-id="4a8db-132">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="4a8db-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4a8db-133">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="4a8db-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="4a8db-134">-Visibilidade</span><span class="sxs-lookup"><span data-stu-id="4a8db-134">-Visibility</span></span>
<span data-ttu-id="4a8db-135">As assinaturas de visibilidade do serviço de link privado</span><span class="sxs-lookup"><span data-stu-id="4a8db-135">The visibility subscriptions of private link service</span></span>

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

### <span data-ttu-id="4a8db-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4a8db-136">-Confirm</span></span>
<span data-ttu-id="4a8db-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a8db-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a8db-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a8db-138">-WhatIf</span></span>
<span data-ttu-id="4a8db-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4a8db-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a8db-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4a8db-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a8db-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a8db-141">CommonParameters</span></span>
<span data-ttu-id="4a8db-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a8db-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a8db-143">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4a8db-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a8db-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4a8db-144">INPUTS</span></span>

### <span data-ttu-id="4a8db-145">System. String</span><span class="sxs-lookup"><span data-stu-id="4a8db-145">System.String</span></span>

### <span data-ttu-id="4a8db-146">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="4a8db-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="4a8db-147">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkServiceIpConfiguration []</span><span class="sxs-lookup"><span data-stu-id="4a8db-147">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration[]</span></span>

## <span data-ttu-id="4a8db-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4a8db-148">OUTPUTS</span></span>

### <span data-ttu-id="4a8db-149">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="4a8db-149">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="4a8db-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4a8db-150">NOTES</span></span>

## <span data-ttu-id="4a8db-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4a8db-151">RELATED LINKS</span></span>

[<span data-ttu-id="4a8db-152">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="4a8db-152">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="4a8db-153">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="4a8db-153">Remove-AzPrivateLinkService</span></span>](./Remove-AzPrivateLinkService.md)

[<span data-ttu-id="4a8db-154">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="4a8db-154">New-AzPrivateLinkServiceIpConfig</span></span>](./New-AzPrivateLinkServiceIpConfig.md)
