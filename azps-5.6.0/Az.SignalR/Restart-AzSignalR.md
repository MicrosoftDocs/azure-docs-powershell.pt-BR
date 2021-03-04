---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/powershell/module/az.signalr/restart-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Restart-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Restart-AzSignalR.md
ms.openlocfilehash: c98b716f37fcf9aafafacdefad4c51b0451cf12d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885818"
---
# <span data-ttu-id="770c1-101">Restart-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="770c1-101">Restart-AzSignalR</span></span>

## <span data-ttu-id="770c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="770c1-102">SYNOPSIS</span></span>
<span data-ttu-id="770c1-103">Reinicie um serviço SignalR.</span><span class="sxs-lookup"><span data-stu-id="770c1-103">Restart a SignalR service.</span></span>

## <span data-ttu-id="770c1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="770c1-104">SYNTAX</span></span>

### <span data-ttu-id="770c1-105">ResourceGroupParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="770c1-105">ResourceGroupParameterSet (Default)</span></span>
```
Restart-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="770c1-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="770c1-106">ResourceIdParameterSet</span></span>
```
Restart-AzSignalR -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="770c1-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="770c1-107">InputObjectParameterSet</span></span>
```
Restart-AzSignalR -InputObject <PSSignalRResource> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="770c1-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="770c1-108">DESCRIPTION</span></span>
<span data-ttu-id="770c1-109">Reinicie um serviço SignalR.</span><span class="sxs-lookup"><span data-stu-id="770c1-109">Restart a SignalR service.</span></span>

## <span data-ttu-id="770c1-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="770c1-110">EXAMPLES</span></span>

### <span data-ttu-id="770c1-111">Reiniciar um serviço SignalR específico</span><span class="sxs-lookup"><span data-stu-id="770c1-111">Restart a specific SignalR service</span></span>
```powershell
PS C:\> Restart-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -PassThru

True
```

<span data-ttu-id="770c1-112">O grupo de recursos padrão pode ser definido por \` Set-AzDefault -ResourceGroupName myResourceGroup \` .</span><span class="sxs-lookup"><span data-stu-id="770c1-112">The default resource group can be set by \`Set-AzDefault -ResourceGroupName myResourceGroup\`.</span></span>

## <span data-ttu-id="770c1-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="770c1-113">PARAMETERS</span></span>

### <span data-ttu-id="770c1-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="770c1-114">-AsJob</span></span>
<span data-ttu-id="770c1-115">Execute o cmdlet em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="770c1-115">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="770c1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="770c1-116">-DefaultProfile</span></span>
<span data-ttu-id="770c1-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="770c1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="770c1-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="770c1-118">-InputObject</span></span>
<span data-ttu-id="770c1-119">O objeto de recurso SignalR.</span><span class="sxs-lookup"><span data-stu-id="770c1-119">The SignalR resource object.</span></span>

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

### <span data-ttu-id="770c1-120">-Name</span><span class="sxs-lookup"><span data-stu-id="770c1-120">-Name</span></span>
<span data-ttu-id="770c1-121">O nome do serviço SignalR.</span><span class="sxs-lookup"><span data-stu-id="770c1-121">The SignalR service name.</span></span>

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

### <span data-ttu-id="770c1-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="770c1-122">-PassThru</span></span>
<span data-ttu-id="770c1-123">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="770c1-123">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="770c1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="770c1-124">-ResourceGroupName</span></span>
<span data-ttu-id="770c1-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="770c1-125">The resource group name.</span></span>
<span data-ttu-id="770c1-126">O padrão será usado se não for especificado.</span><span class="sxs-lookup"><span data-stu-id="770c1-126">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="770c1-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="770c1-127">-ResourceId</span></span>
<span data-ttu-id="770c1-128">A ID do recurso de serviço SignalR.</span><span class="sxs-lookup"><span data-stu-id="770c1-128">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="770c1-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="770c1-129">-Confirm</span></span>
<span data-ttu-id="770c1-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="770c1-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="770c1-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="770c1-131">-WhatIf</span></span>
<span data-ttu-id="770c1-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="770c1-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="770c1-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="770c1-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="770c1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="770c1-134">CommonParameters</span></span>
<span data-ttu-id="770c1-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="770c1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="770c1-136">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="770c1-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="770c1-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="770c1-137">INPUTS</span></span>

### <span data-ttu-id="770c1-138">System.String</span><span class="sxs-lookup"><span data-stu-id="770c1-138">System.String</span></span>

### <span data-ttu-id="770c1-139">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="770c1-139">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="770c1-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="770c1-140">OUTPUTS</span></span>

### <span data-ttu-id="770c1-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="770c1-141">System.Boolean</span></span>

## <span data-ttu-id="770c1-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="770c1-142">NOTES</span></span>

## <span data-ttu-id="770c1-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="770c1-143">RELATED LINKS</span></span>
