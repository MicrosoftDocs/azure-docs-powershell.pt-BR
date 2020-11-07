---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeBandwidthSchedule.md
ms.openlocfilehash: f3f38feff8b6d855121a6772cfb56ef0b57cebfd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940736"
---
# <span data-ttu-id="8dc52-101">Remove-AzStackEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="8dc52-101">Remove-AzStackEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="8dc52-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8dc52-102">SYNOPSIS</span></span>
<span data-ttu-id="8dc52-103">Remove um cronograma de largura de banda.</span><span class="sxs-lookup"><span data-stu-id="8dc52-103">Removes a Bandwidth Schedule.</span></span>

## <span data-ttu-id="8dc52-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8dc52-104">SYNTAX</span></span>

### <span data-ttu-id="8dc52-105">DeleteByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="8dc52-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8dc52-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8dc52-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeBandwidthSchedule -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8dc52-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8dc52-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8dc52-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8dc52-108">DESCRIPTION</span></span>
<span data-ttu-id="8dc52-109">O cmdlet **Remove-AzStackEdgeBandwidthSchedule** remove a programação de largura de banda de um dispositivo de borda de pilha.</span><span class="sxs-lookup"><span data-stu-id="8dc52-109">The **Remove-AzStackEdgeBandwidthSchedule** cmdlet removes the Bandwidth schedule for a Stack Edge device.</span></span> 

## <span data-ttu-id="8dc52-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8dc52-110">EXAMPLES</span></span>

### <span data-ttu-id="8dc52-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8dc52-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule
```

## <span data-ttu-id="8dc52-112">OS</span><span class="sxs-lookup"><span data-stu-id="8dc52-112">PARAMETERS</span></span>

### <span data-ttu-id="8dc52-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8dc52-113">-AsJob</span></span>
<span data-ttu-id="8dc52-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="8dc52-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8dc52-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dc52-115">-DefaultProfile</span></span>
<span data-ttu-id="8dc52-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8dc52-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8dc52-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="8dc52-117">-DeviceName</span></span>
<span data-ttu-id="8dc52-118">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="8dc52-118">Device Name</span></span>

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

### <span data-ttu-id="8dc52-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8dc52-119">-InputObject</span></span>
<span data-ttu-id="8dc52-120">Objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="8dc52-120">Input Object</span></span>

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

### <span data-ttu-id="8dc52-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="8dc52-121">-Name</span></span>
<span data-ttu-id="8dc52-122">Nome do recurso</span><span class="sxs-lookup"><span data-stu-id="8dc52-122">Resource Name</span></span>

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

### <span data-ttu-id="8dc52-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8dc52-123">-PassThru</span></span>
<span data-ttu-id="8dc52-124">Retorna verdadeiro se bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="8dc52-124">returns true if successful</span></span>

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

### <span data-ttu-id="8dc52-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8dc52-125">-ResourceGroupName</span></span>
<span data-ttu-id="8dc52-126">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="8dc52-126">Resource Group Name</span></span>

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

### <span data-ttu-id="8dc52-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8dc52-127">-ResourceId</span></span>
<span data-ttu-id="8dc52-128">ResourceId do Azure</span><span class="sxs-lookup"><span data-stu-id="8dc52-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="8dc52-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8dc52-129">-Confirm</span></span>
<span data-ttu-id="8dc52-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8dc52-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8dc52-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8dc52-131">-WhatIf</span></span>
<span data-ttu-id="8dc52-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8dc52-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8dc52-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8dc52-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8dc52-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dc52-134">CommonParameters</span></span>
<span data-ttu-id="8dc52-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8dc52-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dc52-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8dc52-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dc52-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8dc52-137">INPUTS</span></span>

### <span data-ttu-id="8dc52-138">System. String</span><span class="sxs-lookup"><span data-stu-id="8dc52-138">System.String</span></span>

### <span data-ttu-id="8dc52-139">Microsoft. Azure. PowerShell. cmdlets. StackEdge. Models. PSStackEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="8dc52-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="8dc52-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8dc52-140">OUTPUTS</span></span>

### <span data-ttu-id="8dc52-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8dc52-141">System.Boolean</span></span>

## <span data-ttu-id="8dc52-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8dc52-142">NOTES</span></span>

## <span data-ttu-id="8dc52-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8dc52-143">RELATED LINKS</span></span>
