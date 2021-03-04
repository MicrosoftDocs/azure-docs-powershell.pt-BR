---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/remove-azdataboxedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeOrder.md
ms.openlocfilehash: 8fe4787ca14d26b7e734a0ac081cdbaef8eddbd9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893182"
---
# <span data-ttu-id="bbdff-101">Remove-AzDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="bbdff-101">Remove-AzDataBoxEdgeOrder</span></span>

## <span data-ttu-id="bbdff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bbdff-102">SYNOPSIS</span></span>
<span data-ttu-id="bbdff-103">Remove a ordem de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bbdff-103">Removes the order for a device.</span></span>

## <span data-ttu-id="bbdff-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="bbdff-104">SYNTAX</span></span>

### <span data-ttu-id="bbdff-105">DeleteByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="bbdff-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bbdff-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bbdff-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeOrder -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bbdff-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bbdff-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeOrder -InputObject <PSDataBoxEdgeOrder> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bbdff-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="bbdff-108">DESCRIPTION</span></span>
<span data-ttu-id="bbdff-109">O cmdlet **Remove-AzDataBoxEdgeOrder** exclui uma ordem existente para um dispositivo de Borda da Caixa de Dados.</span><span class="sxs-lookup"><span data-stu-id="bbdff-109">The **Remove-AzDataBoxEdgeOrder** cmdlet deletes an existing order for a Data Box Edge device.</span></span>

## <span data-ttu-id="bbdff-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bbdff-110">EXAMPLES</span></span>

### <span data-ttu-id="bbdff-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bbdff-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
```

## <span data-ttu-id="bbdff-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="bbdff-112">PARAMETERS</span></span>

### <span data-ttu-id="bbdff-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bbdff-113">-AsJob</span></span>
<span data-ttu-id="bbdff-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="bbdff-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bbdff-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbdff-115">-DefaultProfile</span></span>
<span data-ttu-id="bbdff-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bbdff-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bbdff-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="bbdff-117">-DeviceName</span></span>
<span data-ttu-id="bbdff-118">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="bbdff-118">Device Name</span></span>

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

### <span data-ttu-id="bbdff-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bbdff-119">-InputObject</span></span>
<span data-ttu-id="bbdff-120">Objeto Input</span><span class="sxs-lookup"><span data-stu-id="bbdff-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bbdff-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bbdff-121">-PassThru</span></span>
<span data-ttu-id="bbdff-122">retorna true se bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="bbdff-122">returns true if successful</span></span>

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

### <span data-ttu-id="bbdff-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbdff-123">-ResourceGroupName</span></span>
<span data-ttu-id="bbdff-124">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="bbdff-124">Resource Group Name</span></span>

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

### <span data-ttu-id="bbdff-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bbdff-125">-ResourceId</span></span>
<span data-ttu-id="bbdff-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="bbdff-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="bbdff-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bbdff-127">-Confirm</span></span>
<span data-ttu-id="bbdff-128">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbdff-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbdff-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbdff-129">-WhatIf</span></span>
<span data-ttu-id="bbdff-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bbdff-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bbdff-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bbdff-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbdff-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbdff-132">CommonParameters</span></span>
<span data-ttu-id="bbdff-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbdff-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbdff-134">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bbdff-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbdff-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bbdff-135">INPUTS</span></span>

### <span data-ttu-id="bbdff-136">System.String</span><span class="sxs-lookup"><span data-stu-id="bbdff-136">System.String</span></span>

### <span data-ttu-id="bbdff-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="bbdff-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="bbdff-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="bbdff-138">OUTPUTS</span></span>

### <span data-ttu-id="bbdff-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="bbdff-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="bbdff-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="bbdff-140">NOTES</span></span>

## <span data-ttu-id="bbdff-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bbdff-141">RELATED LINKS</span></span>
