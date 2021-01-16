---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: a31759c1ec1d1f3e0e3715c9faa3c0171a6e8537
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261886"
---
# <span data-ttu-id="b37dc-101">Remove-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="b37dc-101">Remove-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="b37dc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b37dc-102">SYNOPSIS</span></span>
<span data-ttu-id="b37dc-103">Remove um cronograma de largura de banda.</span><span class="sxs-lookup"><span data-stu-id="b37dc-103">Removes a Bandwidth Schedule.</span></span>

## <span data-ttu-id="b37dc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b37dc-104">SYNTAX</span></span>

### <span data-ttu-id="b37dc-105">DeleteByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="b37dc-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b37dc-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b37dc-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b37dc-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b37dc-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b37dc-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b37dc-108">DESCRIPTION</span></span>
<span data-ttu-id="b37dc-109">O cmdlet **Remove-AzDataBoxEdgeBandwidthSchedule** remove a programação de largura de banda de um dispositivo de borda de caixa de dados.</span><span class="sxs-lookup"><span data-stu-id="b37dc-109">The **Remove-AzDataBoxEdgeBandwidthSchedule** cmdlet removes the Bandwidth schedule for a Data Box Edge device.</span></span> 

## <span data-ttu-id="b37dc-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b37dc-110">EXAMPLES</span></span>

### <span data-ttu-id="b37dc-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b37dc-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule
```

## <span data-ttu-id="b37dc-112">OS</span><span class="sxs-lookup"><span data-stu-id="b37dc-112">PARAMETERS</span></span>

### <span data-ttu-id="b37dc-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b37dc-113">-AsJob</span></span>
<span data-ttu-id="b37dc-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="b37dc-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b37dc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b37dc-115">-DefaultProfile</span></span>
<span data-ttu-id="b37dc-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b37dc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b37dc-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="b37dc-117">-DeviceName</span></span>
<span data-ttu-id="b37dc-118">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="b37dc-118">Device Name</span></span>

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

### <span data-ttu-id="b37dc-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b37dc-119">-InputObject</span></span>
<span data-ttu-id="b37dc-120">Objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="b37dc-120">Input Object</span></span>

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

### <span data-ttu-id="b37dc-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="b37dc-121">-Name</span></span>
<span data-ttu-id="b37dc-122">Nome do recurso</span><span class="sxs-lookup"><span data-stu-id="b37dc-122">Resource Name</span></span>

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

### <span data-ttu-id="b37dc-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b37dc-123">-PassThru</span></span>
<span data-ttu-id="b37dc-124">Retorna verdadeiro se bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="b37dc-124">returns true if successful</span></span>

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

### <span data-ttu-id="b37dc-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b37dc-125">-ResourceGroupName</span></span>
<span data-ttu-id="b37dc-126">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="b37dc-126">Resource Group Name</span></span>

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

### <span data-ttu-id="b37dc-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b37dc-127">-ResourceId</span></span>
<span data-ttu-id="b37dc-128">ResourceId do Azure</span><span class="sxs-lookup"><span data-stu-id="b37dc-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="b37dc-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b37dc-129">-Confirm</span></span>
<span data-ttu-id="b37dc-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b37dc-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b37dc-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b37dc-131">-WhatIf</span></span>
<span data-ttu-id="b37dc-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b37dc-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b37dc-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b37dc-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b37dc-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b37dc-134">CommonParameters</span></span>
<span data-ttu-id="b37dc-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b37dc-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b37dc-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b37dc-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b37dc-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b37dc-137">INPUTS</span></span>

### <span data-ttu-id="b37dc-138">System. String</span><span class="sxs-lookup"><span data-stu-id="b37dc-138">System.String</span></span>

### <span data-ttu-id="b37dc-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="b37dc-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="b37dc-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b37dc-140">OUTPUTS</span></span>

### <span data-ttu-id="b37dc-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b37dc-141">System.Boolean</span></span>

## <span data-ttu-id="b37dc-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b37dc-142">NOTES</span></span>

## <span data-ttu-id="b37dc-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b37dc-143">RELATED LINKS</span></span>
