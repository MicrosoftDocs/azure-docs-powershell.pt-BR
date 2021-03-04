---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHostGroup.md
ms.openlocfilehash: 69ab5a7ae89184a5d77344d45801da307e7840bd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886345"
---
# <span data-ttu-id="07339-101">New-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="07339-101">New-AzHostGroup</span></span>

## <span data-ttu-id="07339-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07339-102">SYNOPSIS</span></span>
<span data-ttu-id="07339-103">Cria um grupo de host.</span><span class="sxs-lookup"><span data-stu-id="07339-103">Creates a host group.</span></span>

## <span data-ttu-id="07339-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="07339-104">SYNTAX</span></span>

```
New-AzHostGroup [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 -PlatformFaultDomain <Int32> [-Zone <String[]>] [-SupportAutomaticPlacement <bool>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07339-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="07339-105">DESCRIPTION</span></span>
<span data-ttu-id="07339-106">Este cmdlet criará um grupo host.</span><span class="sxs-lookup"><span data-stu-id="07339-106">This cmdlet will create a Host group.</span></span>

## <span data-ttu-id="07339-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="07339-107">EXAMPLES</span></span>

### <span data-ttu-id="07339-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="07339-108">Example 1</span></span>
```
PS C:\> New-AzHostGroup -ResourceGroupName $resourceGroupName -Name $hostGroupName -Location $location -Zone $zone

ResourceGroupName        : myrg01
PlatformFaultDomainCount : 2
Hosts                    : {/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01/hosts/myhost01}
Zones                    : {1}
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01
Name                     : myhostgroup01
Location                 : eastus
Tags                     : {[key1, val1]}
```

<span data-ttu-id="07339-109">Este comando cria um grupo de host no local e zona determinados.</span><span class="sxs-lookup"><span data-stu-id="07339-109">This command creates a host group in the given location and zone.</span></span>

## <span data-ttu-id="07339-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="07339-110">PARAMETERS</span></span>

### <span data-ttu-id="07339-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="07339-111">-AsJob</span></span>
<span data-ttu-id="07339-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="07339-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="07339-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07339-113">-DefaultProfile</span></span>
<span data-ttu-id="07339-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="07339-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07339-115">-Location</span><span class="sxs-lookup"><span data-stu-id="07339-115">-Location</span></span>
<span data-ttu-id="07339-116">Especifica o local.</span><span class="sxs-lookup"><span data-stu-id="07339-116">Specifies location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07339-117">-Name</span><span class="sxs-lookup"><span data-stu-id="07339-117">-Name</span></span>
<span data-ttu-id="07339-118">Especifica o nome do grupo host.</span><span class="sxs-lookup"><span data-stu-id="07339-118">Specifies the name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HostGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07339-119">-PlatformFaultDomain</span><span class="sxs-lookup"><span data-stu-id="07339-119">-PlatformFaultDomain</span></span>
<span data-ttu-id="07339-120">Especifica o número de domínios de falha que o grupo host pode abranger.</span><span class="sxs-lookup"><span data-stu-id="07339-120">Specifies the number of fault domains that the host group can span.</span></span>  <span data-ttu-id="07339-121">O valor mínimo é 1 e o valor máximo é 3.</span><span class="sxs-lookup"><span data-stu-id="07339-121">The minimum value is 1 and the maximum value is 3.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07339-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07339-122">-ResourceGroupName</span></span>
<span data-ttu-id="07339-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="07339-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07339-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="07339-124">-Tag</span></span>
<span data-ttu-id="07339-125">Especifica marcas</span><span class="sxs-lookup"><span data-stu-id="07339-125">Specifies Tags</span></span>

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

### <span data-ttu-id="07339-126">-Zone</span><span class="sxs-lookup"><span data-stu-id="07339-126">-Zone</span></span>
<span data-ttu-id="07339-127">Especifica zonas do grupo host.</span><span class="sxs-lookup"><span data-stu-id="07339-127">Specifies Zones of the host group.</span></span>

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

### <span data-ttu-id="07339-128">-SupportAutomaticPlacement</span><span class="sxs-lookup"><span data-stu-id="07339-128">-SupportAutomaticPlacement</span></span>
<span data-ttu-id="07339-129">Especifica se HostGroup habilitará o posicionamento automático de vms.</span><span class="sxs-lookup"><span data-stu-id="07339-129">Specifies if HostGroup will enable automatic placement of vm's.</span></span>
<span data-ttu-id="07339-130">A colocação automática significa que essas VMs são colocadas em hosts dedicados, escolhidos pelo Azure, no grupo de host dedicado.</span><span class="sxs-lookup"><span data-stu-id="07339-130">Automatic placement means these VMs are placed on dedicated hosts, chosen by Azure, under the dedicated host group.</span></span>
<span data-ttu-id="07339-131">Se não for especificado, o valor padrão será false.</span><span class="sxs-lookup"><span data-stu-id="07339-131">If not specified, default value will be false.</span></span>

```yaml
Type: bool
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: True
Accept pipeline input: False
Accept wildcard characters: False
```


### <span data-ttu-id="07339-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="07339-132">-Confirm</span></span>
<span data-ttu-id="07339-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07339-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07339-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07339-134">-WhatIf</span></span>
<span data-ttu-id="07339-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="07339-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07339-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="07339-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07339-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07339-137">CommonParameters</span></span>
<span data-ttu-id="07339-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07339-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07339-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="07339-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07339-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="07339-140">INPUTS</span></span>

### <span data-ttu-id="07339-141">System.String</span><span class="sxs-lookup"><span data-stu-id="07339-141">System.String</span></span>

## <span data-ttu-id="07339-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="07339-142">OUTPUTS</span></span>

### <span data-ttu-id="07339-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="07339-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="07339-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="07339-144">NOTES</span></span>

## <span data-ttu-id="07339-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="07339-145">RELATED LINKS</span></span>
