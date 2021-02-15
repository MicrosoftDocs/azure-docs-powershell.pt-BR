---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpAllocation.md
ms.openlocfilehash: 9a6c84c0ff5d22a4f6c6038266598c6adfe19b29
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112830"
---
# <span data-ttu-id="7e1b0-101">New-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="7e1b0-101">New-AzIpAllocation</span></span>

## <span data-ttu-id="7e1b0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7e1b0-102">SYNOPSIS</span></span>
<span data-ttu-id="7e1b0-103">Cria uma Localização IpAllocation do Azure.</span><span class="sxs-lookup"><span data-stu-id="7e1b0-103">Creates an Azure IpAllocation.</span></span>

## <span data-ttu-id="7e1b0-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7e1b0-104">SYNTAX</span></span>

```
New-AzIpAllocation -Name <String> -ResourceGroupName <String> -Location <String>
 -IpAllocationType <String> [-Prefix <String>] [-PrefixLength <Int32>] [-PrefixType <String>]
 [-IpamAllocationId <String>] [-IpAllocationTag <Hashtable>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e1b0-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="7e1b0-105">DESCRIPTION</span></span>
<span data-ttu-id="7e1b0-106">O **cmdlet New-AzIpAllocation** cria uma Azure IpAllocation</span><span class="sxs-lookup"><span data-stu-id="7e1b0-106">The **New-AzIpAllocation** cmdlet creates an Azure IpAllocation</span></span>

## <span data-ttu-id="7e1b0-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7e1b0-107">EXAMPLES</span></span>

### <span data-ttu-id="7e1b0-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7e1b0-108">Example 1</span></span>
```powershell
New-AzIpAllocation -ResourceName 'TestIpAllocation'  -ResourceGroupName 'TestResourcegroupName' -Location 'eastus' -IpAllocationType 'Hypernet' -Prefix '1.2.3.4/32' -IpAllocationTag @{"VnetId"="vnet1"}
```

### <span data-ttu-id="7e1b0-109">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="7e1b0-109">Example 2</span></span>
```powershell
New-AzIpAllocation -ResourceName 'TestIpAllocation'  -ResourceGroupName 'TestResourcegroupName' -Location 'eastus' -IpAllocationType 'Hypernet' -PrefixLength 32 -PrefixType 'ipv4' -IpAllocationTag @{"VnetId"="vnet1"}
```

## <span data-ttu-id="7e1b0-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7e1b0-110">PARAMETERS</span></span>

### <span data-ttu-id="7e1b0-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7e1b0-111">-AsJob</span></span>
<span data-ttu-id="7e1b0-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="7e1b0-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7e1b0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e1b0-113">-DefaultProfile</span></span>
<span data-ttu-id="7e1b0-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7e1b0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e1b0-115">-Forçar</span><span class="sxs-lookup"><span data-stu-id="7e1b0-115">-Force</span></span>
<span data-ttu-id="7e1b0-116">Não peça confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="7e1b0-116">Do not ask for confirmation if you want to override a resource</span></span>

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

### <span data-ttu-id="7e1b0-117">-IpAllocationTag</span><span class="sxs-lookup"><span data-stu-id="7e1b0-117">-IpAllocationTag</span></span>
<span data-ttu-id="7e1b0-118">As marcas de alocação da alocação de IP</span><span class="sxs-lookup"><span data-stu-id="7e1b0-118">The allocation tags of the IP allocation</span></span>

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

### <span data-ttu-id="7e1b0-119">-IpAllocationType</span><span class="sxs-lookup"><span data-stu-id="7e1b0-119">-IpAllocationType</span></span>
<span data-ttu-id="7e1b0-120">O tipo da alocação de IP</span><span class="sxs-lookup"><span data-stu-id="7e1b0-120">The type of the IP allocation</span></span>

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

### <span data-ttu-id="7e1b0-121">-IpamAllocationId</span><span class="sxs-lookup"><span data-stu-id="7e1b0-121">-IpamAllocationId</span></span>
<span data-ttu-id="7e1b0-122">A ID de alocação ipam da alocação de IP</span><span class="sxs-lookup"><span data-stu-id="7e1b0-122">The ipam allocation ID of the IP allocation</span></span>

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

### <span data-ttu-id="7e1b0-123">-Local</span><span class="sxs-lookup"><span data-stu-id="7e1b0-123">-Location</span></span>
<span data-ttu-id="7e1b0-124">Localização.</span><span class="sxs-lookup"><span data-stu-id="7e1b0-124">location.</span></span>

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

### <span data-ttu-id="7e1b0-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="7e1b0-125">-Name</span></span>
<span data-ttu-id="7e1b0-126">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="7e1b0-126">The resource name.</span></span>

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

### <span data-ttu-id="7e1b0-127">-Prefixo</span><span class="sxs-lookup"><span data-stu-id="7e1b0-127">-Prefix</span></span>
<span data-ttu-id="7e1b0-128">O prefixo da alocação de IP</span><span class="sxs-lookup"><span data-stu-id="7e1b0-128">The prefix of the IP allocation</span></span>

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

### <span data-ttu-id="7e1b0-129">-PrefixLength</span><span class="sxs-lookup"><span data-stu-id="7e1b0-129">-PrefixLength</span></span>
<span data-ttu-id="7e1b0-130">O comprimento do prefixo da alocação de IP</span><span class="sxs-lookup"><span data-stu-id="7e1b0-130">The prefix length of the IP allocation</span></span>

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

### <span data-ttu-id="7e1b0-131">-PrefixType</span><span class="sxs-lookup"><span data-stu-id="7e1b0-131">-PrefixType</span></span>
<span data-ttu-id="7e1b0-132">O tipo de prefixo da alocação de IP</span><span class="sxs-lookup"><span data-stu-id="7e1b0-132">The prefix type of the IP allocation</span></span>

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

### <span data-ttu-id="7e1b0-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e1b0-133">-ResourceGroupName</span></span>
<span data-ttu-id="7e1b0-134">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7e1b0-134">The resource group name.</span></span>

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

### <span data-ttu-id="7e1b0-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="7e1b0-135">-Tag</span></span>
<span data-ttu-id="7e1b0-136">Uma tabela hash que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="7e1b0-136">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="7e1b0-137">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="7e1b0-137">-Confirm</span></span>
<span data-ttu-id="7e1b0-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e1b0-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e1b0-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e1b0-139">-WhatIf</span></span>
<span data-ttu-id="7e1b0-140">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="7e1b0-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e1b0-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7e1b0-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e1b0-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e1b0-142">CommonParameters</span></span>
<span data-ttu-id="7e1b0-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e1b0-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e1b0-144">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7e1b0-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e1b0-145">Entradas</span><span class="sxs-lookup"><span data-stu-id="7e1b0-145">INPUTS</span></span>

### <span data-ttu-id="7e1b0-146">System.String</span><span class="sxs-lookup"><span data-stu-id="7e1b0-146">System.String</span></span>

### <span data-ttu-id="7e1b0-147">System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="7e1b0-147">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="7e1b0-148">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="7e1b0-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7e1b0-149">Saídas</span><span class="sxs-lookup"><span data-stu-id="7e1b0-149">OUTPUTS</span></span>

### <span data-ttu-id="7e1b0-150">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="7e1b0-150">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="7e1b0-151">Notas</span><span class="sxs-lookup"><span data-stu-id="7e1b0-151">NOTES</span></span>

## <span data-ttu-id="7e1b0-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7e1b0-152">RELATED LINKS</span></span>
