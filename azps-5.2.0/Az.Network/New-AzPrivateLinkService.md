---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
ms.openlocfilehash: 2723ca0f5bebfbf65fefbfbd94fa995d544d9f71
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98257829"
---
# <span data-ttu-id="b6a5e-101">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="b6a5e-101">New-AzPrivateLinkService</span></span>

## <span data-ttu-id="b6a5e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b6a5e-102">SYNOPSIS</span></span>
<span data-ttu-id="b6a5e-103">Cria um serviço de link privado</span><span class="sxs-lookup"><span data-stu-id="b6a5e-103">Creates a private link service</span></span>

## <span data-ttu-id="b6a5e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b6a5e-104">SYNTAX</span></span>

```
New-AzPrivateLinkService -Name <String> -ResourceGroupName <String> -Location <String>
 -LoadBalancerFrontendIpConfiguration <PSFrontendIPConfiguration[]>
 -IpConfiguration <PSPrivateLinkServiceIpConfiguration[]> [-Visibility <String[]>] [-AutoApproval <String[]>] [-EnableProxyProtocol]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b6a5e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b6a5e-105">DESCRIPTION</span></span>
<span data-ttu-id="b6a5e-106">O cmdlet **New-AzPrivateLinkService** cria um serviço de link privado</span><span class="sxs-lookup"><span data-stu-id="b6a5e-106">The **New-AzPrivateLinkService** cmdlet creates a private link service</span></span>

## <span data-ttu-id="b6a5e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b6a5e-107">EXAMPLES</span></span>

### <span data-ttu-id="b6a5e-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b6a5e-108">Example 1</span></span>

<span data-ttu-id="b6a5e-109">O exemplo a seguir cria um serviço de link particular.</span><span class="sxs-lookup"><span data-stu-id="b6a5e-109">The following example creates a private link service.</span></span>

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

## <span data-ttu-id="b6a5e-110">OS</span><span class="sxs-lookup"><span data-stu-id="b6a5e-110">PARAMETERS</span></span>

### <span data-ttu-id="b6a5e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b6a5e-111">-AsJob</span></span>
<span data-ttu-id="b6a5e-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="b6a5e-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b6a5e-113">-Aprovação automática</span><span class="sxs-lookup"><span data-stu-id="b6a5e-113">-AutoApproval</span></span>
<span data-ttu-id="b6a5e-114">Assinaturas de aprovação automática do serviço de link privado</span><span class="sxs-lookup"><span data-stu-id="b6a5e-114">The auto approval subscriptions of private link service</span></span>

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

### <span data-ttu-id="b6a5e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6a5e-115">-DefaultProfile</span></span>
<span data-ttu-id="b6a5e-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b6a5e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6a5e-117">-EnableProxyProtocol</span><span class="sxs-lookup"><span data-stu-id="b6a5e-117">-EnableProxyProtocol</span></span>
<span data-ttu-id="b6a5e-118">Habilite o protocolo proxy para o serviço de link privado.</span><span class="sxs-lookup"><span data-stu-id="b6a5e-118">Enable proxy protocol for the private link service.</span></span>

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

### <span data-ttu-id="b6a5e-119">-Force</span><span class="sxs-lookup"><span data-stu-id="b6a5e-119">-Force</span></span>
<span data-ttu-id="b6a5e-120">Não pedir confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="b6a5e-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="b6a5e-121">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="b6a5e-121">-IpConfiguration</span></span>
<span data-ttu-id="b6a5e-122">As configurações de IP</span><span class="sxs-lookup"><span data-stu-id="b6a5e-122">The ip configurations</span></span>

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

### <span data-ttu-id="b6a5e-123">-LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="b6a5e-123">-LoadBalancerFrontendIpConfiguration</span></span>
<span data-ttu-id="b6a5e-124">As configurações de front-end de IP</span><span class="sxs-lookup"><span data-stu-id="b6a5e-124">The front end ip configurations</span></span>

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

### <span data-ttu-id="b6a5e-125">-Local</span><span class="sxs-lookup"><span data-stu-id="b6a5e-125">-Location</span></span>
<span data-ttu-id="b6a5e-126">ponto.</span><span class="sxs-lookup"><span data-stu-id="b6a5e-126">location.</span></span>

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

### <span data-ttu-id="b6a5e-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="b6a5e-127">-Name</span></span>
<span data-ttu-id="b6a5e-128">O nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="b6a5e-128">The name of the service.</span></span>

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

### <span data-ttu-id="b6a5e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6a5e-129">-ResourceGroupName</span></span>
<span data-ttu-id="b6a5e-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b6a5e-130">The resource group name.</span></span>

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

### <span data-ttu-id="b6a5e-131">-Marca</span><span class="sxs-lookup"><span data-stu-id="b6a5e-131">-Tag</span></span>
<span data-ttu-id="b6a5e-132">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="b6a5e-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b6a5e-133">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="b6a5e-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="b6a5e-134">-Visibilidade</span><span class="sxs-lookup"><span data-stu-id="b6a5e-134">-Visibility</span></span>
<span data-ttu-id="b6a5e-135">As assinaturas de visibilidade do serviço de link privado</span><span class="sxs-lookup"><span data-stu-id="b6a5e-135">The visibility subscriptions of private link service</span></span>

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

### <span data-ttu-id="b6a5e-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b6a5e-136">-Confirm</span></span>
<span data-ttu-id="b6a5e-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6a5e-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6a5e-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6a5e-138">-WhatIf</span></span>
<span data-ttu-id="b6a5e-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b6a5e-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6a5e-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b6a5e-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6a5e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6a5e-141">CommonParameters</span></span>
<span data-ttu-id="b6a5e-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6a5e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6a5e-143">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b6a5e-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6a5e-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b6a5e-144">INPUTS</span></span>

### <span data-ttu-id="b6a5e-145">System. String</span><span class="sxs-lookup"><span data-stu-id="b6a5e-145">System.String</span></span>

### <span data-ttu-id="b6a5e-146">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="b6a5e-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="b6a5e-147">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkServiceIpConfiguration []</span><span class="sxs-lookup"><span data-stu-id="b6a5e-147">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration[]</span></span>

## <span data-ttu-id="b6a5e-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b6a5e-148">OUTPUTS</span></span>

### <span data-ttu-id="b6a5e-149">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="b6a5e-149">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="b6a5e-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b6a5e-150">NOTES</span></span>

## <span data-ttu-id="b6a5e-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b6a5e-151">RELATED LINKS</span></span>

[<span data-ttu-id="b6a5e-152">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="b6a5e-152">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="b6a5e-153">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="b6a5e-153">Remove-AzPrivateLinkService</span></span>](./Remove-AzPrivateLinkService.md)

[<span data-ttu-id="b6a5e-154">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="b6a5e-154">New-AzPrivateLinkServiceIpConfig</span></span>](./New-AzPrivateLinkServiceIpConfig.md)
