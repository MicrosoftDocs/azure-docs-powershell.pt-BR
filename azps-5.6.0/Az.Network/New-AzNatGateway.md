---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznatgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNatGateway.md
ms.openlocfilehash: 168a1803781748eb81c3a2087876b2a7b18d9d39
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885407"
---
# <span data-ttu-id="33918-101">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="33918-101">New-AzNatGateway</span></span>

## <span data-ttu-id="33918-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33918-102">SYNOPSIS</span></span>
<span data-ttu-id="33918-103">Crie novo recurso Nat Gateway com propriedades Endereço Ip Público/Prefixo ip público, IdleTimeoutInMinutes e Sku.</span><span class="sxs-lookup"><span data-stu-id="33918-103">Create new Nat Gateway resource with properties Public Ip Address/Public Ip Prefix, IdleTimeoutInMinutes and Sku.</span></span>

## <span data-ttu-id="33918-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="33918-104">SYNTAX</span></span>

```
New-AzNatGateway -ResourceGroupName <String> -Name <String> [-IdleTimeoutInMinutes <Int32>] [-Zone <String[]>]
 [-Sku <String>] [-Location <String>] [-Tag <Hashtable>] [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33918-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="33918-105">DESCRIPTION</span></span>
<span data-ttu-id="33918-106">O cmdlet **New-AzNatGateway** cria um Recurso nat gateway.</span><span class="sxs-lookup"><span data-stu-id="33918-106">The **New-AzNatGateway** cmdlet creates a Nat Gateway Resource.</span></span> <span data-ttu-id="33918-107">Um natgateway exige o seguinte:</span><span class="sxs-lookup"><span data-stu-id="33918-107">A natgateway requires the following:</span></span> 
- <span data-ttu-id="33918-108">Endereço Ip Público e/ou Prefixo Ip Público</span><span class="sxs-lookup"><span data-stu-id="33918-108">Public Ip Address and/or Public Ip Prefix</span></span>
- <span data-ttu-id="33918-109">IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="33918-109">IdleTimeoutInMinutes</span></span> 
- <span data-ttu-id="33918-110">Sku</span><span class="sxs-lookup"><span data-stu-id="33918-110">Sku</span></span>
- <span data-ttu-id="33918-111">ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33918-111">ResourceGroupName</span></span>
- <span data-ttu-id="33918-112">ResourceName</span><span class="sxs-lookup"><span data-stu-id="33918-112">ResourceName</span></span>
- <span data-ttu-id="33918-113">Local</span><span class="sxs-lookup"><span data-stu-id="33918-113">Location</span></span>

## <span data-ttu-id="33918-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="33918-114">EXAMPLES</span></span>

### <span data-ttu-id="33918-115">Exemplo 1: Criar Gateway Nat com Endereço Ip Público</span><span class="sxs-lookup"><span data-stu-id="33918-115">Example 1: Create Nat Gateway with Public Ip Address</span></span>
```powershell
PS C:> $pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip
```

### <span data-ttu-id="33918-116">Exemplo 2: Criar Gateway Nat com prefixo ip público</span><span class="sxs-lookup"><span data-stu-id="33918-116">Example 2: Create Nat Gateway with Public Ip Prefix</span></span>
```powershell
PS C:> $publicipprefix = New-AzPublicIpPrefix -Name "prefix2" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -PrefixLength "31"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpPrefix $publicipprefix
```

### <span data-ttu-id="33918-117">Exemplo 3: Criar Gateway Nat com endereço IP público na Zona de Disponibilidade 1</span><span class="sxs-lookup"><span data-stu-id="33918-117">Example 3: Create Nat Gateway with Public IP Address in Availability Zone 1</span></span>
```powershell
PS C:> $pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip -Zone "1"
```

<span data-ttu-id="33918-118">O primeiro comando cria endereço IP público padrão.</span><span class="sxs-lookup"><span data-stu-id="33918-118">The first command creates standard Public IP Address.</span></span>
<span data-ttu-id="33918-119">O segundo comando cria o Gateway NAT com Endereço IP Público na Zona de Disponibilidade 1.</span><span class="sxs-lookup"><span data-stu-id="33918-119">The second command creates NAT Gateway with Public IP Address in Availability Zone 1.</span></span>

## <span data-ttu-id="33918-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="33918-120">PARAMETERS</span></span>

### <span data-ttu-id="33918-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="33918-121">-AsJob</span></span>
<span data-ttu-id="33918-122">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="33918-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="33918-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33918-123">-DefaultProfile</span></span>
<span data-ttu-id="33918-124">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="33918-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33918-125">-Force</span><span class="sxs-lookup"><span data-stu-id="33918-125">-Force</span></span>
<span data-ttu-id="33918-126">Não peça confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="33918-126">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="33918-127">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="33918-127">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="33918-128">O tempo de ocioso do gateway nat.</span><span class="sxs-lookup"><span data-stu-id="33918-128">The idle timeout of the nat gateway.</span></span>

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

### <span data-ttu-id="33918-129">-Location</span><span class="sxs-lookup"><span data-stu-id="33918-129">-Location</span></span>
<span data-ttu-id="33918-130">O local.</span><span class="sxs-lookup"><span data-stu-id="33918-130">The location.</span></span>

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

### <span data-ttu-id="33918-131">-Name</span><span class="sxs-lookup"><span data-stu-id="33918-131">-Name</span></span>
<span data-ttu-id="33918-132">O nome do gateway nat.</span><span class="sxs-lookup"><span data-stu-id="33918-132">The name of the nat gateway.</span></span>

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

### <span data-ttu-id="33918-133">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="33918-133">-PublicIpAddress</span></span>
<span data-ttu-id="33918-134">Uma matriz de endereços IP públicos associados ao recurso de gateway nat.</span><span class="sxs-lookup"><span data-stu-id="33918-134">An array of public ip addresses associated with the nat gateway resource.</span></span>

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

### <span data-ttu-id="33918-135">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="33918-135">-PublicIpPrefix</span></span>
<span data-ttu-id="33918-136">Uma matriz de prefixos ip públicos associados ao recurso de gateway nat.</span><span class="sxs-lookup"><span data-stu-id="33918-136">An array of public ip prefixes associated with the nat gateway resource.</span></span>

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

### <span data-ttu-id="33918-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33918-137">-ResourceGroupName</span></span>
<span data-ttu-id="33918-138">O nome do grupo de recursos do gateway nat.</span><span class="sxs-lookup"><span data-stu-id="33918-138">The resource group name of the nat gateway.</span></span>

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

### <span data-ttu-id="33918-139">-Sku</span><span class="sxs-lookup"><span data-stu-id="33918-139">-Sku</span></span>
<span data-ttu-id="33918-140">Nome de um SKU do gateway NAT.</span><span class="sxs-lookup"><span data-stu-id="33918-140">Name of a NAT gateway SKU.</span></span>

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

### <span data-ttu-id="33918-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="33918-141">-Tag</span></span>
<span data-ttu-id="33918-142">Uma hashtable que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="33918-142">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="33918-143">-Zone</span><span class="sxs-lookup"><span data-stu-id="33918-143">-Zone</span></span>
<span data-ttu-id="33918-144">Uma lista de zonas de disponibilidade que denotam a zona na qual Nat Gateway deve ser implantado.</span><span class="sxs-lookup"><span data-stu-id="33918-144">A list of availability zones denoting the zone in which Nat Gateway should be deployed.</span></span>

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

### <span data-ttu-id="33918-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="33918-145">-Confirm</span></span>
<span data-ttu-id="33918-146">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33918-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33918-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33918-147">-WhatIf</span></span>
<span data-ttu-id="33918-148">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="33918-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33918-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="33918-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33918-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33918-150">CommonParameters</span></span>
<span data-ttu-id="33918-151">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33918-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33918-152">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="33918-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33918-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="33918-153">INPUTS</span></span>

### <span data-ttu-id="33918-154">System.String</span><span class="sxs-lookup"><span data-stu-id="33918-154">System.String</span></span>

### <span data-ttu-id="33918-155">System.Int32</span><span class="sxs-lookup"><span data-stu-id="33918-155">System.Int32</span></span>

### <span data-ttu-id="33918-156">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="33918-156">System.Collections.Hashtable</span></span>

### <span data-ttu-id="33918-157">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span><span class="sxs-lookup"><span data-stu-id="33918-157">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

## <span data-ttu-id="33918-158">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="33918-158">OUTPUTS</span></span>

### <span data-ttu-id="33918-159">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="33918-159">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="33918-160">NOTES</span><span class="sxs-lookup"><span data-stu-id="33918-160">NOTES</span></span>

## <span data-ttu-id="33918-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="33918-161">RELATED LINKS</span></span>
