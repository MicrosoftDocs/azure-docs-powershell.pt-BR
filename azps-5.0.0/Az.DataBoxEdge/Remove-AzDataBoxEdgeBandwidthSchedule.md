---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: a31759c1ec1d1f3e0e3715c9faa3c0171a6e8537
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281125"
---
# <span data-ttu-id="a1e55-101">Remove-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="a1e55-101">Remove-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="a1e55-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a1e55-102">SYNOPSIS</span></span>
<span data-ttu-id="a1e55-103">Remove um cronograma de largura de banda.</span><span class="sxs-lookup"><span data-stu-id="a1e55-103">Removes a Bandwidth Schedule.</span></span>

## <span data-ttu-id="a1e55-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a1e55-104">SYNTAX</span></span>

### <span data-ttu-id="a1e55-105">DeleteByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="a1e55-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1e55-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1e55-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1e55-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1e55-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1e55-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a1e55-108">DESCRIPTION</span></span>
<span data-ttu-id="a1e55-109">O cmdlet **Remove-AzDataBoxEdgeBandwidthSchedule** remove a programação de largura de banda de um dispositivo de borda de caixa de dados.</span><span class="sxs-lookup"><span data-stu-id="a1e55-109">The **Remove-AzDataBoxEdgeBandwidthSchedule** cmdlet removes the Bandwidth schedule for a Data Box Edge device.</span></span> 

## <span data-ttu-id="a1e55-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a1e55-110">EXAMPLES</span></span>

### <span data-ttu-id="a1e55-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a1e55-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule
```

## <span data-ttu-id="a1e55-112">OS</span><span class="sxs-lookup"><span data-stu-id="a1e55-112">PARAMETERS</span></span>

### <span data-ttu-id="a1e55-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a1e55-113">-AsJob</span></span>
<span data-ttu-id="a1e55-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="a1e55-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a1e55-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1e55-115">-DefaultProfile</span></span>
<span data-ttu-id="a1e55-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a1e55-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1e55-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="a1e55-117">-DeviceName</span></span>
<span data-ttu-id="a1e55-118">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="a1e55-118">Device Name</span></span>

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

### <span data-ttu-id="a1e55-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a1e55-119">-InputObject</span></span>
<span data-ttu-id="a1e55-120">Objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="a1e55-120">Input Object</span></span>

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

### <span data-ttu-id="a1e55-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="a1e55-121">-Name</span></span>
<span data-ttu-id="a1e55-122">Nome do recurso</span><span class="sxs-lookup"><span data-stu-id="a1e55-122">Resource Name</span></span>

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

### <span data-ttu-id="a1e55-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a1e55-123">-PassThru</span></span>
<span data-ttu-id="a1e55-124">Retorna verdadeiro se bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="a1e55-124">returns true if successful</span></span>

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

### <span data-ttu-id="a1e55-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1e55-125">-ResourceGroupName</span></span>
<span data-ttu-id="a1e55-126">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="a1e55-126">Resource Group Name</span></span>

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

### <span data-ttu-id="a1e55-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1e55-127">-ResourceId</span></span>
<span data-ttu-id="a1e55-128">ResourceId do Azure</span><span class="sxs-lookup"><span data-stu-id="a1e55-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="a1e55-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a1e55-129">-Confirm</span></span>
<span data-ttu-id="a1e55-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1e55-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1e55-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1e55-131">-WhatIf</span></span>
<span data-ttu-id="a1e55-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a1e55-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a1e55-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a1e55-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1e55-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1e55-134">CommonParameters</span></span>
<span data-ttu-id="a1e55-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1e55-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1e55-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a1e55-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1e55-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a1e55-137">INPUTS</span></span>

### <span data-ttu-id="a1e55-138">System. String</span><span class="sxs-lookup"><span data-stu-id="a1e55-138">System.String</span></span>

### <span data-ttu-id="a1e55-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="a1e55-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="a1e55-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a1e55-140">OUTPUTS</span></span>

### <span data-ttu-id="a1e55-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a1e55-141">System.Boolean</span></span>

## <span data-ttu-id="a1e55-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a1e55-142">NOTES</span></span>

## <span data-ttu-id="a1e55-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a1e55-143">RELATED LINKS</span></span>
