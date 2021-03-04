---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/powershell/module/az.signalr/remove-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Remove-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Remove-AzSignalR.md
ms.openlocfilehash: 067dd93f28a5019de96f146a237fe131a9717bfc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885819"
---
# <span data-ttu-id="a6b8c-101">Remove-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="a6b8c-101">Remove-AzSignalR</span></span>

## <span data-ttu-id="a6b8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6b8c-102">SYNOPSIS</span></span>
<span data-ttu-id="a6b8c-103">Remova um serviço SignalR.</span><span class="sxs-lookup"><span data-stu-id="a6b8c-103">Remove a SignalR service.</span></span>

## <span data-ttu-id="a6b8c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a6b8c-104">SYNTAX</span></span>

### <span data-ttu-id="a6b8c-105">ResourceGroupParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a6b8c-105">ResourceGroupParameterSet (Default)</span></span>
```
Remove-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6b8c-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6b8c-106">ResourceIdParameterSet</span></span>
```
Remove-AzSignalR -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6b8c-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6b8c-107">InputObjectParameterSet</span></span>
```
Remove-AzSignalR -InputObject <PSSignalRResource> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6b8c-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a6b8c-108">DESCRIPTION</span></span>
<span data-ttu-id="a6b8c-109">Remova um serviço SignalR.</span><span class="sxs-lookup"><span data-stu-id="a6b8c-109">Remove a SignalR service.</span></span>

## <span data-ttu-id="a6b8c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a6b8c-110">EXAMPLES</span></span>

### <span data-ttu-id="a6b8c-111">Remover um serviço SignalR</span><span class="sxs-lookup"><span data-stu-id="a6b8c-111">Remove a SignalR service</span></span>
```
PS C:\> Remove-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -PassThru

True
```

### <span data-ttu-id="a6b8c-112">Remover todo o serviço signalr do pipe</span><span class="sxs-lookup"><span data-stu-id="a6b8c-112">Remove all SignalR service from pipe</span></span>
```
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup | Remove-AzSignalR
```

## <span data-ttu-id="a6b8c-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a6b8c-113">PARAMETERS</span></span>

### <span data-ttu-id="a6b8c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a6b8c-114">-AsJob</span></span>
<span data-ttu-id="a6b8c-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="a6b8c-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6b8c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6b8c-116">-DefaultProfile</span></span>
<span data-ttu-id="a6b8c-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a6b8c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6b8c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6b8c-118">-InputObject</span></span>
<span data-ttu-id="a6b8c-119">O objeto de recurso SignalR.</span><span class="sxs-lookup"><span data-stu-id="a6b8c-119">The SignalR resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6b8c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="a6b8c-120">-Name</span></span>
<span data-ttu-id="a6b8c-121">Nome do serviço signalr.</span><span class="sxs-lookup"><span data-stu-id="a6b8c-121">SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6b8c-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a6b8c-122">-PassThru</span></span>
<span data-ttu-id="a6b8c-123">Retorna true se a remoção foi concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="a6b8c-123">Returns true if the removal was completed successfully.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6b8c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6b8c-124">-ResourceGroupName</span></span>
<span data-ttu-id="a6b8c-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a6b8c-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6b8c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a6b8c-126">-ResourceId</span></span>
<span data-ttu-id="a6b8c-127">A ID do recurso de serviço SignalR.</span><span class="sxs-lookup"><span data-stu-id="a6b8c-127">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6b8c-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a6b8c-128">-Confirm</span></span>
<span data-ttu-id="a6b8c-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6b8c-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6b8c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6b8c-130">-WhatIf</span></span>
<span data-ttu-id="a6b8c-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a6b8c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6b8c-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a6b8c-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6b8c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6b8c-133">CommonParameters</span></span>
<span data-ttu-id="a6b8c-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6b8c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6b8c-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a6b8c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6b8c-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a6b8c-136">INPUTS</span></span>

### <span data-ttu-id="a6b8c-137">System.String</span><span class="sxs-lookup"><span data-stu-id="a6b8c-137">System.String</span></span>
### <span data-ttu-id="a6b8c-138">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="a6b8c-138">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="a6b8c-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a6b8c-139">OUTPUTS</span></span>

### <span data-ttu-id="a6b8c-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a6b8c-140">System.Boolean</span></span>
## <span data-ttu-id="a6b8c-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="a6b8c-141">NOTES</span></span>

## <span data-ttu-id="a6b8c-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a6b8c-142">RELATED LINKS</span></span>
