---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeOrder.md
ms.openlocfilehash: 5effec8ed39f9219bcecba23f6ca3cabaae5cec9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113822"
---
# <span data-ttu-id="4735b-101">Remove-AzStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="4735b-101">Remove-AzStackEdgeOrder</span></span>

## <span data-ttu-id="4735b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4735b-102">SYNOPSIS</span></span>
<span data-ttu-id="4735b-103">Remove o pedido de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4735b-103">Removes the order for a device.</span></span>

## <span data-ttu-id="4735b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4735b-104">SYNTAX</span></span>

### <span data-ttu-id="4735b-105">DeleteByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="4735b-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4735b-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4735b-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeOrder -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4735b-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4735b-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeOrder -InputObject <PSStackEdgeOrder> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4735b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4735b-108">DESCRIPTION</span></span>
<span data-ttu-id="4735b-109">O cmdlet **Remove-AzStackEdgeOrder** exclui uma ordem existente de um dispositivo de borda de pilha.</span><span class="sxs-lookup"><span data-stu-id="4735b-109">The **Remove-AzStackEdgeOrder** cmdlet deletes an existing order for a Stack Edge device.</span></span>

## <span data-ttu-id="4735b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4735b-110">EXAMPLES</span></span>

### <span data-ttu-id="4735b-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4735b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
```

## <span data-ttu-id="4735b-112">OS</span><span class="sxs-lookup"><span data-stu-id="4735b-112">PARAMETERS</span></span>

### <span data-ttu-id="4735b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4735b-113">-AsJob</span></span>
<span data-ttu-id="4735b-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="4735b-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4735b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4735b-115">-DefaultProfile</span></span>
<span data-ttu-id="4735b-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4735b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4735b-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="4735b-117">-DeviceName</span></span>
<span data-ttu-id="4735b-118">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="4735b-118">Device Name</span></span>

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

### <span data-ttu-id="4735b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4735b-119">-InputObject</span></span>
<span data-ttu-id="4735b-120">Objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="4735b-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4735b-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4735b-121">-PassThru</span></span>
<span data-ttu-id="4735b-122">Retorna verdadeiro se bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="4735b-122">returns true if successful</span></span>

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

### <span data-ttu-id="4735b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4735b-123">-ResourceGroupName</span></span>
<span data-ttu-id="4735b-124">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="4735b-124">Resource Group Name</span></span>

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

### <span data-ttu-id="4735b-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4735b-125">-ResourceId</span></span>
<span data-ttu-id="4735b-126">ResourceId do Azure</span><span class="sxs-lookup"><span data-stu-id="4735b-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="4735b-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4735b-127">-Confirm</span></span>
<span data-ttu-id="4735b-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4735b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4735b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4735b-129">-WhatIf</span></span>
<span data-ttu-id="4735b-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4735b-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4735b-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4735b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4735b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4735b-132">CommonParameters</span></span>
<span data-ttu-id="4735b-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4735b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4735b-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4735b-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4735b-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4735b-135">INPUTS</span></span>

### <span data-ttu-id="4735b-136">System. String</span><span class="sxs-lookup"><span data-stu-id="4735b-136">System.String</span></span>

### <span data-ttu-id="4735b-137">Microsoft. Azure. PowerShell. cmdlets. StackEdge. Models. PSStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="4735b-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="4735b-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4735b-138">OUTPUTS</span></span>

### <span data-ttu-id="4735b-139">Microsoft. Azure. PowerShell. cmdlets. StackEdge. Models. PSStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="4735b-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="4735b-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4735b-140">NOTES</span></span>

## <span data-ttu-id="4735b-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4735b-141">RELATED LINKS</span></span>
