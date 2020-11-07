---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringService.md
ms.openlocfilehash: 60772963530d14eeb93f2f28fbf5e067ac5833ab
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944473"
---
# <span data-ttu-id="dd82f-101">New-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="dd82f-101">New-AzPeeringService</span></span>

## <span data-ttu-id="dd82f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dd82f-102">SYNOPSIS</span></span>
<span data-ttu-id="dd82f-103">Cria um novo serviço de emparelhamento.</span><span class="sxs-lookup"><span data-stu-id="dd82f-103">Creates a new peering service.</span></span>

## <span data-ttu-id="dd82f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dd82f-104">SYNTAX</span></span>

```
New-AzPeeringService [-ResourceGroupName] <String> [-Name] <String> [-PeeringLocation] <String>
 [-PeeringServiceProvider] <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd82f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dd82f-105">DESCRIPTION</span></span>
<span data-ttu-id="dd82f-106">Cria um serviço de emparelhamento.</span><span class="sxs-lookup"><span data-stu-id="dd82f-106">Creates peering service.</span></span>

## <span data-ttu-id="dd82f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dd82f-107">EXAMPLES</span></span>

### <span data-ttu-id="dd82f-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="dd82f-108">Example 1</span></span>
```powershell
PS C:\> New-AzPeeringService -ResourceGroupName $resourceGroup -Name $name -Location $loc -PeeringServiceProvider $provider

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService3990
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService3990
Type                   : Microsoft.Peering/peeringServices
```

<span data-ttu-id="dd82f-109">Cria um objeto de serviço de emparelhamento com o provedor e o local de emparelhamento.</span><span class="sxs-lookup"><span data-stu-id="dd82f-109">Creates a peering service object with provider and peering location.</span></span> <span data-ttu-id="dd82f-110">Use no conjuction com `Get-AzPeeringServiceProvider` e `Get-AzPeeringServiceLocation`</span><span class="sxs-lookup"><span data-stu-id="dd82f-110">Use in conjuction with `Get-AzPeeringServiceProvider` and `Get-AzPeeringServiceLocation`</span></span>

## <span data-ttu-id="dd82f-111">OS</span><span class="sxs-lookup"><span data-stu-id="dd82f-111">PARAMETERS</span></span>

### <span data-ttu-id="dd82f-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dd82f-112">-AsJob</span></span>
<span data-ttu-id="dd82f-113">Executar em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="dd82f-113">Run in the background.</span></span>

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

### <span data-ttu-id="dd82f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd82f-114">-DefaultProfile</span></span>
<span data-ttu-id="dd82f-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dd82f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd82f-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="dd82f-116">-Name</span></span>
<span data-ttu-id="dd82f-117">O nome exclusivo da PSPeering.</span><span class="sxs-lookup"><span data-stu-id="dd82f-117">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd82f-118">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="dd82f-118">-PeeringLocation</span></span>
<span data-ttu-id="dd82f-119">A localização física é diferente da região do Azure.</span><span class="sxs-lookup"><span data-stu-id="dd82f-119">The Physical Location Different from Azure Region.</span></span> <span data-ttu-id="dd82f-120">Usar Get-AzPeeringServiceLocation [-Country <country> ]</span><span class="sxs-lookup"><span data-stu-id="dd82f-120">Use Get-AzPeeringServiceLocation [-Country <country>]</span></span>

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

### <span data-ttu-id="dd82f-121">-PeeringServiceProvider</span><span class="sxs-lookup"><span data-stu-id="dd82f-121">-PeeringServiceProvider</span></span>
<span data-ttu-id="dd82f-122">O nome do provedor de serviço de emparelhamento.</span><span class="sxs-lookup"><span data-stu-id="dd82f-122">The peering service provider name.</span></span>
<span data-ttu-id="dd82f-123">Usar o cmdlet Get-AzPeeringServiceProvider para uma lista</span><span class="sxs-lookup"><span data-stu-id="dd82f-123">Use Get-AzPeeringServiceProvider cmdlet for a list</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd82f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd82f-124">-ResourceGroupName</span></span>
<span data-ttu-id="dd82f-125">Criar ou usar um nome de grupo de recursos existente.</span><span class="sxs-lookup"><span data-stu-id="dd82f-125">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd82f-126">-Marca</span><span class="sxs-lookup"><span data-stu-id="dd82f-126">-Tag</span></span>
<span data-ttu-id="dd82f-127">As marcas a serem associadas ao serviço Microsoft InputObject.</span><span class="sxs-lookup"><span data-stu-id="dd82f-127">The tags to associate with the Microsoft InputObject Service.</span></span>

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

### <span data-ttu-id="dd82f-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="dd82f-128">-Confirm</span></span>
<span data-ttu-id="dd82f-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd82f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd82f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd82f-130">-WhatIf</span></span>
<span data-ttu-id="dd82f-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="dd82f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd82f-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dd82f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd82f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd82f-133">CommonParameters</span></span>
<span data-ttu-id="dd82f-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd82f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd82f-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dd82f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd82f-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dd82f-136">INPUTS</span></span>

### <span data-ttu-id="dd82f-137">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="dd82f-137">None</span></span>

## <span data-ttu-id="dd82f-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dd82f-138">OUTPUTS</span></span>

### <span data-ttu-id="dd82f-139">Microsoft. Azure. PowerShell. cmdlets. peering. Models. PSPeeringService</span><span class="sxs-lookup"><span data-stu-id="dd82f-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="dd82f-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dd82f-140">NOTES</span></span>

## <span data-ttu-id="dd82f-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dd82f-141">RELATED LINKS</span></span>
