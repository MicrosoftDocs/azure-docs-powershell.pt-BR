---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeBandwidthSchedule.md
ms.openlocfilehash: f3f38feff8b6d855121a6772cfb56ef0b57cebfd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113821"
---
# <span data-ttu-id="6bfa8-101">Remove-AzStackEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="6bfa8-101">Remove-AzStackEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="6bfa8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6bfa8-102">SYNOPSIS</span></span>
<span data-ttu-id="6bfa8-103">Remove um cronograma de largura de banda.</span><span class="sxs-lookup"><span data-stu-id="6bfa8-103">Removes a Bandwidth Schedule.</span></span>

## <span data-ttu-id="6bfa8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6bfa8-104">SYNTAX</span></span>

### <span data-ttu-id="6bfa8-105">DeleteByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="6bfa8-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bfa8-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6bfa8-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeBandwidthSchedule -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bfa8-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6bfa8-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6bfa8-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6bfa8-108">DESCRIPTION</span></span>
<span data-ttu-id="6bfa8-109">O cmdlet **Remove-AzStackEdgeBandwidthSchedule** remove a programação de largura de banda de um dispositivo de borda de pilha.</span><span class="sxs-lookup"><span data-stu-id="6bfa8-109">The **Remove-AzStackEdgeBandwidthSchedule** cmdlet removes the Bandwidth schedule for a Stack Edge device.</span></span> 

## <span data-ttu-id="6bfa8-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6bfa8-110">EXAMPLES</span></span>

### <span data-ttu-id="6bfa8-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6bfa8-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule
```

## <span data-ttu-id="6bfa8-112">OS</span><span class="sxs-lookup"><span data-stu-id="6bfa8-112">PARAMETERS</span></span>

### <span data-ttu-id="6bfa8-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6bfa8-113">-AsJob</span></span>
<span data-ttu-id="6bfa8-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="6bfa8-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6bfa8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bfa8-115">-DefaultProfile</span></span>
<span data-ttu-id="6bfa8-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6bfa8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6bfa8-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="6bfa8-117">-DeviceName</span></span>
<span data-ttu-id="6bfa8-118">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="6bfa8-118">Device Name</span></span>

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

### <span data-ttu-id="6bfa8-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6bfa8-119">-InputObject</span></span>
<span data-ttu-id="6bfa8-120">Objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="6bfa8-120">Input Object</span></span>

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

### <span data-ttu-id="6bfa8-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="6bfa8-121">-Name</span></span>
<span data-ttu-id="6bfa8-122">Nome do recurso</span><span class="sxs-lookup"><span data-stu-id="6bfa8-122">Resource Name</span></span>

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

### <span data-ttu-id="6bfa8-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6bfa8-123">-PassThru</span></span>
<span data-ttu-id="6bfa8-124">Retorna verdadeiro se bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="6bfa8-124">returns true if successful</span></span>

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

### <span data-ttu-id="6bfa8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bfa8-125">-ResourceGroupName</span></span>
<span data-ttu-id="6bfa8-126">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="6bfa8-126">Resource Group Name</span></span>

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

### <span data-ttu-id="6bfa8-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6bfa8-127">-ResourceId</span></span>
<span data-ttu-id="6bfa8-128">ResourceId do Azure</span><span class="sxs-lookup"><span data-stu-id="6bfa8-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="6bfa8-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6bfa8-129">-Confirm</span></span>
<span data-ttu-id="6bfa8-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6bfa8-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bfa8-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bfa8-131">-WhatIf</span></span>
<span data-ttu-id="6bfa8-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6bfa8-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6bfa8-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6bfa8-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bfa8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bfa8-134">CommonParameters</span></span>
<span data-ttu-id="6bfa8-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6bfa8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bfa8-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6bfa8-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bfa8-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6bfa8-137">INPUTS</span></span>

### <span data-ttu-id="6bfa8-138">System. String</span><span class="sxs-lookup"><span data-stu-id="6bfa8-138">System.String</span></span>

### <span data-ttu-id="6bfa8-139">Microsoft. Azure. PowerShell. cmdlets. StackEdge. Models. PSStackEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="6bfa8-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="6bfa8-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6bfa8-140">OUTPUTS</span></span>

### <span data-ttu-id="6bfa8-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6bfa8-141">System.Boolean</span></span>

## <span data-ttu-id="6bfa8-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6bfa8-142">NOTES</span></span>

## <span data-ttu-id="6bfa8-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6bfa8-143">RELATED LINKS</span></span>
