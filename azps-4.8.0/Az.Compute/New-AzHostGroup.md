---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHostGroup.md
ms.openlocfilehash: 2fdb5317504bb1bc08ed45e8224a30a61cca8e8c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955063"
---
# <span data-ttu-id="6d677-101">New-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="6d677-101">New-AzHostGroup</span></span>

## <span data-ttu-id="6d677-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6d677-102">SYNOPSIS</span></span>
<span data-ttu-id="6d677-103">Cria um grupo de hosts.</span><span class="sxs-lookup"><span data-stu-id="6d677-103">Creates a host group.</span></span>

## <span data-ttu-id="6d677-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6d677-104">SYNTAX</span></span>

```
New-AzHostGroup [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 -PlatformFaultDomain <Int32> [-Zone <String[]>] [-SupportAutomaticPlacement <bool>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d677-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6d677-105">DESCRIPTION</span></span>
<span data-ttu-id="6d677-106">Esse cmdlet criará um grupo de hosts.</span><span class="sxs-lookup"><span data-stu-id="6d677-106">This cmdlet will create a Host group.</span></span>

## <span data-ttu-id="6d677-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6d677-107">EXAMPLES</span></span>

### <span data-ttu-id="6d677-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6d677-108">Example 1</span></span>
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

<span data-ttu-id="6d677-109">Esse comando cria um grupo de hosts no local e na zona especificados.</span><span class="sxs-lookup"><span data-stu-id="6d677-109">This command creates a host group in the given location and zone.</span></span>

## <span data-ttu-id="6d677-110">OS</span><span class="sxs-lookup"><span data-stu-id="6d677-110">PARAMETERS</span></span>

### <span data-ttu-id="6d677-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6d677-111">-AsJob</span></span>
<span data-ttu-id="6d677-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="6d677-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6d677-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d677-113">-DefaultProfile</span></span>
<span data-ttu-id="6d677-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6d677-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d677-115">-Local</span><span class="sxs-lookup"><span data-stu-id="6d677-115">-Location</span></span>
<span data-ttu-id="6d677-116">Especifica o local.</span><span class="sxs-lookup"><span data-stu-id="6d677-116">Specifies location.</span></span>

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

### <span data-ttu-id="6d677-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="6d677-117">-Name</span></span>
<span data-ttu-id="6d677-118">Especifica o nome do grupo host.</span><span class="sxs-lookup"><span data-stu-id="6d677-118">Specifies the name of the host group.</span></span>

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

### <span data-ttu-id="6d677-119">-PlatformFaultDomain</span><span class="sxs-lookup"><span data-stu-id="6d677-119">-PlatformFaultDomain</span></span>
<span data-ttu-id="6d677-120">Especifica o número de domínios de falha que o grupo de hosts pode abranger.</span><span class="sxs-lookup"><span data-stu-id="6d677-120">Specifies the number of fault domains that the host group can span.</span></span>  <span data-ttu-id="6d677-121">O valor mínimo é 1 e o valor máximo é 3.</span><span class="sxs-lookup"><span data-stu-id="6d677-121">The minimum value is 1 and the maximum value is 3.</span></span>

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

### <span data-ttu-id="6d677-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d677-122">-ResourceGroupName</span></span>
<span data-ttu-id="6d677-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6d677-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="6d677-124">-Marca</span><span class="sxs-lookup"><span data-stu-id="6d677-124">-Tag</span></span>
<span data-ttu-id="6d677-125">Especifica marcas</span><span class="sxs-lookup"><span data-stu-id="6d677-125">Specifies Tags</span></span>

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

### <span data-ttu-id="6d677-126">-Zone</span><span class="sxs-lookup"><span data-stu-id="6d677-126">-Zone</span></span>
<span data-ttu-id="6d677-127">Especifica zonas do grupo host.</span><span class="sxs-lookup"><span data-stu-id="6d677-127">Specifies Zones of the host group.</span></span>

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

### <span data-ttu-id="6d677-128">-SupportAutomaticPlacement</span><span class="sxs-lookup"><span data-stu-id="6d677-128">-SupportAutomaticPlacement</span></span>
<span data-ttu-id="6d677-129">Especifica se o controlador de host habilitará o posicionamento automático de máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="6d677-129">Specifies if HostGroup will enable automatic placement of vm's.</span></span>
<span data-ttu-id="6d677-130">Posicionamento automático significa que essas VMs são colocadas em hosts dedicados, escolhidos pelo Azure, sob o grupo host dedicado.</span><span class="sxs-lookup"><span data-stu-id="6d677-130">Automatic placement means these VMs are placed on dedicated hosts, chosen by Azure, under the dedicated host group.</span></span>
<span data-ttu-id="6d677-131">Se não for especificado, o valor padrão será true.</span><span class="sxs-lookup"><span data-stu-id="6d677-131">If not specified, default value will be true.</span></span>

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


### <span data-ttu-id="6d677-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6d677-132">-Confirm</span></span>
<span data-ttu-id="6d677-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d677-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d677-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d677-134">-WhatIf</span></span>
<span data-ttu-id="6d677-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6d677-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d677-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6d677-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d677-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d677-137">CommonParameters</span></span>
<span data-ttu-id="6d677-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d677-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d677-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6d677-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d677-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6d677-140">INPUTS</span></span>

### <span data-ttu-id="6d677-141">System. String</span><span class="sxs-lookup"><span data-stu-id="6d677-141">System.String</span></span>

## <span data-ttu-id="6d677-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6d677-142">OUTPUTS</span></span>

### <span data-ttu-id="6d677-143">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="6d677-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="6d677-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6d677-144">NOTES</span></span>

## <span data-ttu-id="6d677-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6d677-145">RELATED LINKS</span></span>
