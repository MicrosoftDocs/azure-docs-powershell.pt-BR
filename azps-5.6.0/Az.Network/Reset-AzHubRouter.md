---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/reset-azhubrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzHubRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzHubRouter.md
ms.openlocfilehash: 2261e3e0f9237985459dc69e06ba4f055dd86427
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886719"
---
# <span data-ttu-id="ebac1-101">Reset-AzHubRouter</span><span class="sxs-lookup"><span data-stu-id="ebac1-101">Reset-AzHubRouter</span></span>

## <span data-ttu-id="ebac1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ebac1-102">SYNOPSIS</span></span>
<span data-ttu-id="ebac1-103">Redefine RoutingState de um recurso VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="ebac1-103">Resets the RoutingState of a VirtualHub resource.</span></span>

## <span data-ttu-id="ebac1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ebac1-104">SYNTAX</span></span>

### <span data-ttu-id="ebac1-105">ByVirtualHubName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ebac1-105">ByVirtualHubName (Default)</span></span>
```
Reset-AzHubRouter -ResourceGroupName <String> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebac1-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="ebac1-106">ByVirtualHubResourceId</span></span>
```
Reset-AzHubRouter -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebac1-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="ebac1-107">ByVirtualHubObject</span></span>
```
Reset-AzHubRouter -InputObject <PSVirtualHub> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ebac1-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ebac1-108">DESCRIPTION</span></span>
<span data-ttu-id="ebac1-109">Redefine o Estado de Roteamento de um recurso VirtualHub existente somente se o Estado de Roteamento do hub virtual não for Provisionado.</span><span class="sxs-lookup"><span data-stu-id="ebac1-109">Resets the Routing State of an existing VirtualHub resource only if the Routing State of the virtual hub is not Provisioned.</span></span>

## <span data-ttu-id="ebac1-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ebac1-110">EXAMPLES</span></span>

### <span data-ttu-id="ebac1-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ebac1-111">Example 1</span></span>

```powershell
PS C:\> Reset-AzHubRouter -ResourceGroupName "testRG" -Name "westushub"
```

<span data-ttu-id="ebac1-112">Redefina o estado de roteamento do hub virtual usando resourceGroupName e ResourceName.</span><span class="sxs-lookup"><span data-stu-id="ebac1-112">Reset the routing state of the virtual hub using its ResourceGroupName and ResourceName.</span></span>

### <span data-ttu-id="ebac1-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ebac1-113">Example 2</span></span>

```powershell
PS C:\> Reset-AzHubRouter -ResourceId "/subscriptions/testSub/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub"
```

<span data-ttu-id="ebac1-114">Redefina o estado de roteamento do hub virtual usando sua ResourceId.</span><span class="sxs-lookup"><span data-stu-id="ebac1-114">Reset the routing state of the virtual hub using its ResourceId.</span></span>

### <span data-ttu-id="ebac1-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="ebac1-115">Example 3</span></span>

```powershell
PS C:\> Reset-AzHubRouter -InputObject $virtualHub
```

<span data-ttu-id="ebac1-116">Redefina o estado de roteamento do hub virtual usando um objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="ebac1-116">Reset the routing state of the virtual hub using an input object.</span></span> <span data-ttu-id="ebac1-117">O objeto de entrada é do tipo PSVirtualHub.</span><span class="sxs-lookup"><span data-stu-id="ebac1-117">The input object is of type PSVirtualHub.</span></span>

### <span data-ttu-id="ebac1-118">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="ebac1-118">Example 4</span></span>

```powershell
PS C:\> Get-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub" | Reset-AzHubRouter
```

<span data-ttu-id="ebac1-119">Um objeto de hub virtual existente pode ser recuperado e passado como objeto de entrada para Reset-AzHubRouter.</span><span class="sxs-lookup"><span data-stu-id="ebac1-119">An existing virtual hub object can be retrieved and then passed as input object to Reset-AzHubRouter.</span></span>

## <span data-ttu-id="ebac1-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ebac1-120">PARAMETERS</span></span>

### <span data-ttu-id="ebac1-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ebac1-121">-AsJob</span></span>
<span data-ttu-id="ebac1-122">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="ebac1-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ebac1-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebac1-123">-DefaultProfile</span></span>
<span data-ttu-id="ebac1-124">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ebac1-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ebac1-125">-Force</span><span class="sxs-lookup"><span data-stu-id="ebac1-125">-Force</span></span>
<span data-ttu-id="ebac1-126">Não peça confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="ebac1-126">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="ebac1-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ebac1-127">-InputObject</span></span>
<span data-ttu-id="ebac1-128">O objeto de hub virtual a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="ebac1-128">The Virtual hub object to be modified.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: VirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ebac1-129">-Name</span><span class="sxs-lookup"><span data-stu-id="ebac1-129">-Name</span></span>
<span data-ttu-id="ebac1-130">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="ebac1-130">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases: ResourceName, VirtualHubName, HubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebac1-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebac1-131">-ResourceGroupName</span></span>
<span data-ttu-id="ebac1-132">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ebac1-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebac1-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ebac1-133">-ResourceId</span></span>
<span data-ttu-id="ebac1-134">A id de recurso do hub virtual a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="ebac1-134">The resource id of the Virtual hub to be modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebac1-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ebac1-135">-Confirm</span></span>
<span data-ttu-id="ebac1-136">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ebac1-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ebac1-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebac1-137">-WhatIf</span></span>
<span data-ttu-id="ebac1-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ebac1-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ebac1-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ebac1-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ebac1-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebac1-140">CommonParameters</span></span>
<span data-ttu-id="ebac1-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebac1-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebac1-142">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebac1-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebac1-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ebac1-143">INPUTS</span></span>

### <span data-ttu-id="ebac1-144">System.String</span><span class="sxs-lookup"><span data-stu-id="ebac1-144">System.String</span></span>

### <span data-ttu-id="ebac1-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="ebac1-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="ebac1-146">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ebac1-146">OUTPUTS</span></span>

### <span data-ttu-id="ebac1-147">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="ebac1-147">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="ebac1-148">NOTES</span><span class="sxs-lookup"><span data-stu-id="ebac1-148">NOTES</span></span>

## <span data-ttu-id="ebac1-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ebac1-149">RELATED LINKS</span></span>

[<span data-ttu-id="ebac1-150">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="ebac1-150">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)
