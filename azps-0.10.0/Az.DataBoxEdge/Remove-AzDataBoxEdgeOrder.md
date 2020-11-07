---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeOrder.md
ms.openlocfilehash: 7ac5bce520e566208ddac18374ef01f2cff843ab
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776746"
---
# <span data-ttu-id="eea37-101">Remove-AzDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="eea37-101">Remove-AzDataBoxEdgeOrder</span></span>

## <span data-ttu-id="eea37-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="eea37-102">SYNOPSIS</span></span>
<span data-ttu-id="eea37-103">Remove o pedido de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eea37-103">Removes the order for a device.</span></span>

## <span data-ttu-id="eea37-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eea37-104">SYNTAX</span></span>

### <span data-ttu-id="eea37-105">DeleteByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="eea37-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eea37-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eea37-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeOrder -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eea37-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eea37-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeOrder -InputObject <PSDataBoxEdgeOrder> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eea37-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="eea37-108">DESCRIPTION</span></span>
<span data-ttu-id="eea37-109">O cmdlet **Remove-AzDataBoxEdgeOrder** exclui uma ordem existente de um dispositivo de borda de caixa de dados.</span><span class="sxs-lookup"><span data-stu-id="eea37-109">The **Remove-AzDataBoxEdgeOrder** cmdlet deletes an existing order for a Data Box Edge device.</span></span>

## <span data-ttu-id="eea37-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="eea37-110">EXAMPLES</span></span>

### <span data-ttu-id="eea37-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="eea37-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
```

## <span data-ttu-id="eea37-112">OS</span><span class="sxs-lookup"><span data-stu-id="eea37-112">PARAMETERS</span></span>

### <span data-ttu-id="eea37-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eea37-113">-AsJob</span></span>
<span data-ttu-id="eea37-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="eea37-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eea37-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eea37-115">-DefaultProfile</span></span>
<span data-ttu-id="eea37-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="eea37-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eea37-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="eea37-117">-DeviceName</span></span>
<span data-ttu-id="eea37-118">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="eea37-118">Device Name</span></span>

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

### <span data-ttu-id="eea37-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eea37-119">-InputObject</span></span>
<span data-ttu-id="eea37-120">Objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="eea37-120">Input Object</span></span>

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

### <span data-ttu-id="eea37-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eea37-121">-PassThru</span></span>
<span data-ttu-id="eea37-122">Retorna verdadeiro se bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="eea37-122">returns true if successful</span></span>

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

### <span data-ttu-id="eea37-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eea37-123">-ResourceGroupName</span></span>
<span data-ttu-id="eea37-124">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="eea37-124">Resource Group Name</span></span>

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

### <span data-ttu-id="eea37-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eea37-125">-ResourceId</span></span>
<span data-ttu-id="eea37-126">ResourceId do Azure</span><span class="sxs-lookup"><span data-stu-id="eea37-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="eea37-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="eea37-127">-Confirm</span></span>
<span data-ttu-id="eea37-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eea37-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eea37-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eea37-129">-WhatIf</span></span>
<span data-ttu-id="eea37-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="eea37-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eea37-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="eea37-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eea37-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eea37-132">CommonParameters</span></span>
<span data-ttu-id="eea37-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eea37-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eea37-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eea37-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eea37-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="eea37-135">INPUTS</span></span>

### <span data-ttu-id="eea37-136">System. String</span><span class="sxs-lookup"><span data-stu-id="eea37-136">System.String</span></span>

### <span data-ttu-id="eea37-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="eea37-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="eea37-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="eea37-138">OUTPUTS</span></span>

### <span data-ttu-id="eea37-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="eea37-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="eea37-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="eea37-140">NOTES</span></span>

## <span data-ttu-id="eea37-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eea37-141">RELATED LINKS</span></span>
