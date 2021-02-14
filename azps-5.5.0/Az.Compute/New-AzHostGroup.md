---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHostGroup.md
ms.openlocfilehash: 53f83fcc304b92c7e890126e4c8dff1a5cc539d8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115471"
---
# <span data-ttu-id="71956-101">New-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="71956-101">New-AzHostGroup</span></span>

## <span data-ttu-id="71956-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="71956-102">SYNOPSIS</span></span>
<span data-ttu-id="71956-103">Cria um grupo de host.</span><span class="sxs-lookup"><span data-stu-id="71956-103">Creates a host group.</span></span>

## <span data-ttu-id="71956-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="71956-104">SYNTAX</span></span>

```
New-AzHostGroup [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 -PlatformFaultDomain <Int32> [-Zone <String[]>] [-SupportAutomaticPlacement <bool>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71956-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="71956-105">DESCRIPTION</span></span>
<span data-ttu-id="71956-106">Este cmdlet criará um grupo host.</span><span class="sxs-lookup"><span data-stu-id="71956-106">This cmdlet will create a Host group.</span></span>

## <span data-ttu-id="71956-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="71956-107">EXAMPLES</span></span>

### <span data-ttu-id="71956-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="71956-108">Example 1</span></span>
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

<span data-ttu-id="71956-109">Esse comando cria um grupo de host em determinado local e zona.</span><span class="sxs-lookup"><span data-stu-id="71956-109">This command creates a host group in the given location and zone.</span></span>

## <span data-ttu-id="71956-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="71956-110">PARAMETERS</span></span>

### <span data-ttu-id="71956-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="71956-111">-AsJob</span></span>
<span data-ttu-id="71956-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="71956-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="71956-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71956-113">-DefaultProfile</span></span>
<span data-ttu-id="71956-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="71956-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71956-115">-Local</span><span class="sxs-lookup"><span data-stu-id="71956-115">-Location</span></span>
<span data-ttu-id="71956-116">Especifica o local.</span><span class="sxs-lookup"><span data-stu-id="71956-116">Specifies location.</span></span>

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

### <span data-ttu-id="71956-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="71956-117">-Name</span></span>
<span data-ttu-id="71956-118">Especifica o nome do grupo de host.</span><span class="sxs-lookup"><span data-stu-id="71956-118">Specifies the name of the host group.</span></span>

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

### <span data-ttu-id="71956-119">-PlatformFaultDomain</span><span class="sxs-lookup"><span data-stu-id="71956-119">-PlatformFaultDomain</span></span>
<span data-ttu-id="71956-120">Especifica o número de domínios de falha que o grupo de host pode abranger.</span><span class="sxs-lookup"><span data-stu-id="71956-120">Specifies the number of fault domains that the host group can span.</span></span>  <span data-ttu-id="71956-121">O valor mínimo é 1 e o valor máximo é 3.</span><span class="sxs-lookup"><span data-stu-id="71956-121">The minimum value is 1 and the maximum value is 3.</span></span>

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

### <span data-ttu-id="71956-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71956-122">-ResourceGroupName</span></span>
<span data-ttu-id="71956-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="71956-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="71956-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="71956-124">-Tag</span></span>
<span data-ttu-id="71956-125">Especifica marcas</span><span class="sxs-lookup"><span data-stu-id="71956-125">Specifies Tags</span></span>

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

### <span data-ttu-id="71956-126">-Zona</span><span class="sxs-lookup"><span data-stu-id="71956-126">-Zone</span></span>
<span data-ttu-id="71956-127">Especifica zonas do grupo host.</span><span class="sxs-lookup"><span data-stu-id="71956-127">Specifies Zones of the host group.</span></span>

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

### <span data-ttu-id="71956-128">-SupportAutomaticPlacement</span><span class="sxs-lookup"><span data-stu-id="71956-128">-SupportAutomaticPlacement</span></span>
<span data-ttu-id="71956-129">Especifica se o HostGroup habilitará o posicionamento automático de vms.</span><span class="sxs-lookup"><span data-stu-id="71956-129">Specifies if HostGroup will enable automatic placement of vm's.</span></span>
<span data-ttu-id="71956-130">O posicionamento automático significa que esses VMs são colocados em hosts dedicados, escolhidos pelo Azure, no grupo de host dedicado.</span><span class="sxs-lookup"><span data-stu-id="71956-130">Automatic placement means these VMs are placed on dedicated hosts, chosen by Azure, under the dedicated host group.</span></span>
<span data-ttu-id="71956-131">Se não especificado, o valor padrão será falso.</span><span class="sxs-lookup"><span data-stu-id="71956-131">If not specified, default value will be false.</span></span>

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


### <span data-ttu-id="71956-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="71956-132">-Confirm</span></span>
<span data-ttu-id="71956-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71956-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71956-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71956-134">-WhatIf</span></span>
<span data-ttu-id="71956-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="71956-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71956-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="71956-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71956-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71956-137">CommonParameters</span></span>
<span data-ttu-id="71956-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71956-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71956-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="71956-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71956-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="71956-140">INPUTS</span></span>

### <span data-ttu-id="71956-141">System.String</span><span class="sxs-lookup"><span data-stu-id="71956-141">System.String</span></span>

## <span data-ttu-id="71956-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="71956-142">OUTPUTS</span></span>

### <span data-ttu-id="71956-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="71956-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="71956-144">Notas</span><span class="sxs-lookup"><span data-stu-id="71956-144">NOTES</span></span>

## <span data-ttu-id="71956-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="71956-145">RELATED LINKS</span></span>
