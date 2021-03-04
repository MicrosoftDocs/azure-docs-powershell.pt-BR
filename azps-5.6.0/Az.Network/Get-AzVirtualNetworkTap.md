---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkTap.md
ms.openlocfilehash: 154cededf20ceb88fdbc851b96189282e1b6123a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892101"
---
# <span data-ttu-id="1c2d9-101">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="1c2d9-101">Get-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="1c2d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c2d9-102">SYNOPSIS</span></span>
<span data-ttu-id="1c2d9-103">Obtém um toque de rede virtual</span><span class="sxs-lookup"><span data-stu-id="1c2d9-103">Gets a virtual network tap</span></span>

## <span data-ttu-id="1c2d9-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="1c2d9-104">SYNTAX</span></span>

### <span data-ttu-id="1c2d9-105">ListParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="1c2d9-105">ListParameterSet (Default)</span></span>
```
Get-AzVirtualNetworkTap [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c2d9-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c2d9-106">GetByResourceIdParameterSet</span></span>
```
Get-AzVirtualNetworkTap -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1c2d9-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="1c2d9-107">DESCRIPTION</span></span>
<span data-ttu-id="1c2d9-108">O cmdlet **Get-AzVirtualNetworkTap** obtém um toque de rede virtual do Azure ou uma lista de toques de rede virtual do Azure em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1c2d9-108">The **Get-AzVirtualNetworkTap** cmdlet gets an Azure virtual network tap or a list of Azure virtual network taps in a resource group.</span></span>

## <span data-ttu-id="1c2d9-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1c2d9-109">EXAMPLES</span></span>

### <span data-ttu-id="1c2d9-110">Exemplo 1: Obter um toque de rede virtual</span><span class="sxs-lookup"><span data-stu-id="1c2d9-110">Example 1: Get a virtual network tap</span></span>
```
PS C:\> Get-AzVirtualNetworkTap -ResourceGroupName "ResourceGroup1" -Name "VirtualTap1"
```

<span data-ttu-id="1c2d9-111">Este comando obtém uma referência de toque virtualNetwork para determinado "VirtualTap1" em "ResourceGroup1".</span><span class="sxs-lookup"><span data-stu-id="1c2d9-111">This command gets a VirtualNetwork tap reference for given "VirtualTap1" in "ResourceGroup1".</span></span>

### <span data-ttu-id="1c2d9-112">Exemplo 2: Obter todos os toques de rede virtual usando filtragem</span><span class="sxs-lookup"><span data-stu-id="1c2d9-112">Example 2: Get all virtual network taps using filtering</span></span>
```
PS C:\> Get-AzVirtualNetworkTap -Name "VirtualTap*"
```

<span data-ttu-id="1c2d9-113">Este comando obtém todas as referências de toque virtualNetwork que começam com "VirtualTap".</span><span class="sxs-lookup"><span data-stu-id="1c2d9-113">This command gets all VirtualNetwork tap references that start with "VirtualTap".</span></span>

## <span data-ttu-id="1c2d9-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="1c2d9-114">PARAMETERS</span></span>

### <span data-ttu-id="1c2d9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c2d9-115">-DefaultProfile</span></span>
<span data-ttu-id="1c2d9-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1c2d9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c2d9-117">-Name</span><span class="sxs-lookup"><span data-stu-id="1c2d9-117">-Name</span></span>
<span data-ttu-id="1c2d9-118">O nome do toque.</span><span class="sxs-lookup"><span data-stu-id="1c2d9-118">The name of the tap.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="1c2d9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c2d9-119">-ResourceGroupName</span></span>
<span data-ttu-id="1c2d9-120">O nome do grupo de recursos do toque de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="1c2d9-120">The resource group name of the virtual network tap.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="1c2d9-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1c2d9-121">-ResourceId</span></span>
<span data-ttu-id="1c2d9-122">ResourceId do recurso VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="1c2d9-122">ResourceId of the VirtualNetworkTap resource</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c2d9-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1c2d9-123">-Confirm</span></span>
<span data-ttu-id="1c2d9-124">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c2d9-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c2d9-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c2d9-125">-WhatIf</span></span>
<span data-ttu-id="1c2d9-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1c2d9-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1c2d9-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1c2d9-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c2d9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c2d9-128">CommonParameters</span></span>
<span data-ttu-id="1c2d9-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c2d9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c2d9-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1c2d9-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c2d9-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1c2d9-131">INPUTS</span></span>

### <span data-ttu-id="1c2d9-132">System.String</span><span class="sxs-lookup"><span data-stu-id="1c2d9-132">System.String</span></span>

## <span data-ttu-id="1c2d9-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="1c2d9-133">OUTPUTS</span></span>

### <span data-ttu-id="1c2d9-134">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="1c2d9-134">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="1c2d9-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="1c2d9-135">NOTES</span></span>

## <span data-ttu-id="1c2d9-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1c2d9-136">RELATED LINKS</span></span>

[<span data-ttu-id="1c2d9-137">New-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="1c2d9-137">New-AzVirtualNetworkTap</span></span>](./New-AzVirtualNetworkTap.md)

[<span data-ttu-id="1c2d9-138">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="1c2d9-138">Remove-AzVirtualNetworkTap</span></span>](./Remove-AzVirtualNetworkTap.md)

[<span data-ttu-id="1c2d9-139">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="1c2d9-139">Set-AzVirtualNetworkTap</span></span>](./Set-AzVirtualNetworkTap.md)
