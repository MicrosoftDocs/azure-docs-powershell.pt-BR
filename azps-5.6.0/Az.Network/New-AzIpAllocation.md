---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpAllocation.md
ms.openlocfilehash: 0c7325d43ca1e1aefa2ee4751cc90369e06beca6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887971"
---
# <span data-ttu-id="bac07-101">New-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="bac07-101">New-AzIpAllocation</span></span>

## <span data-ttu-id="bac07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bac07-102">SYNOPSIS</span></span>
<span data-ttu-id="bac07-103">Cria um IpAllocation do Azure.</span><span class="sxs-lookup"><span data-stu-id="bac07-103">Creates an Azure IpAllocation.</span></span>

## <span data-ttu-id="bac07-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="bac07-104">SYNTAX</span></span>

```
New-AzIpAllocation -Name <String> -ResourceGroupName <String> -Location <String>
 -IpAllocationType <String> [-Prefix <String>] [-PrefixLength <Int32>] [-PrefixType <String>]
 [-IpamAllocationId <String>] [-IpAllocationTag <Hashtable>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bac07-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="bac07-105">DESCRIPTION</span></span>
<span data-ttu-id="bac07-106">O cmdlet **New-AzIpAllocation** cria um IpAllocation do Azure</span><span class="sxs-lookup"><span data-stu-id="bac07-106">The **New-AzIpAllocation** cmdlet creates an Azure IpAllocation</span></span>

## <span data-ttu-id="bac07-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bac07-107">EXAMPLES</span></span>

### <span data-ttu-id="bac07-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bac07-108">Example 1</span></span>
```powershell
New-AzIpAllocation -ResourceName 'TestIpAllocation'  -ResourceGroupName 'TestResourcegroupName' -Location 'eastus' -IpAllocationType 'Hypernet' -Prefix '1.2.3.4/32' -IpAllocationTag @{"VnetId"="vnet1"}
```

### <span data-ttu-id="bac07-109">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="bac07-109">Example 2</span></span>
```powershell
New-AzIpAllocation -ResourceName 'TestIpAllocation'  -ResourceGroupName 'TestResourcegroupName' -Location 'eastus' -IpAllocationType 'Hypernet' -PrefixLength 32 -PrefixType 'ipv4' -IpAllocationTag @{"VnetId"="vnet1"}
```

## <span data-ttu-id="bac07-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="bac07-110">PARAMETERS</span></span>

### <span data-ttu-id="bac07-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bac07-111">-AsJob</span></span>
<span data-ttu-id="bac07-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="bac07-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bac07-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bac07-113">-DefaultProfile</span></span>
<span data-ttu-id="bac07-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bac07-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bac07-115">-Force</span><span class="sxs-lookup"><span data-stu-id="bac07-115">-Force</span></span>
<span data-ttu-id="bac07-116">Não peça confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="bac07-116">Do not ask for confirmation if you want to override a resource</span></span>

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

### <span data-ttu-id="bac07-117">-IpAllocationTag</span><span class="sxs-lookup"><span data-stu-id="bac07-117">-IpAllocationTag</span></span>
<span data-ttu-id="bac07-118">As marcas de alocação da alocação de IP</span><span class="sxs-lookup"><span data-stu-id="bac07-118">The allocation tags of the IP allocation</span></span>

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

### <span data-ttu-id="bac07-119">-IpAllocationType</span><span class="sxs-lookup"><span data-stu-id="bac07-119">-IpAllocationType</span></span>
<span data-ttu-id="bac07-120">O tipo de alocação de IP</span><span class="sxs-lookup"><span data-stu-id="bac07-120">The type of the IP allocation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Hypernet, Undefined

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bac07-121">-IpamAllocationId</span><span class="sxs-lookup"><span data-stu-id="bac07-121">-IpamAllocationId</span></span>
<span data-ttu-id="bac07-122">A ID de alocação de ipam da alocação de IP</span><span class="sxs-lookup"><span data-stu-id="bac07-122">The ipam allocation ID of the IP allocation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bac07-123">-Location</span><span class="sxs-lookup"><span data-stu-id="bac07-123">-Location</span></span>
<span data-ttu-id="bac07-124">location.</span><span class="sxs-lookup"><span data-stu-id="bac07-124">location.</span></span>

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

### <span data-ttu-id="bac07-125">-Name</span><span class="sxs-lookup"><span data-stu-id="bac07-125">-Name</span></span>
<span data-ttu-id="bac07-126">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="bac07-126">The resource name.</span></span>

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

### <span data-ttu-id="bac07-127">-Prefix</span><span class="sxs-lookup"><span data-stu-id="bac07-127">-Prefix</span></span>
<span data-ttu-id="bac07-128">O prefixo da alocação de IP</span><span class="sxs-lookup"><span data-stu-id="bac07-128">The prefix of the IP allocation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bac07-129">-PrefixLength</span><span class="sxs-lookup"><span data-stu-id="bac07-129">-PrefixLength</span></span>
<span data-ttu-id="bac07-130">O comprimento do prefixo da alocação de IP</span><span class="sxs-lookup"><span data-stu-id="bac07-130">The prefix length of the IP allocation</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bac07-131">-PrefixType</span><span class="sxs-lookup"><span data-stu-id="bac07-131">-PrefixType</span></span>
<span data-ttu-id="bac07-132">O tipo de prefixo da alocação de IP</span><span class="sxs-lookup"><span data-stu-id="bac07-132">The prefix type of the IP allocation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPV4, IPV6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bac07-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bac07-133">-ResourceGroupName</span></span>
<span data-ttu-id="bac07-134">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bac07-134">The resource group name.</span></span>

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

### <span data-ttu-id="bac07-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="bac07-135">-Tag</span></span>
<span data-ttu-id="bac07-136">Uma hashtable que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="bac07-136">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="bac07-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bac07-137">-Confirm</span></span>
<span data-ttu-id="bac07-138">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bac07-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bac07-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bac07-139">-WhatIf</span></span>
<span data-ttu-id="bac07-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bac07-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bac07-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bac07-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bac07-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bac07-142">CommonParameters</span></span>
<span data-ttu-id="bac07-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bac07-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bac07-144">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bac07-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bac07-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bac07-145">INPUTS</span></span>

### <span data-ttu-id="bac07-146">System.String</span><span class="sxs-lookup"><span data-stu-id="bac07-146">System.String</span></span>

### <span data-ttu-id="bac07-147">System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="bac07-147">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="bac07-148">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="bac07-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="bac07-149">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="bac07-149">OUTPUTS</span></span>

### <span data-ttu-id="bac07-150">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="bac07-150">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="bac07-151">NOTES</span><span class="sxs-lookup"><span data-stu-id="bac07-151">NOTES</span></span>

## <span data-ttu-id="bac07-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bac07-152">RELATED LINKS</span></span>
