---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeBandwidthSchedule.md
ms.openlocfilehash: f3f38feff8b6d855121a6772cfb56ef0b57cebfd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118914"
---
# <span data-ttu-id="e0f3e-101">Remove-AzStackEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="e0f3e-101">Remove-AzStackEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="e0f3e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e0f3e-102">SYNOPSIS</span></span>
<span data-ttu-id="e0f3e-103">Remove um Cronograma de Largura de Banda.</span><span class="sxs-lookup"><span data-stu-id="e0f3e-103">Removes a Bandwidth Schedule.</span></span>

## <span data-ttu-id="e0f3e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e0f3e-104">SYNTAX</span></span>

### <span data-ttu-id="e0f3e-105">DeleteByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e0f3e-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0f3e-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0f3e-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeBandwidthSchedule -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0f3e-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0f3e-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0f3e-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="e0f3e-108">DESCRIPTION</span></span>
<span data-ttu-id="e0f3e-109">O cmdlet **Remove-AzSt stackEdgeBandwidthSchedule** remove o cronograma de largura de banda de um dispositivo stack edge.</span><span class="sxs-lookup"><span data-stu-id="e0f3e-109">The **Remove-AzStackEdgeBandwidthSchedule** cmdlet removes the Bandwidth schedule for a Stack Edge device.</span></span> 

## <span data-ttu-id="e0f3e-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e0f3e-110">EXAMPLES</span></span>

### <span data-ttu-id="e0f3e-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e0f3e-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule
```

## <span data-ttu-id="e0f3e-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e0f3e-112">PARAMETERS</span></span>

### <span data-ttu-id="e0f3e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e0f3e-113">-AsJob</span></span>
<span data-ttu-id="e0f3e-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e0f3e-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e0f3e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0f3e-115">-DefaultProfile</span></span>
<span data-ttu-id="e0f3e-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e0f3e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0f3e-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="e0f3e-117">-DeviceName</span></span>
<span data-ttu-id="e0f3e-118">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="e0f3e-118">Device Name</span></span>

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

### <span data-ttu-id="e0f3e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e0f3e-119">-InputObject</span></span>
<span data-ttu-id="e0f3e-120">Objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="e0f3e-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: BandwidthSchedule

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0f3e-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="e0f3e-121">-Name</span></span>
<span data-ttu-id="e0f3e-122">Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="e0f3e-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: BandwidthScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0f3e-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e0f3e-123">-PassThru</span></span>
<span data-ttu-id="e0f3e-124">retorna verdadeiro se for bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="e0f3e-124">returns true if successful</span></span>

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

### <span data-ttu-id="e0f3e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0f3e-125">-ResourceGroupName</span></span>
<span data-ttu-id="e0f3e-126">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="e0f3e-126">Resource Group Name</span></span>

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

### <span data-ttu-id="e0f3e-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e0f3e-127">-ResourceId</span></span>
<span data-ttu-id="e0f3e-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="e0f3e-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="e0f3e-129">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="e0f3e-129">-Confirm</span></span>
<span data-ttu-id="e0f3e-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0f3e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0f3e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0f3e-131">-WhatIf</span></span>
<span data-ttu-id="e0f3e-132">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="e0f3e-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e0f3e-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e0f3e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0f3e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0f3e-134">CommonParameters</span></span>
<span data-ttu-id="e0f3e-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0f3e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0f3e-136">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e0f3e-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0f3e-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="e0f3e-137">INPUTS</span></span>

### <span data-ttu-id="e0f3e-138">System.String</span><span class="sxs-lookup"><span data-stu-id="e0f3e-138">System.String</span></span>

### <span data-ttu-id="e0f3e-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSSt stackEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="e0f3e-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="e0f3e-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="e0f3e-140">OUTPUTS</span></span>

### <span data-ttu-id="e0f3e-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e0f3e-141">System.Boolean</span></span>

## <span data-ttu-id="e0f3e-142">Notas</span><span class="sxs-lookup"><span data-stu-id="e0f3e-142">NOTES</span></span>

## <span data-ttu-id="e0f3e-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e0f3e-143">RELATED LINKS</span></span>
