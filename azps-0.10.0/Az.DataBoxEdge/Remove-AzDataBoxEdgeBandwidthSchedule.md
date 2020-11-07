---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: 91be880f5e667287c1a9e62e2a003eb306ae1f5c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776748"
---
# <span data-ttu-id="eadcd-101">Remove-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="eadcd-101">Remove-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="eadcd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="eadcd-102">SYNOPSIS</span></span>
<span data-ttu-id="eadcd-103">Remove um cronograma de largura de banda.</span><span class="sxs-lookup"><span data-stu-id="eadcd-103">Removes a Bandwidth Schedule.</span></span>

## <span data-ttu-id="eadcd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eadcd-104">SYNTAX</span></span>

### <span data-ttu-id="eadcd-105">DeleteByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="eadcd-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eadcd-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eadcd-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eadcd-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eadcd-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eadcd-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="eadcd-108">DESCRIPTION</span></span>
<span data-ttu-id="eadcd-109">O cmdlet **Remove-AzDataBoxEdgeBandwidthSchedule** remove a programação de largura de banda de um dispositivo de borda de caixa de dados.</span><span class="sxs-lookup"><span data-stu-id="eadcd-109">The **Remove-AzDataBoxEdgeBandwidthSchedule** cmdlet removes the Bandwidth schedule for a Data Box Edge device.</span></span> 

## <span data-ttu-id="eadcd-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="eadcd-110">EXAMPLES</span></span>

### <span data-ttu-id="eadcd-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="eadcd-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule
```

## <span data-ttu-id="eadcd-112">OS</span><span class="sxs-lookup"><span data-stu-id="eadcd-112">PARAMETERS</span></span>

### <span data-ttu-id="eadcd-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eadcd-113">-AsJob</span></span>
<span data-ttu-id="eadcd-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="eadcd-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eadcd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eadcd-115">-DefaultProfile</span></span>
<span data-ttu-id="eadcd-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="eadcd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eadcd-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="eadcd-117">-DeviceName</span></span>
<span data-ttu-id="eadcd-118">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="eadcd-118">Device Name</span></span>

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

### <span data-ttu-id="eadcd-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eadcd-119">-InputObject</span></span>
<span data-ttu-id="eadcd-120">Objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="eadcd-120">Input Object</span></span>

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

### <span data-ttu-id="eadcd-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="eadcd-121">-Name</span></span>
<span data-ttu-id="eadcd-122">Nome do recurso</span><span class="sxs-lookup"><span data-stu-id="eadcd-122">Resource Name</span></span>

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

### <span data-ttu-id="eadcd-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eadcd-123">-PassThru</span></span>
<span data-ttu-id="eadcd-124">Retorna verdadeiro se bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="eadcd-124">returns true if successful</span></span>

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

### <span data-ttu-id="eadcd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eadcd-125">-ResourceGroupName</span></span>
<span data-ttu-id="eadcd-126">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="eadcd-126">Resource Group Name</span></span>

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

### <span data-ttu-id="eadcd-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eadcd-127">-ResourceId</span></span>
<span data-ttu-id="eadcd-128">ResourceId do Azure</span><span class="sxs-lookup"><span data-stu-id="eadcd-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="eadcd-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="eadcd-129">-Confirm</span></span>
<span data-ttu-id="eadcd-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eadcd-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eadcd-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eadcd-131">-WhatIf</span></span>
<span data-ttu-id="eadcd-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="eadcd-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eadcd-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="eadcd-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eadcd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eadcd-134">CommonParameters</span></span>
<span data-ttu-id="eadcd-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eadcd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eadcd-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eadcd-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eadcd-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="eadcd-137">INPUTS</span></span>

### <span data-ttu-id="eadcd-138">System. String</span><span class="sxs-lookup"><span data-stu-id="eadcd-138">System.String</span></span>

### <span data-ttu-id="eadcd-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="eadcd-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="eadcd-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="eadcd-140">OUTPUTS</span></span>

### <span data-ttu-id="eadcd-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="eadcd-141">System.Boolean</span></span>

## <span data-ttu-id="eadcd-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="eadcd-142">NOTES</span></span>

## <span data-ttu-id="eadcd-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eadcd-143">RELATED LINKS</span></span>
