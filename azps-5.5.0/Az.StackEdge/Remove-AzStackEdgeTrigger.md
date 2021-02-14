---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeTrigger.md
ms.openlocfilehash: ad2761e4e0fba3ef7dbb7a28b15477a649891042
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110887"
---
# <span data-ttu-id="e920b-101">Remove-AzStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="e920b-101">Remove-AzStackEdgeTrigger</span></span>

## <span data-ttu-id="e920b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e920b-102">SYNOPSIS</span></span>
<span data-ttu-id="e920b-103">Remove um gatilho existente no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e920b-103">Removes an existing trigger on the device.</span></span>

## <span data-ttu-id="e920b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e920b-104">SYNTAX</span></span>

### <span data-ttu-id="e920b-105">DeleteByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e920b-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e920b-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e920b-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeTrigger [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e920b-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e920b-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeTrigger [-InputObject] <PSStackEdgeTrigger> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e920b-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="e920b-108">DESCRIPTION</span></span>
<span data-ttu-id="e920b-109">O cmdlet **Remove-AzSt stackEdgeTri stack** remove um gatilho existente no dispositivo Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="e920b-109">The **Remove-AzStackEdgeTrigger** cmdlet removes an existing trigger on the Stack Edge device.</span></span>

## <span data-ttu-id="e920b-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e920b-110">EXAMPLES</span></span>

### <span data-ttu-id="e920b-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e920b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName -Name triggerName
```

## <span data-ttu-id="e920b-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e920b-112">PARAMETERS</span></span>

### <span data-ttu-id="e920b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e920b-113">-AsJob</span></span>
<span data-ttu-id="e920b-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e920b-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e920b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e920b-115">-DefaultProfile</span></span>
<span data-ttu-id="e920b-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e920b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e920b-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="e920b-117">-DeviceName</span></span>
<span data-ttu-id="e920b-118">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="e920b-118">Device Name</span></span>

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

### <span data-ttu-id="e920b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e920b-119">-InputObject</span></span>
<span data-ttu-id="e920b-120">Objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="e920b-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: Trigger

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e920b-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="e920b-121">-Name</span></span>
<span data-ttu-id="e920b-122">Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="e920b-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e920b-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e920b-123">-PassThru</span></span>
<span data-ttu-id="e920b-124">retorna verdadeiro se for bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="e920b-124">returns true if successful</span></span>

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

### <span data-ttu-id="e920b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e920b-125">-ResourceGroupName</span></span>
<span data-ttu-id="e920b-126">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="e920b-126">Resource Group Name</span></span>

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

### <span data-ttu-id="e920b-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e920b-127">-ResourceId</span></span>
<span data-ttu-id="e920b-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="e920b-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e920b-129">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="e920b-129">-Confirm</span></span>
<span data-ttu-id="e920b-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e920b-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e920b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e920b-131">-WhatIf</span></span>
<span data-ttu-id="e920b-132">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="e920b-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e920b-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e920b-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e920b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e920b-134">CommonParameters</span></span>
<span data-ttu-id="e920b-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e920b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e920b-136">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e920b-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e920b-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="e920b-137">INPUTS</span></span>

### <span data-ttu-id="e920b-138">System.String</span><span class="sxs-lookup"><span data-stu-id="e920b-138">System.String</span></span>

### <span data-ttu-id="e920b-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSSt stackEdgeTri meteor</span><span class="sxs-lookup"><span data-stu-id="e920b-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger</span></span>

## <span data-ttu-id="e920b-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="e920b-140">OUTPUTS</span></span>

### <span data-ttu-id="e920b-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e920b-141">System.Boolean</span></span>

## <span data-ttu-id="e920b-142">Notas</span><span class="sxs-lookup"><span data-stu-id="e920b-142">NOTES</span></span>

## <span data-ttu-id="e920b-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e920b-143">RELATED LINKS</span></span>
