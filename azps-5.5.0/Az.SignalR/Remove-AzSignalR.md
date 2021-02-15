---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/remove-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Remove-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Remove-AzSignalR.md
ms.openlocfilehash: 89df3c19b34ee7175e6fe65269f8df5f218a49f3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112570"
---
# <span data-ttu-id="8f4de-101">Remove-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="8f4de-101">Remove-AzSignalR</span></span>

## <span data-ttu-id="8f4de-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8f4de-102">SYNOPSIS</span></span>
<span data-ttu-id="8f4de-103">Remover um serviço de Sinalização.</span><span class="sxs-lookup"><span data-stu-id="8f4de-103">Remove a SignalR service.</span></span>

## <span data-ttu-id="8f4de-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8f4de-104">SYNTAX</span></span>

### <span data-ttu-id="8f4de-105">ResourceGroupParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8f4de-105">ResourceGroupParameterSet (Default)</span></span>
```
Remove-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f4de-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f4de-106">ResourceIdParameterSet</span></span>
```
Remove-AzSignalR -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f4de-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f4de-107">InputObjectParameterSet</span></span>
```
Remove-AzSignalR -InputObject <PSSignalRResource> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f4de-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="8f4de-108">DESCRIPTION</span></span>
<span data-ttu-id="8f4de-109">Remover um serviço de Sinalização.</span><span class="sxs-lookup"><span data-stu-id="8f4de-109">Remove a SignalR service.</span></span>

## <span data-ttu-id="8f4de-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8f4de-110">EXAMPLES</span></span>

### <span data-ttu-id="8f4de-111">Remover um serviço de Sinalização</span><span class="sxs-lookup"><span data-stu-id="8f4de-111">Remove a SignalR service</span></span>
```
PS C:\> Remove-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -PassThru

True
```

### <span data-ttu-id="8f4de-112">Remover todos os serviços de Sinalização do cano</span><span class="sxs-lookup"><span data-stu-id="8f4de-112">Remove all SignalR service from pipe</span></span>
```
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup | Remove-AzSignalR
```

## <span data-ttu-id="8f4de-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8f4de-113">PARAMETERS</span></span>

### <span data-ttu-id="8f4de-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8f4de-114">-AsJob</span></span>
<span data-ttu-id="8f4de-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="8f4de-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8f4de-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f4de-116">-DefaultProfile</span></span>
<span data-ttu-id="8f4de-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8f4de-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f4de-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8f4de-118">-InputObject</span></span>
<span data-ttu-id="8f4de-119">O objeto de recurso signalr.</span><span class="sxs-lookup"><span data-stu-id="8f4de-119">The SignalR resource object.</span></span>

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

### <span data-ttu-id="8f4de-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="8f4de-120">-Name</span></span>
<span data-ttu-id="8f4de-121">Nome do serviço de Sinalização.</span><span class="sxs-lookup"><span data-stu-id="8f4de-121">SignalR service name.</span></span>

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

### <span data-ttu-id="8f4de-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8f4de-122">-PassThru</span></span>
<span data-ttu-id="8f4de-123">Retorna verdadeiro se a remoção foi concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="8f4de-123">Returns true if the removal was completed successfully.</span></span>

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

### <span data-ttu-id="8f4de-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f4de-124">-ResourceGroupName</span></span>
<span data-ttu-id="8f4de-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8f4de-125">Resource group name.</span></span>

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

### <span data-ttu-id="8f4de-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8f4de-126">-ResourceId</span></span>
<span data-ttu-id="8f4de-127">A ID do recurso de serviço de Sinalização.</span><span class="sxs-lookup"><span data-stu-id="8f4de-127">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="8f4de-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="8f4de-128">-Confirm</span></span>
<span data-ttu-id="8f4de-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f4de-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f4de-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f4de-130">-WhatIf</span></span>
<span data-ttu-id="8f4de-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="8f4de-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f4de-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8f4de-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f4de-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f4de-133">CommonParameters</span></span>
<span data-ttu-id="8f4de-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f4de-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f4de-135">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8f4de-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f4de-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="8f4de-136">INPUTS</span></span>

### <span data-ttu-id="8f4de-137">System.String</span><span class="sxs-lookup"><span data-stu-id="8f4de-137">System.String</span></span>
### <span data-ttu-id="8f4de-138">Microsoft.Azure.Commands.Signalr.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="8f4de-138">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="8f4de-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="8f4de-139">OUTPUTS</span></span>

### <span data-ttu-id="8f4de-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8f4de-140">System.Boolean</span></span>
## <span data-ttu-id="8f4de-141">Notas</span><span class="sxs-lookup"><span data-stu-id="8f4de-141">NOTES</span></span>

## <span data-ttu-id="8f4de-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8f4de-142">RELATED LINKS</span></span>
