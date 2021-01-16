---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azhubrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzHubRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzHubRouter.md
ms.openlocfilehash: 039d37f9d9dd7b5af026b7ce2a87113513949b67
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272597"
---
# <span data-ttu-id="55200-101">Reset-AzHubRouter</span><span class="sxs-lookup"><span data-stu-id="55200-101">Reset-AzHubRouter</span></span>

## <span data-ttu-id="55200-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="55200-102">SYNOPSIS</span></span>
<span data-ttu-id="55200-103">Redefine o RoutingState de um recurso VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="55200-103">Resets the RoutingState of a VirtualHub resource.</span></span>

## <span data-ttu-id="55200-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="55200-104">SYNTAX</span></span>

### <span data-ttu-id="55200-105">ByVirtualHubName (padrão)</span><span class="sxs-lookup"><span data-stu-id="55200-105">ByVirtualHubName (Default)</span></span>
```
Reset-AzHubRouter -ResourceGroupName <String> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55200-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="55200-106">ByVirtualHubResourceId</span></span>
```
Reset-AzHubRouter -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55200-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="55200-107">ByVirtualHubObject</span></span>
```
Reset-AzHubRouter -InputObject <PSVirtualHub> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55200-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="55200-108">DESCRIPTION</span></span>
<span data-ttu-id="55200-109">Redefine o estado de roteamento de um recurso VirtualHub existente somente se o estado de roteamento do Hub virtual não for provisionado.</span><span class="sxs-lookup"><span data-stu-id="55200-109">Resets the Routing State of an existing VirtualHub resource only if the Routing State of the virtual hub is not Provisioned.</span></span>

## <span data-ttu-id="55200-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="55200-110">EXAMPLES</span></span>

### <span data-ttu-id="55200-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="55200-111">Example 1</span></span>

```powershell
PS C:\> Reset-AzHubRouter -ResourceGroupName "testRG" -Name "westushub"
```

<span data-ttu-id="55200-112">Redefina o estado de roteamento do Hub virtual usando seu ResourceGroupName e Resource Resource.</span><span class="sxs-lookup"><span data-stu-id="55200-112">Reset the routing state of the virtual hub using its ResourceGroupName and ResourceName.</span></span>

### <span data-ttu-id="55200-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="55200-113">Example 2</span></span>

```powershell
PS C:\> Reset-AzHubRouter -ResourceId "/subscriptions/testSub/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub"
```

<span data-ttu-id="55200-114">Redefina o estado de roteamento do Hub virtual usando seu ResourceId.</span><span class="sxs-lookup"><span data-stu-id="55200-114">Reset the routing state of the virtual hub using its ResourceId.</span></span>

### <span data-ttu-id="55200-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="55200-115">Example 3</span></span>

```powershell
PS C:\> Reset-AzHubRouter -InputObject $virtualHub
```

<span data-ttu-id="55200-116">Redefina o estado de roteamento do Hub virtual usando um objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="55200-116">Reset the routing state of the virtual hub using an input object.</span></span> <span data-ttu-id="55200-117">O objeto de entrada é do tipo PSVirtualHub.</span><span class="sxs-lookup"><span data-stu-id="55200-117">The input object is of type PSVirtualHub.</span></span>

### <span data-ttu-id="55200-118">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="55200-118">Example 4</span></span>

```powershell
PS C:\> Get-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub" | Reset-AzHubRouter
```

<span data-ttu-id="55200-119">Um objeto Hub virtual existente pode ser recuperado e, em seguida, passado como objeto de entrada para Reset-AzHubRouter.</span><span class="sxs-lookup"><span data-stu-id="55200-119">An existing virtual hub object can be retrieved and then passed as input object to Reset-AzHubRouter.</span></span>

## <span data-ttu-id="55200-120">OS</span><span class="sxs-lookup"><span data-stu-id="55200-120">PARAMETERS</span></span>

### <span data-ttu-id="55200-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="55200-121">-AsJob</span></span>
<span data-ttu-id="55200-122">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="55200-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="55200-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55200-123">-DefaultProfile</span></span>
<span data-ttu-id="55200-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="55200-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55200-125">-Force</span><span class="sxs-lookup"><span data-stu-id="55200-125">-Force</span></span>
<span data-ttu-id="55200-126">Não pedir confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="55200-126">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="55200-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="55200-127">-InputObject</span></span>
<span data-ttu-id="55200-128">O objeto de Hub virtual a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="55200-128">The Virtual hub object to be modified.</span></span>

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

### <span data-ttu-id="55200-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="55200-129">-Name</span></span>
<span data-ttu-id="55200-130">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="55200-130">The resource name.</span></span>

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

### <span data-ttu-id="55200-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55200-131">-ResourceGroupName</span></span>
<span data-ttu-id="55200-132">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="55200-132">The resource group name.</span></span>

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

### <span data-ttu-id="55200-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="55200-133">-ResourceId</span></span>
<span data-ttu-id="55200-134">A ID do recurso do Hub virtual a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="55200-134">The resource id of the Virtual hub to be modified.</span></span>

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

### <span data-ttu-id="55200-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="55200-135">-Confirm</span></span>
<span data-ttu-id="55200-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55200-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55200-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55200-137">-WhatIf</span></span>
<span data-ttu-id="55200-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="55200-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55200-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="55200-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55200-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55200-140">CommonParameters</span></span>
<span data-ttu-id="55200-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55200-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55200-142">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55200-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55200-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="55200-143">INPUTS</span></span>

### <span data-ttu-id="55200-144">System. String</span><span class="sxs-lookup"><span data-stu-id="55200-144">System.String</span></span>

### <span data-ttu-id="55200-145">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="55200-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="55200-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="55200-146">OUTPUTS</span></span>

### <span data-ttu-id="55200-147">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="55200-147">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="55200-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="55200-148">NOTES</span></span>

## <span data-ttu-id="55200-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="55200-149">RELATED LINKS</span></span>

[<span data-ttu-id="55200-150">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="55200-150">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)
