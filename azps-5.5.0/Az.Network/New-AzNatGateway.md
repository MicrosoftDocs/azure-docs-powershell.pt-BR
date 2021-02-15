---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznatgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNatGateway.md
ms.openlocfilehash: 0855ba4e7e16503045d13c370838cd5d3fffb033
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115127"
---
# <span data-ttu-id="a510e-101">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="a510e-101">New-AzNatGateway</span></span>

## <span data-ttu-id="a510e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a510e-102">SYNOPSIS</span></span>
<span data-ttu-id="a510e-103">Crie um novo recurso Nat Gateway com propriedades Endereço Ip Público/Prefixo Ip Público, IdleTimeoutInMinutes e SKU.</span><span class="sxs-lookup"><span data-stu-id="a510e-103">Create new Nat Gateway resource with properties Public Ip Address/Public Ip Prefix, IdleTimeoutInMinutes and Sku.</span></span>

## <span data-ttu-id="a510e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a510e-104">SYNTAX</span></span>

```
New-AzNatGateway -ResourceGroupName <String> -Name <String> [-IdleTimeoutInMinutes <Int32>] [-Zone <String[]>]
 [-Sku <String>] [-Location <String>] [-Tag <Hashtable>] [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a510e-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="a510e-105">DESCRIPTION</span></span>
<span data-ttu-id="a510e-106">O **cmdlet New-AzNatGateway** cria um Recurso de Gateway Nat.</span><span class="sxs-lookup"><span data-stu-id="a510e-106">The **New-AzNatGateway** cmdlet creates a Nat Gateway Resource.</span></span> <span data-ttu-id="a510e-107">Um natgateway requer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="a510e-107">A natgateway requires the following:</span></span> 
- <span data-ttu-id="a510e-108">Endereço Ip Público e/ou Prefixo Ip Público</span><span class="sxs-lookup"><span data-stu-id="a510e-108">Public Ip Address and/or Public Ip Prefix</span></span>
- <span data-ttu-id="a510e-109">IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="a510e-109">IdleTimeoutInMinutes</span></span> 
- <span data-ttu-id="a510e-110">Sku</span><span class="sxs-lookup"><span data-stu-id="a510e-110">Sku</span></span>
- <span data-ttu-id="a510e-111">ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a510e-111">ResourceGroupName</span></span>
- <span data-ttu-id="a510e-112">Resourcename</span><span class="sxs-lookup"><span data-stu-id="a510e-112">ResourceName</span></span>
- <span data-ttu-id="a510e-113">Localização</span><span class="sxs-lookup"><span data-stu-id="a510e-113">Location</span></span>

## <span data-ttu-id="a510e-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a510e-114">EXAMPLES</span></span>

### <span data-ttu-id="a510e-115">Exemplo 1: Criar Gateway Nat com Endereço Ip Público</span><span class="sxs-lookup"><span data-stu-id="a510e-115">Example 1: Create Nat Gateway with Public Ip Address</span></span>
```powershell
PS C:> $pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip
```

### <span data-ttu-id="a510e-116">Exemplo 2: Criar Gateway Nat com Prefixo Ip Público</span><span class="sxs-lookup"><span data-stu-id="a510e-116">Example 2: Create Nat Gateway with Public Ip Prefix</span></span>
```powershell
PS C:> $publicipprefix = New-AzPublicIpPrefix -Name "prefix2" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -PrefixLength "31"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpPrefix $publicipprefix
```

### <span data-ttu-id="a510e-117">Exemplo 3: Criar Gateway Nat com Endereço IP Público na Zona de Disponibilidade 1</span><span class="sxs-lookup"><span data-stu-id="a510e-117">Example 3: Create Nat Gateway with Public IP Address in Availability Zone 1</span></span>
```powershell
PS C:> $pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip -Zone "1"
```

<span data-ttu-id="a510e-118">O primeiro comando cria o Endereço IP público padrão.</span><span class="sxs-lookup"><span data-stu-id="a510e-118">The first command creates standard Public IP Address.</span></span>
<span data-ttu-id="a510e-119">O segundo comando cria o Gateway NAT com Endereço IP Público na Zona de Disponibilidade 1.</span><span class="sxs-lookup"><span data-stu-id="a510e-119">The second command creates NAT Gateway with Public IP Address in Availability Zone 1.</span></span>

## <span data-ttu-id="a510e-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a510e-120">PARAMETERS</span></span>

### <span data-ttu-id="a510e-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a510e-121">-AsJob</span></span>
<span data-ttu-id="a510e-122">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="a510e-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a510e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a510e-123">-DefaultProfile</span></span>
<span data-ttu-id="a510e-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a510e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a510e-125">-Forçar</span><span class="sxs-lookup"><span data-stu-id="a510e-125">-Force</span></span>
<span data-ttu-id="a510e-126">Não peça confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="a510e-126">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="a510e-127">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="a510e-127">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="a510e-128">O tempo ocioso do gateway nat.</span><span class="sxs-lookup"><span data-stu-id="a510e-128">The idle timeout of the nat gateway.</span></span>

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

### <span data-ttu-id="a510e-129">-Local</span><span class="sxs-lookup"><span data-stu-id="a510e-129">-Location</span></span>
<span data-ttu-id="a510e-130">O local.</span><span class="sxs-lookup"><span data-stu-id="a510e-130">The location.</span></span>

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

### <span data-ttu-id="a510e-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="a510e-131">-Name</span></span>
<span data-ttu-id="a510e-132">O nome do gateway nat.</span><span class="sxs-lookup"><span data-stu-id="a510e-132">The name of the nat gateway.</span></span>

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

### <span data-ttu-id="a510e-133">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a510e-133">-PublicIpAddress</span></span>
<span data-ttu-id="a510e-134">Uma matriz de endereços IP públicos associados ao recurso nat gateway.</span><span class="sxs-lookup"><span data-stu-id="a510e-134">An array of public ip addresses associated with the nat gateway resource.</span></span>

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

### <span data-ttu-id="a510e-135">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="a510e-135">-PublicIpPrefix</span></span>
<span data-ttu-id="a510e-136">Uma matriz de prefixos ip públicos associados ao recurso nat gateway.</span><span class="sxs-lookup"><span data-stu-id="a510e-136">An array of public ip prefixes associated with the nat gateway resource.</span></span>

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

### <span data-ttu-id="a510e-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a510e-137">-ResourceGroupName</span></span>
<span data-ttu-id="a510e-138">O nome do grupo de recursos do gateway nat.</span><span class="sxs-lookup"><span data-stu-id="a510e-138">The resource group name of the nat gateway.</span></span>

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

### <span data-ttu-id="a510e-139">-SKU</span><span class="sxs-lookup"><span data-stu-id="a510e-139">-Sku</span></span>
<span data-ttu-id="a510e-140">Nome de uma SKU do gateway NAT.</span><span class="sxs-lookup"><span data-stu-id="a510e-140">Name of a NAT gateway SKU.</span></span>

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

### <span data-ttu-id="a510e-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="a510e-141">-Tag</span></span>
<span data-ttu-id="a510e-142">Uma tabela hash que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="a510e-142">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="a510e-143">-Zona</span><span class="sxs-lookup"><span data-stu-id="a510e-143">-Zone</span></span>
<span data-ttu-id="a510e-144">Uma lista de zonas de disponibilidade que denotam a zona na qual Nat Gateway deve ser implantado.</span><span class="sxs-lookup"><span data-stu-id="a510e-144">A list of availability zones denoting the zone in which Nat Gateway should be deployed.</span></span>

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

### <span data-ttu-id="a510e-145">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="a510e-145">-Confirm</span></span>
<span data-ttu-id="a510e-146">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a510e-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a510e-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a510e-147">-WhatIf</span></span>
<span data-ttu-id="a510e-148">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="a510e-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a510e-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a510e-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a510e-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a510e-150">CommonParameters</span></span>
<span data-ttu-id="a510e-151">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a510e-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a510e-152">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a510e-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a510e-153">Entradas</span><span class="sxs-lookup"><span data-stu-id="a510e-153">INPUTS</span></span>

### <span data-ttu-id="a510e-154">System.String</span><span class="sxs-lookup"><span data-stu-id="a510e-154">System.String</span></span>

### <span data-ttu-id="a510e-155">System.Int32</span><span class="sxs-lookup"><span data-stu-id="a510e-155">System.Int32</span></span>

### <span data-ttu-id="a510e-156">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="a510e-156">System.Collections.Hashtable</span></span>

### <span data-ttu-id="a510e-157">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span><span class="sxs-lookup"><span data-stu-id="a510e-157">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

## <span data-ttu-id="a510e-158">Saídas</span><span class="sxs-lookup"><span data-stu-id="a510e-158">OUTPUTS</span></span>

### <span data-ttu-id="a510e-159">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="a510e-159">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="a510e-160">Notas</span><span class="sxs-lookup"><span data-stu-id="a510e-160">NOTES</span></span>

## <span data-ttu-id="a510e-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a510e-161">RELATED LINKS</span></span>
