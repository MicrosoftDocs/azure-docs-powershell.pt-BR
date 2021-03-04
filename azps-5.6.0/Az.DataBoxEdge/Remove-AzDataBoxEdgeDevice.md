---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/remove-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeDevice.md
ms.openlocfilehash: 1f2c2e2bf02718053d3656b084f845f40215aceb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889994"
---
# <span data-ttu-id="bc436-101">Remove-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="bc436-101">Remove-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="bc436-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc436-102">SYNOPSIS</span></span>
<span data-ttu-id="bc436-103">Remove um dispositivo de Borda da Caixa de Dados.</span><span class="sxs-lookup"><span data-stu-id="bc436-103">Removes a Data Box Edge device.</span></span>

## <span data-ttu-id="bc436-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="bc436-104">SYNTAX</span></span>

### <span data-ttu-id="bc436-105">DeleteByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="bc436-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc436-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc436-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeDevice -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc436-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc436-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeDevice -InputObject <PSDataBoxEdgeDevice> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc436-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="bc436-108">DESCRIPTION</span></span>
<span data-ttu-id="bc436-109">O cmdlet **Remove-AzDataBoxEdgeDevice** remove a configuração de um dispositivo de Borda da Caixa de Dados.</span><span class="sxs-lookup"><span data-stu-id="bc436-109">The **Remove-AzDataBoxEdgeDevice** cmdlet removes the configuration for a Data Box Edge device.</span></span>
<span data-ttu-id="bc436-110">Observe que o dispositivo só pode ser excluído depois que você tiver feito o pedido e antes de o dispositivo ser preparado pela Microsoft para envio.</span><span class="sxs-lookup"><span data-stu-id="bc436-110">Note that the device can only be deleted after you have placed the order and before the device is prepared by Microsoft for shipment.</span></span>

<span data-ttu-id="bc436-111">Consulte a documentação sobre Como excluir o recurso antes de usar este [cmdlet](https://docs.microsoft.com/azure/databox-online/data-box-edge-return-device#delete-the-resource)</span><span class="sxs-lookup"><span data-stu-id="bc436-111">Refer the documentation on Deleting the resource before using this [cmdlet](https://docs.microsoft.com/azure/databox-online/data-box-edge-return-device#delete-the-resource)</span></span>

## <span data-ttu-id="bc436-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bc436-112">EXAMPLES</span></span>

### <span data-ttu-id="bc436-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bc436-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeDevice ResourceGroupName resourceGroupName -Name deviceName
```

## <span data-ttu-id="bc436-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="bc436-114">PARAMETERS</span></span>

### <span data-ttu-id="bc436-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bc436-115">-AsJob</span></span>
<span data-ttu-id="bc436-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="bc436-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bc436-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc436-117">-DefaultProfile</span></span>
<span data-ttu-id="bc436-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bc436-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc436-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bc436-119">-InputObject</span></span>
<span data-ttu-id="bc436-120">Objeto Input</span><span class="sxs-lookup"><span data-stu-id="bc436-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc436-121">-Name</span><span class="sxs-lookup"><span data-stu-id="bc436-121">-Name</span></span>
<span data-ttu-id="bc436-122">Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="bc436-122">Resource Name</span></span>

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

### <span data-ttu-id="bc436-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bc436-123">-PassThru</span></span>
<span data-ttu-id="bc436-124">retorna true se bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="bc436-124">returns true if successful</span></span>

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

### <span data-ttu-id="bc436-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc436-125">-ResourceGroupName</span></span>
<span data-ttu-id="bc436-126">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="bc436-126">Resource Group Name</span></span>

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

### <span data-ttu-id="bc436-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bc436-127">-ResourceId</span></span>
<span data-ttu-id="bc436-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="bc436-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="bc436-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bc436-129">-Confirm</span></span>
<span data-ttu-id="bc436-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc436-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc436-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc436-131">-WhatIf</span></span>
<span data-ttu-id="bc436-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bc436-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bc436-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bc436-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc436-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc436-134">CommonParameters</span></span>
<span data-ttu-id="bc436-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc436-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc436-136">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bc436-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc436-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bc436-137">INPUTS</span></span>

### <span data-ttu-id="bc436-138">System.String</span><span class="sxs-lookup"><span data-stu-id="bc436-138">System.String</span></span>

### <span data-ttu-id="bc436-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="bc436-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="bc436-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="bc436-140">OUTPUTS</span></span>

### <span data-ttu-id="bc436-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bc436-141">System.Boolean</span></span>

## <span data-ttu-id="bc436-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="bc436-142">NOTES</span></span>

## <span data-ttu-id="bc436-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bc436-143">RELATED LINKS</span></span>
