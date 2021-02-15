---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
ms.openlocfilehash: 2723ca0f5bebfbf65fefbfbd94fa995d544d9f71
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112811"
---
# <span data-ttu-id="0a607-101">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0a607-101">New-AzPrivateLinkService</span></span>

## <span data-ttu-id="0a607-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0a607-102">SYNOPSIS</span></span>
<span data-ttu-id="0a607-103">Cria um serviço de vinculação particular</span><span class="sxs-lookup"><span data-stu-id="0a607-103">Creates a private link service</span></span>

## <span data-ttu-id="0a607-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0a607-104">SYNTAX</span></span>

```
New-AzPrivateLinkService -Name <String> -ResourceGroupName <String> -Location <String>
 -LoadBalancerFrontendIpConfiguration <PSFrontendIPConfiguration[]>
 -IpConfiguration <PSPrivateLinkServiceIpConfiguration[]> [-Visibility <String[]>] [-AutoApproval <String[]>] [-EnableProxyProtocol]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0a607-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="0a607-105">DESCRIPTION</span></span>
<span data-ttu-id="0a607-106">O **cmdlet New-AzPrivateLinkService cria** um serviço de link particular</span><span class="sxs-lookup"><span data-stu-id="0a607-106">The **New-AzPrivateLinkService** cmdlet creates a private link service</span></span>

## <span data-ttu-id="0a607-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0a607-107">EXAMPLES</span></span>

### <span data-ttu-id="0a607-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0a607-108">Example 1</span></span>

<span data-ttu-id="0a607-109">O exemplo a seguir cria um serviço de vinculação particular.</span><span class="sxs-lookup"><span data-stu-id="0a607-109">The following example creates a private link service.</span></span>

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

## <span data-ttu-id="0a607-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0a607-110">PARAMETERS</span></span>

### <span data-ttu-id="0a607-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0a607-111">-AsJob</span></span>
<span data-ttu-id="0a607-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="0a607-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0a607-113">-Aprovação Automática</span><span class="sxs-lookup"><span data-stu-id="0a607-113">-AutoApproval</span></span>
<span data-ttu-id="0a607-114">As assinaturas de aprovação automática do serviço de link particular</span><span class="sxs-lookup"><span data-stu-id="0a607-114">The auto approval subscriptions of private link service</span></span>

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

### <span data-ttu-id="0a607-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a607-115">-DefaultProfile</span></span>
<span data-ttu-id="0a607-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0a607-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a607-117">-EnableProxyProtocol</span><span class="sxs-lookup"><span data-stu-id="0a607-117">-EnableProxyProtocol</span></span>
<span data-ttu-id="0a607-118">Habilitar o protocolo proxy para o serviço de link privado.</span><span class="sxs-lookup"><span data-stu-id="0a607-118">Enable proxy protocol for the private link service.</span></span>

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

### <span data-ttu-id="0a607-119">-Forçar</span><span class="sxs-lookup"><span data-stu-id="0a607-119">-Force</span></span>
<span data-ttu-id="0a607-120">Não peça confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="0a607-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="0a607-121">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a607-121">-IpConfiguration</span></span>
<span data-ttu-id="0a607-122">As configurações de ip</span><span class="sxs-lookup"><span data-stu-id="0a607-122">The ip configurations</span></span>

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

### <span data-ttu-id="0a607-123">-LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a607-123">-LoadBalancerFrontendIpConfiguration</span></span>
<span data-ttu-id="0a607-124">As configurações de ip front-end</span><span class="sxs-lookup"><span data-stu-id="0a607-124">The front end ip configurations</span></span>

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

### <span data-ttu-id="0a607-125">-Local</span><span class="sxs-lookup"><span data-stu-id="0a607-125">-Location</span></span>
<span data-ttu-id="0a607-126">Localização.</span><span class="sxs-lookup"><span data-stu-id="0a607-126">location.</span></span>

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

### <span data-ttu-id="0a607-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="0a607-127">-Name</span></span>
<span data-ttu-id="0a607-128">O nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="0a607-128">The name of the service.</span></span>

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

### <span data-ttu-id="0a607-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a607-129">-ResourceGroupName</span></span>
<span data-ttu-id="0a607-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0a607-130">The resource group name.</span></span>

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

### <span data-ttu-id="0a607-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="0a607-131">-Tag</span></span>
<span data-ttu-id="0a607-132">Pares de valor-chave na forma de uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="0a607-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0a607-133">Por exemplo: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="0a607-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="0a607-134">-Visibilidade</span><span class="sxs-lookup"><span data-stu-id="0a607-134">-Visibility</span></span>
<span data-ttu-id="0a607-135">As assinaturas de visibilidade do serviço de link privado</span><span class="sxs-lookup"><span data-stu-id="0a607-135">The visibility subscriptions of private link service</span></span>

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

### <span data-ttu-id="0a607-136">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="0a607-136">-Confirm</span></span>
<span data-ttu-id="0a607-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a607-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a607-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a607-138">-WhatIf</span></span>
<span data-ttu-id="0a607-139">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="0a607-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a607-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0a607-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a607-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a607-141">CommonParameters</span></span>
<span data-ttu-id="0a607-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a607-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a607-143">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0a607-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a607-144">Entradas</span><span class="sxs-lookup"><span data-stu-id="0a607-144">INPUTS</span></span>

### <span data-ttu-id="0a607-145">System.String</span><span class="sxs-lookup"><span data-stu-id="0a607-145">System.String</span></span>

### <span data-ttu-id="0a607-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="0a607-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="0a607-147">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="0a607-147">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration[]</span></span>

## <span data-ttu-id="0a607-148">Saídas</span><span class="sxs-lookup"><span data-stu-id="0a607-148">OUTPUTS</span></span>

### <span data-ttu-id="0a607-149">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0a607-149">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="0a607-150">Notas</span><span class="sxs-lookup"><span data-stu-id="0a607-150">NOTES</span></span>

## <span data-ttu-id="0a607-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0a607-151">RELATED LINKS</span></span>

[<span data-ttu-id="0a607-152">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0a607-152">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="0a607-153">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0a607-153">Remove-AzPrivateLinkService</span></span>](./Remove-AzPrivateLinkService.md)

[<span data-ttu-id="0a607-154">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="0a607-154">New-AzPrivateLinkServiceIpConfig</span></span>](./New-AzPrivateLinkServiceIpConfig.md)
