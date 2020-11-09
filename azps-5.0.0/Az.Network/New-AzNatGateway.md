---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznatgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNatGateway.md
ms.openlocfilehash: 0855ba4e7e16503045d13c370838cd5d3fffb033
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94283871"
---
# <span data-ttu-id="5d610-101">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="5d610-101">New-AzNatGateway</span></span>

## <span data-ttu-id="5d610-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5d610-102">SYNOPSIS</span></span>
<span data-ttu-id="5d610-103">Criar novo recurso de gateway NAT com o endereço IP público/prefixo de IP público, IdleTimeoutInMinutes e SKU.</span><span class="sxs-lookup"><span data-stu-id="5d610-103">Create new Nat Gateway resource with properties Public Ip Address/Public Ip Prefix, IdleTimeoutInMinutes and Sku.</span></span>

## <span data-ttu-id="5d610-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5d610-104">SYNTAX</span></span>

```
New-AzNatGateway -ResourceGroupName <String> -Name <String> [-IdleTimeoutInMinutes <Int32>] [-Zone <String[]>]
 [-Sku <String>] [-Location <String>] [-Tag <Hashtable>] [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d610-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5d610-105">DESCRIPTION</span></span>
<span data-ttu-id="5d610-106">O cmdlet **New-AzNatGateway** cria um recurso de gateway NAT.</span><span class="sxs-lookup"><span data-stu-id="5d610-106">The **New-AzNatGateway** cmdlet creates a Nat Gateway Resource.</span></span> <span data-ttu-id="5d610-107">Um natgateway requer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="5d610-107">A natgateway requires the following:</span></span> 
- <span data-ttu-id="5d610-108">Endereço IP público e/ou prefixo de IP público</span><span class="sxs-lookup"><span data-stu-id="5d610-108">Public Ip Address and/or Public Ip Prefix</span></span>
- <span data-ttu-id="5d610-109">IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="5d610-109">IdleTimeoutInMinutes</span></span> 
- <span data-ttu-id="5d610-110">SKU</span><span class="sxs-lookup"><span data-stu-id="5d610-110">Sku</span></span>
- <span data-ttu-id="5d610-111">ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d610-111">ResourceGroupName</span></span>
- <span data-ttu-id="5d610-112">Source</span><span class="sxs-lookup"><span data-stu-id="5d610-112">ResourceName</span></span>
- <span data-ttu-id="5d610-113">Ponto</span><span class="sxs-lookup"><span data-stu-id="5d610-113">Location</span></span>

## <span data-ttu-id="5d610-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5d610-114">EXAMPLES</span></span>

### <span data-ttu-id="5d610-115">Exemplo 1: criar gateway NAT com endereço IP público</span><span class="sxs-lookup"><span data-stu-id="5d610-115">Example 1: Create Nat Gateway with Public Ip Address</span></span>
```powershell
PS C:> $pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip
```

### <span data-ttu-id="5d610-116">Exemplo 2: criar o gateway NAT com prefixo de IP público</span><span class="sxs-lookup"><span data-stu-id="5d610-116">Example 2: Create Nat Gateway with Public Ip Prefix</span></span>
```powershell
PS C:> $publicipprefix = New-AzPublicIpPrefix -Name "prefix2" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -PrefixLength "31"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpPrefix $publicipprefix
```

### <span data-ttu-id="5d610-117">Exemplo 3: criar o gateway NAT com o endereço IP público na zona de disponibilidade 1</span><span class="sxs-lookup"><span data-stu-id="5d610-117">Example 3: Create Nat Gateway with Public IP Address in Availability Zone 1</span></span>
```powershell
PS C:> $pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip -Zone "1"
```

<span data-ttu-id="5d610-118">O primeiro comando cria um endereço IP público padrão.</span><span class="sxs-lookup"><span data-stu-id="5d610-118">The first command creates standard Public IP Address.</span></span>
<span data-ttu-id="5d610-119">O segundo comando cria o gateway NAT com o endereço IP público na zona de disponibilidade 1.</span><span class="sxs-lookup"><span data-stu-id="5d610-119">The second command creates NAT Gateway with Public IP Address in Availability Zone 1.</span></span>

## <span data-ttu-id="5d610-120">OS</span><span class="sxs-lookup"><span data-stu-id="5d610-120">PARAMETERS</span></span>

### <span data-ttu-id="5d610-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5d610-121">-AsJob</span></span>
<span data-ttu-id="5d610-122">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="5d610-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5d610-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d610-123">-DefaultProfile</span></span>
<span data-ttu-id="5d610-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5d610-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d610-125">-Force</span><span class="sxs-lookup"><span data-stu-id="5d610-125">-Force</span></span>
<span data-ttu-id="5d610-126">Não pedir confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="5d610-126">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="5d610-127">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="5d610-127">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="5d610-128">O tempo limite ocioso do gateway NAT.</span><span class="sxs-lookup"><span data-stu-id="5d610-128">The idle timeout of the nat gateway.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d610-129">-Local</span><span class="sxs-lookup"><span data-stu-id="5d610-129">-Location</span></span>
<span data-ttu-id="5d610-130">O local.</span><span class="sxs-lookup"><span data-stu-id="5d610-130">The location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d610-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="5d610-131">-Name</span></span>
<span data-ttu-id="5d610-132">O nome do gateway NAT.</span><span class="sxs-lookup"><span data-stu-id="5d610-132">The name of the nat gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d610-133">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="5d610-133">-PublicIpAddress</span></span>
<span data-ttu-id="5d610-134">Uma matriz de endereços IP públicos associados ao recurso de gateway NAT.</span><span class="sxs-lookup"><span data-stu-id="5d610-134">An array of public ip addresses associated with the nat gateway resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d610-135">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="5d610-135">-PublicIpPrefix</span></span>
<span data-ttu-id="5d610-136">Uma matriz de prefixos IP públicos associados ao recurso de gateway NAT.</span><span class="sxs-lookup"><span data-stu-id="5d610-136">An array of public ip prefixes associated with the nat gateway resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d610-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d610-137">-ResourceGroupName</span></span>
<span data-ttu-id="5d610-138">O nome do grupo de recursos do gateway NAT.</span><span class="sxs-lookup"><span data-stu-id="5d610-138">The resource group name of the nat gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d610-139">-SKU</span><span class="sxs-lookup"><span data-stu-id="5d610-139">-Sku</span></span>
<span data-ttu-id="5d610-140">Nome de uma SKU do gateway NAT.</span><span class="sxs-lookup"><span data-stu-id="5d610-140">Name of a NAT gateway SKU.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d610-141">-Marca</span><span class="sxs-lookup"><span data-stu-id="5d610-141">-Tag</span></span>
<span data-ttu-id="5d610-142">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="5d610-142">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d610-143">-Zone</span><span class="sxs-lookup"><span data-stu-id="5d610-143">-Zone</span></span>
<span data-ttu-id="5d610-144">Uma lista de zonas de disponibilidade que indicam a zona na qual o gateway NAT deve ser implantado.</span><span class="sxs-lookup"><span data-stu-id="5d610-144">A list of availability zones denoting the zone in which Nat Gateway should be deployed.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d610-145">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5d610-145">-Confirm</span></span>
<span data-ttu-id="5d610-146">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d610-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d610-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d610-147">-WhatIf</span></span>
<span data-ttu-id="5d610-148">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5d610-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d610-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5d610-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d610-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d610-150">CommonParameters</span></span>
<span data-ttu-id="5d610-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d610-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d610-152">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5d610-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d610-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5d610-153">INPUTS</span></span>

### <span data-ttu-id="5d610-154">System. String</span><span class="sxs-lookup"><span data-stu-id="5d610-154">System.String</span></span>

### <span data-ttu-id="5d610-155">System. Int32</span><span class="sxs-lookup"><span data-stu-id="5d610-155">System.Int32</span></span>

### <span data-ttu-id="5d610-156">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="5d610-156">System.Collections.Hashtable</span></span>

### <span data-ttu-id="5d610-157">Microsoft. Azure. Commands. Network. Models. PSResourceId []</span><span class="sxs-lookup"><span data-stu-id="5d610-157">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

## <span data-ttu-id="5d610-158">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5d610-158">OUTPUTS</span></span>

### <span data-ttu-id="5d610-159">Microsoft. Azure. Commands. Network. Models. PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="5d610-159">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="5d610-160">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5d610-160">NOTES</span></span>

## <span data-ttu-id="5d610-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5d610-161">RELATED LINKS</span></span>
