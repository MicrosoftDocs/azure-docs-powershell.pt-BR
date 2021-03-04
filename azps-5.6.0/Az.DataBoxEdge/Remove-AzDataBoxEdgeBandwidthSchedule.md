---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/remove-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: 6b30f79f7ef1e2819004c8ac7e9d3b6737bfb7d6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892524"
---
# <span data-ttu-id="b4ce2-101">Remove-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="b4ce2-101">Remove-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="b4ce2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4ce2-102">SYNOPSIS</span></span>
<span data-ttu-id="b4ce2-103">Remove um Cronograma de Largura de Banda.</span><span class="sxs-lookup"><span data-stu-id="b4ce2-103">Removes a Bandwidth Schedule.</span></span>

## <span data-ttu-id="b4ce2-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b4ce2-104">SYNTAX</span></span>

### <span data-ttu-id="b4ce2-105">DeleteByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b4ce2-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4ce2-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4ce2-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4ce2-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4ce2-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4ce2-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b4ce2-108">DESCRIPTION</span></span>
<span data-ttu-id="b4ce2-109">O cmdlet **Remove-AzDataBoxEdgeBandwidthSchedule** remove a agenda de largura de banda de um dispositivo de Borda da Caixa de Dados.</span><span class="sxs-lookup"><span data-stu-id="b4ce2-109">The **Remove-AzDataBoxEdgeBandwidthSchedule** cmdlet removes the Bandwidth schedule for a Data Box Edge device.</span></span> 

## <span data-ttu-id="b4ce2-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b4ce2-110">EXAMPLES</span></span>

### <span data-ttu-id="b4ce2-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b4ce2-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule
```

## <span data-ttu-id="b4ce2-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b4ce2-112">PARAMETERS</span></span>

### <span data-ttu-id="b4ce2-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b4ce2-113">-AsJob</span></span>
<span data-ttu-id="b4ce2-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="b4ce2-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b4ce2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4ce2-115">-DefaultProfile</span></span>
<span data-ttu-id="b4ce2-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b4ce2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4ce2-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="b4ce2-117">-DeviceName</span></span>
<span data-ttu-id="b4ce2-118">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="b4ce2-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4ce2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4ce2-119">-InputObject</span></span>
<span data-ttu-id="b4ce2-120">Objeto Input</span><span class="sxs-lookup"><span data-stu-id="b4ce2-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4ce2-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b4ce2-121">-Name</span></span>
<span data-ttu-id="b4ce2-122">Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="b4ce2-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4ce2-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b4ce2-123">-PassThru</span></span>
<span data-ttu-id="b4ce2-124">retorna true se bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="b4ce2-124">returns true if successful</span></span>

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

### <span data-ttu-id="b4ce2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4ce2-125">-ResourceGroupName</span></span>
<span data-ttu-id="b4ce2-126">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="b4ce2-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4ce2-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4ce2-127">-ResourceId</span></span>
<span data-ttu-id="b4ce2-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4ce2-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="b4ce2-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b4ce2-129">-Confirm</span></span>
<span data-ttu-id="b4ce2-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4ce2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4ce2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4ce2-131">-WhatIf</span></span>
<span data-ttu-id="b4ce2-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b4ce2-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b4ce2-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b4ce2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4ce2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4ce2-134">CommonParameters</span></span>
<span data-ttu-id="b4ce2-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4ce2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4ce2-136">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b4ce2-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4ce2-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b4ce2-137">INPUTS</span></span>

### <span data-ttu-id="b4ce2-138">System.String</span><span class="sxs-lookup"><span data-stu-id="b4ce2-138">System.String</span></span>

### <span data-ttu-id="b4ce2-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="b4ce2-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="b4ce2-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b4ce2-140">OUTPUTS</span></span>

### <span data-ttu-id="b4ce2-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b4ce2-141">System.Boolean</span></span>

## <span data-ttu-id="b4ce2-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="b4ce2-142">NOTES</span></span>

## <span data-ttu-id="b4ce2-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b4ce2-143">RELATED LINKS</span></span>
