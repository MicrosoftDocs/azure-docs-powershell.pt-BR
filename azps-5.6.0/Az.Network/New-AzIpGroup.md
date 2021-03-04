---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpGroup.md
ms.openlocfilehash: c8959d281c5eda7e2dd3f40941f5c727a000c588
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889185"
---
# <span data-ttu-id="7bd68-101">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="7bd68-101">New-AzIpGroup</span></span>

## <span data-ttu-id="7bd68-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7bd68-102">SYNOPSIS</span></span>
<span data-ttu-id="7bd68-103">Cria um Azure IpGroup.</span><span class="sxs-lookup"><span data-stu-id="7bd68-103">Creates an Azure IpGroup.</span></span>

## <span data-ttu-id="7bd68-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7bd68-104">SYNTAX</span></span>

```
New-AzIpGroup -Name <String> -ResourceGroupName <String> [-IpAddress <String[]>] -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7bd68-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7bd68-105">DESCRIPTION</span></span>
<span data-ttu-id="7bd68-106">O cmdlet **New-AzIpGroup** cria um Azure IpGroup</span><span class="sxs-lookup"><span data-stu-id="7bd68-106">The **New-AzIpGroup** cmdlet creates an Azure IpGroup</span></span>

## <span data-ttu-id="7bd68-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7bd68-107">EXAMPLES</span></span>

### <span data-ttu-id="7bd68-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7bd68-108">Example 1</span></span>
```powershell
New-AzIpGroup -Name ipGroup -ResourceGroupName ipGroupRG -Location 'West US'
```

### <span data-ttu-id="7bd68-109">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="7bd68-109">Example 2</span></span>
```powershell
New-AzIpGroup -Name ipGroup -ResourceGroupName ipGroupRG -Location 'West US' -IpAddress 10.0.0.0/24,11.9.0.0/24
```

## <span data-ttu-id="7bd68-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7bd68-110">PARAMETERS</span></span>

### <span data-ttu-id="7bd68-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7bd68-111">-AsJob</span></span>
<span data-ttu-id="7bd68-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="7bd68-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bd68-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bd68-113">-DefaultProfile</span></span>
<span data-ttu-id="7bd68-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7bd68-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bd68-115">-Force</span><span class="sxs-lookup"><span data-stu-id="7bd68-115">-Force</span></span>
<span data-ttu-id="7bd68-116">Não peça confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="7bd68-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bd68-117">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="7bd68-117">-IpAddress</span></span>
<span data-ttu-id="7bd68-118">IpAddresses definidos no IpGroup</span><span class="sxs-lookup"><span data-stu-id="7bd68-118">IpAddresses defined in the IpGroup</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bd68-119">-Location</span><span class="sxs-lookup"><span data-stu-id="7bd68-119">-Location</span></span>
<span data-ttu-id="7bd68-120">O local.</span><span class="sxs-lookup"><span data-stu-id="7bd68-120">The location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bd68-121">-Name</span><span class="sxs-lookup"><span data-stu-id="7bd68-121">-Name</span></span>
<span data-ttu-id="7bd68-122">O nome do grupo de ip.</span><span class="sxs-lookup"><span data-stu-id="7bd68-122">The name of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bd68-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bd68-123">-ResourceGroupName</span></span>
<span data-ttu-id="7bd68-124">O nome do grupo de recursos do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7bd68-124">The resource group name of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bd68-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="7bd68-125">-Tag</span></span>
<span data-ttu-id="7bd68-126">Uma hashtable que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="7bd68-126">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bd68-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7bd68-127">-Confirm</span></span>
<span data-ttu-id="7bd68-128">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7bd68-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bd68-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bd68-129">-WhatIf</span></span>
<span data-ttu-id="7bd68-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7bd68-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7bd68-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7bd68-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bd68-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bd68-132">CommonParameters</span></span>
<span data-ttu-id="7bd68-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bd68-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bd68-134">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7bd68-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bd68-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7bd68-135">INPUTS</span></span>

### <span data-ttu-id="7bd68-136">System.String</span><span class="sxs-lookup"><span data-stu-id="7bd68-136">System.String</span></span>

### <span data-ttu-id="7bd68-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7bd68-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="7bd68-138">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="7bd68-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7bd68-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7bd68-139">OUTPUTS</span></span>

### <span data-ttu-id="7bd68-140">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="7bd68-140">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="7bd68-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="7bd68-141">NOTES</span></span>

## <span data-ttu-id="7bd68-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7bd68-142">RELATED LINKS</span></span>
