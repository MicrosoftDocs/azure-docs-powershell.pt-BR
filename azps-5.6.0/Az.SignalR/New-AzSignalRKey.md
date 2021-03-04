---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/powershell/module/az.signalr/new-azsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalRKey.md
ms.openlocfilehash: a17f8e6457cc62799fdef3d3606e04962774fdac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885820"
---
# <span data-ttu-id="477c2-101">New-AzSignalRKey</span><span class="sxs-lookup"><span data-stu-id="477c2-101">New-AzSignalRKey</span></span>

## <span data-ttu-id="477c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="477c2-102">SYNOPSIS</span></span>
<span data-ttu-id="477c2-103">Regenerar uma chave de acesso para um serviço SignalR.</span><span class="sxs-lookup"><span data-stu-id="477c2-103">Regenerate an access key for a SignalR service.</span></span>

## <span data-ttu-id="477c2-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="477c2-104">SYNTAX</span></span>

### <span data-ttu-id="477c2-105">ResourceGroupParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="477c2-105">ResourceGroupParameterSet (Default)</span></span>
```
New-AzSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="477c2-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="477c2-106">ResourceIdParameterSet</span></span>
```
New-AzSignalRKey -ResourceId <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="477c2-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="477c2-107">InputObjectParameterSet</span></span>
```
New-AzSignalRKey -InputObject <PSSignalRResource> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="477c2-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="477c2-108">DESCRIPTION</span></span>
<span data-ttu-id="477c2-109">Regenerar uma chave de acesso para um serviço SignalR.</span><span class="sxs-lookup"><span data-stu-id="477c2-109">Regenerate an access key for a SignalR service.</span></span>

## <span data-ttu-id="477c2-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="477c2-110">EXAMPLES</span></span>

### <span data-ttu-id="477c2-111">Regenerar a chave primária</span><span class="sxs-lookup"><span data-stu-id="477c2-111">Regenerate the primary key</span></span>
```powershell
PS C:\> New-AzSignalRKey -ResourceGroupName myResourceGroup -Name mysignalr1 -KeyType Primary -PassThru

True
```

## <span data-ttu-id="477c2-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="477c2-112">PARAMETERS</span></span>

### <span data-ttu-id="477c2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="477c2-113">-DefaultProfile</span></span>
<span data-ttu-id="477c2-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="477c2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="477c2-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="477c2-115">-InputObject</span></span>
<span data-ttu-id="477c2-116">O objeto de recurso SignalR.</span><span class="sxs-lookup"><span data-stu-id="477c2-116">The SignalR resource object.</span></span>

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

### <span data-ttu-id="477c2-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="477c2-117">-KeyType</span></span>
<span data-ttu-id="477c2-118">O tipo de chave, primário ou secundário.</span><span class="sxs-lookup"><span data-stu-id="477c2-118">The key type, either Primary or Secondary.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="477c2-119">-Name</span><span class="sxs-lookup"><span data-stu-id="477c2-119">-Name</span></span>
<span data-ttu-id="477c2-120">Nome do serviço signalr.</span><span class="sxs-lookup"><span data-stu-id="477c2-120">SignalR service name.</span></span>

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

### <span data-ttu-id="477c2-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="477c2-121">-PassThru</span></span>
<span data-ttu-id="477c2-122">Retorna true se a regeneração foi concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="477c2-122">Returns true if the regeneration was completed successfully.</span></span>

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

### <span data-ttu-id="477c2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="477c2-123">-ResourceGroupName</span></span>
<span data-ttu-id="477c2-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="477c2-124">Resource group name.</span></span>

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

### <span data-ttu-id="477c2-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="477c2-125">-ResourceId</span></span>
<span data-ttu-id="477c2-126">A ID do recurso de serviço SignalR.</span><span class="sxs-lookup"><span data-stu-id="477c2-126">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="477c2-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="477c2-127">-Confirm</span></span>
<span data-ttu-id="477c2-128">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="477c2-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="477c2-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="477c2-129">-WhatIf</span></span>
<span data-ttu-id="477c2-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="477c2-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="477c2-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="477c2-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="477c2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="477c2-132">CommonParameters</span></span>
<span data-ttu-id="477c2-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="477c2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="477c2-134">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="477c2-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="477c2-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="477c2-135">INPUTS</span></span>

### <span data-ttu-id="477c2-136">System.String</span><span class="sxs-lookup"><span data-stu-id="477c2-136">System.String</span></span>
### <span data-ttu-id="477c2-137">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="477c2-137">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="477c2-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="477c2-138">OUTPUTS</span></span>

### <span data-ttu-id="477c2-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="477c2-139">System.Boolean</span></span>
## <span data-ttu-id="477c2-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="477c2-140">NOTES</span></span>

## <span data-ttu-id="477c2-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="477c2-141">RELATED LINKS</span></span>
