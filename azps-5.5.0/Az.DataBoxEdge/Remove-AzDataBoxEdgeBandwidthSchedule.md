---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: a31759c1ec1d1f3e0e3715c9faa3c0171a6e8537
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111987"
---
# <span data-ttu-id="e87f9-101">Remove-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="e87f9-101">Remove-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="e87f9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e87f9-102">SYNOPSIS</span></span>
<span data-ttu-id="e87f9-103">Remove um Cronograma de Largura de Banda.</span><span class="sxs-lookup"><span data-stu-id="e87f9-103">Removes a Bandwidth Schedule.</span></span>

## <span data-ttu-id="e87f9-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e87f9-104">SYNTAX</span></span>

### <span data-ttu-id="e87f9-105">DeleteByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e87f9-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e87f9-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e87f9-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e87f9-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e87f9-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e87f9-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="e87f9-108">DESCRIPTION</span></span>
<span data-ttu-id="e87f9-109">O cmdlet **Remove-AzDataBoxEdgeBandwidthSchedule** remove o cronograma de largura de banda de um dispositivo de borda de caixa de dados.</span><span class="sxs-lookup"><span data-stu-id="e87f9-109">The **Remove-AzDataBoxEdgeBandwidthSchedule** cmdlet removes the Bandwidth schedule for a Data Box Edge device.</span></span> 

## <span data-ttu-id="e87f9-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e87f9-110">EXAMPLES</span></span>

### <span data-ttu-id="e87f9-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e87f9-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule
```

## <span data-ttu-id="e87f9-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e87f9-112">PARAMETERS</span></span>

### <span data-ttu-id="e87f9-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e87f9-113">-AsJob</span></span>
<span data-ttu-id="e87f9-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e87f9-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e87f9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e87f9-115">-DefaultProfile</span></span>
<span data-ttu-id="e87f9-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e87f9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e87f9-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="e87f9-117">-DeviceName</span></span>
<span data-ttu-id="e87f9-118">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="e87f9-118">Device Name</span></span>

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

### <span data-ttu-id="e87f9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e87f9-119">-InputObject</span></span>
<span data-ttu-id="e87f9-120">Objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="e87f9-120">Input Object</span></span>

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

### <span data-ttu-id="e87f9-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="e87f9-121">-Name</span></span>
<span data-ttu-id="e87f9-122">Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="e87f9-122">Resource Name</span></span>

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

### <span data-ttu-id="e87f9-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e87f9-123">-PassThru</span></span>
<span data-ttu-id="e87f9-124">retorna verdadeiro se for bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="e87f9-124">returns true if successful</span></span>

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

### <span data-ttu-id="e87f9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e87f9-125">-ResourceGroupName</span></span>
<span data-ttu-id="e87f9-126">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="e87f9-126">Resource Group Name</span></span>

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

### <span data-ttu-id="e87f9-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e87f9-127">-ResourceId</span></span>
<span data-ttu-id="e87f9-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="e87f9-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="e87f9-129">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="e87f9-129">-Confirm</span></span>
<span data-ttu-id="e87f9-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e87f9-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e87f9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e87f9-131">-WhatIf</span></span>
<span data-ttu-id="e87f9-132">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="e87f9-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e87f9-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e87f9-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e87f9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e87f9-134">CommonParameters</span></span>
<span data-ttu-id="e87f9-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e87f9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e87f9-136">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e87f9-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e87f9-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="e87f9-137">INPUTS</span></span>

### <span data-ttu-id="e87f9-138">System.String</span><span class="sxs-lookup"><span data-stu-id="e87f9-138">System.String</span></span>

### <span data-ttu-id="e87f9-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="e87f9-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="e87f9-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="e87f9-140">OUTPUTS</span></span>

### <span data-ttu-id="e87f9-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e87f9-141">System.Boolean</span></span>

## <span data-ttu-id="e87f9-142">Notas</span><span class="sxs-lookup"><span data-stu-id="e87f9-142">NOTES</span></span>

## <span data-ttu-id="e87f9-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e87f9-143">RELATED LINKS</span></span>
