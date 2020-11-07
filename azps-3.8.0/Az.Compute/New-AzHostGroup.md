---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHostGroup.md
ms.openlocfilehash: f83a52281cbe244e91b22300b7f10582d6ca6349
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941459"
---
# <span data-ttu-id="b2e8b-101">New-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="b2e8b-101">New-AzHostGroup</span></span>

## <span data-ttu-id="b2e8b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b2e8b-102">SYNOPSIS</span></span>
<span data-ttu-id="b2e8b-103">Cria um grupo de hosts.</span><span class="sxs-lookup"><span data-stu-id="b2e8b-103">Creates a host group.</span></span>

## <span data-ttu-id="b2e8b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b2e8b-104">SYNTAX</span></span>

```
New-AzHostGroup [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 -PlatformFaultDomain <Int32> [-Zone <String[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2e8b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b2e8b-105">DESCRIPTION</span></span>
<span data-ttu-id="b2e8b-106">Esse cmdlet criará um grupo de hosts.</span><span class="sxs-lookup"><span data-stu-id="b2e8b-106">This cmdlet will create a Host group.</span></span>

## <span data-ttu-id="b2e8b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b2e8b-107">EXAMPLES</span></span>

### <span data-ttu-id="b2e8b-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b2e8b-108">Example 1</span></span>
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

<span data-ttu-id="b2e8b-109">Esse comando cria um grupo de hosts no local e na zona especificados.</span><span class="sxs-lookup"><span data-stu-id="b2e8b-109">This command creates a host group in the given location and zone.</span></span>

## <span data-ttu-id="b2e8b-110">OS</span><span class="sxs-lookup"><span data-stu-id="b2e8b-110">PARAMETERS</span></span>

### <span data-ttu-id="b2e8b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b2e8b-111">-AsJob</span></span>
<span data-ttu-id="b2e8b-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="b2e8b-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b2e8b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2e8b-113">-DefaultProfile</span></span>
<span data-ttu-id="b2e8b-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b2e8b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2e8b-115">-Local</span><span class="sxs-lookup"><span data-stu-id="b2e8b-115">-Location</span></span>
<span data-ttu-id="b2e8b-116">Especifica o local.</span><span class="sxs-lookup"><span data-stu-id="b2e8b-116">Specifies location.</span></span>

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

### <span data-ttu-id="b2e8b-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="b2e8b-117">-Name</span></span>
<span data-ttu-id="b2e8b-118">Especifica o nome do grupo host.</span><span class="sxs-lookup"><span data-stu-id="b2e8b-118">Specifies the name of the host group.</span></span>

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

### <span data-ttu-id="b2e8b-119">-PlatformFaultDomain</span><span class="sxs-lookup"><span data-stu-id="b2e8b-119">-PlatformFaultDomain</span></span>
<span data-ttu-id="b2e8b-120">Especifica o número de domínios de falha que o grupo de hosts pode abranger.</span><span class="sxs-lookup"><span data-stu-id="b2e8b-120">Specifies the number of fault domains that the host group can span.</span></span>  <span data-ttu-id="b2e8b-121">O valor mínimo é 1 e o valor máximo é 3.</span><span class="sxs-lookup"><span data-stu-id="b2e8b-121">The minimum value is 1 and the maximum value is 3.</span></span>

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

### <span data-ttu-id="b2e8b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2e8b-122">-ResourceGroupName</span></span>
<span data-ttu-id="b2e8b-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b2e8b-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="b2e8b-124">-Marca</span><span class="sxs-lookup"><span data-stu-id="b2e8b-124">-Tag</span></span>
<span data-ttu-id="b2e8b-125">Especifica marcas</span><span class="sxs-lookup"><span data-stu-id="b2e8b-125">Specifies Tags</span></span>

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

### <span data-ttu-id="b2e8b-126">-Zone</span><span class="sxs-lookup"><span data-stu-id="b2e8b-126">-Zone</span></span>
<span data-ttu-id="b2e8b-127">Especifica zonas do grupo host.</span><span class="sxs-lookup"><span data-stu-id="b2e8b-127">Specifies Zones of the host group.</span></span>

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

### <span data-ttu-id="b2e8b-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b2e8b-128">-Confirm</span></span>
<span data-ttu-id="b2e8b-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2e8b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2e8b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2e8b-130">-WhatIf</span></span>
<span data-ttu-id="b2e8b-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b2e8b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2e8b-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b2e8b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2e8b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2e8b-133">CommonParameters</span></span>
<span data-ttu-id="b2e8b-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2e8b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2e8b-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b2e8b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2e8b-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b2e8b-136">INPUTS</span></span>

### <span data-ttu-id="b2e8b-137">System. String</span><span class="sxs-lookup"><span data-stu-id="b2e8b-137">System.String</span></span>

## <span data-ttu-id="b2e8b-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b2e8b-138">OUTPUTS</span></span>

### <span data-ttu-id="b2e8b-139">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="b2e8b-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="b2e8b-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b2e8b-140">NOTES</span></span>

## <span data-ttu-id="b2e8b-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b2e8b-141">RELATED LINKS</span></span>
