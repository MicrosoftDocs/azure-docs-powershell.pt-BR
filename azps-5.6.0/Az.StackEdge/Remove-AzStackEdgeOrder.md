---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/remove-azstackedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeOrder.md
ms.openlocfilehash: 716beafc05c4746d0cfe76dce70109226b1f8f26
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892297"
---
# <span data-ttu-id="ed8c6-101">Remove-AzStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="ed8c6-101">Remove-AzStackEdgeOrder</span></span>

## <span data-ttu-id="ed8c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed8c6-102">SYNOPSIS</span></span>
<span data-ttu-id="ed8c6-103">Remove a ordem de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ed8c6-103">Removes the order for a device.</span></span>

## <span data-ttu-id="ed8c6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ed8c6-104">SYNTAX</span></span>

### <span data-ttu-id="ed8c6-105">DeleteByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ed8c6-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed8c6-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed8c6-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeOrder -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed8c6-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed8c6-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeOrder -InputObject <PSStackEdgeOrder> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed8c6-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ed8c6-108">DESCRIPTION</span></span>
<span data-ttu-id="ed8c6-109">O cmdlet **Remove-AzStackEdgeOrder** exclui uma ordem existente para um dispositivo de Borda de Pilha.</span><span class="sxs-lookup"><span data-stu-id="ed8c6-109">The **Remove-AzStackEdgeOrder** cmdlet deletes an existing order for a Stack Edge device.</span></span>

## <span data-ttu-id="ed8c6-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ed8c6-110">EXAMPLES</span></span>

### <span data-ttu-id="ed8c6-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ed8c6-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
```

## <span data-ttu-id="ed8c6-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ed8c6-112">PARAMETERS</span></span>

### <span data-ttu-id="ed8c6-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ed8c6-113">-AsJob</span></span>
<span data-ttu-id="ed8c6-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="ed8c6-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ed8c6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed8c6-115">-DefaultProfile</span></span>
<span data-ttu-id="ed8c6-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ed8c6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed8c6-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="ed8c6-117">-DeviceName</span></span>
<span data-ttu-id="ed8c6-118">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="ed8c6-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed8c6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed8c6-119">-InputObject</span></span>
<span data-ttu-id="ed8c6-120">Objeto Input</span><span class="sxs-lookup"><span data-stu-id="ed8c6-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed8c6-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ed8c6-121">-PassThru</span></span>
<span data-ttu-id="ed8c6-122">retorna true se bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="ed8c6-122">returns true if successful</span></span>

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

### <span data-ttu-id="ed8c6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed8c6-123">-ResourceGroupName</span></span>
<span data-ttu-id="ed8c6-124">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="ed8c6-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed8c6-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed8c6-125">-ResourceId</span></span>
<span data-ttu-id="ed8c6-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed8c6-126">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed8c6-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ed8c6-127">-Confirm</span></span>
<span data-ttu-id="ed8c6-128">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed8c6-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed8c6-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed8c6-129">-WhatIf</span></span>
<span data-ttu-id="ed8c6-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ed8c6-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ed8c6-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ed8c6-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed8c6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed8c6-132">CommonParameters</span></span>
<span data-ttu-id="ed8c6-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed8c6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed8c6-134">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ed8c6-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed8c6-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ed8c6-135">INPUTS</span></span>

### <span data-ttu-id="ed8c6-136">System.String</span><span class="sxs-lookup"><span data-stu-id="ed8c6-136">System.String</span></span>

### <span data-ttu-id="ed8c6-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="ed8c6-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="ed8c6-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ed8c6-138">OUTPUTS</span></span>

### <span data-ttu-id="ed8c6-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="ed8c6-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="ed8c6-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="ed8c6-140">NOTES</span></span>

## <span data-ttu-id="ed8c6-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ed8c6-141">RELATED LINKS</span></span>
