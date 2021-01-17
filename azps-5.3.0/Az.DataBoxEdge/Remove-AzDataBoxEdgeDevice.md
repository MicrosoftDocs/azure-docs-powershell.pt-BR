---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeDevice.md
ms.openlocfilehash: 69a484734dfde2459cf05f6eea763a8433b15827
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429942"
---
# <span data-ttu-id="1f62b-101">Remove-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="1f62b-101">Remove-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="1f62b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1f62b-102">SYNOPSIS</span></span>
<span data-ttu-id="1f62b-103">Remove um dispositivo de borda de caixa de dados.</span><span class="sxs-lookup"><span data-stu-id="1f62b-103">Removes a Data Box Edge device.</span></span>

## <span data-ttu-id="1f62b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1f62b-104">SYNTAX</span></span>

### <span data-ttu-id="1f62b-105">DeleteByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="1f62b-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f62b-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f62b-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeDevice -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f62b-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f62b-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeDevice -InputObject <PSDataBoxEdgeDevice> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f62b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1f62b-108">DESCRIPTION</span></span>
<span data-ttu-id="1f62b-109">O cmdlet **Remove-AzDataBoxEdgeDevice** remove a configuração de um dispositivo de borda de caixa de dados.</span><span class="sxs-lookup"><span data-stu-id="1f62b-109">The **Remove-AzDataBoxEdgeDevice** cmdlet removes the configuration for a Data Box Edge device.</span></span>
<span data-ttu-id="1f62b-110">Observe que o dispositivo só pode ser excluído depois que você tiver feito o pedido e antes que o dispositivo seja preparado pela Microsoft para remessa.</span><span class="sxs-lookup"><span data-stu-id="1f62b-110">Note that the device can only be deleted after you have placed the order and before the device is prepared by Microsoft for shipment.</span></span>

<span data-ttu-id="1f62b-111">Consulte a documentação sobre como excluir o recurso antes de usar este [cmdlet](https://docs.microsoft.com/en-us/azure/databox-online/data-box-edge-return-device#delete-the-resource)</span><span class="sxs-lookup"><span data-stu-id="1f62b-111">Refer the documentation on Deleting the resource before using this [cmdlet](https://docs.microsoft.com/en-us/azure/databox-online/data-box-edge-return-device#delete-the-resource)</span></span>

## <span data-ttu-id="1f62b-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1f62b-112">EXAMPLES</span></span>

### <span data-ttu-id="1f62b-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1f62b-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeDevice ResourceGroupName resourceGroupName -Name deviceName
```

## <span data-ttu-id="1f62b-114">OS</span><span class="sxs-lookup"><span data-stu-id="1f62b-114">PARAMETERS</span></span>

### <span data-ttu-id="1f62b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1f62b-115">-AsJob</span></span>
<span data-ttu-id="1f62b-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="1f62b-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1f62b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f62b-117">-DefaultProfile</span></span>
<span data-ttu-id="1f62b-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1f62b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f62b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1f62b-119">-InputObject</span></span>
<span data-ttu-id="1f62b-120">Objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="1f62b-120">Input Object</span></span>

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

### <span data-ttu-id="1f62b-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="1f62b-121">-Name</span></span>
<span data-ttu-id="1f62b-122">Nome do recurso</span><span class="sxs-lookup"><span data-stu-id="1f62b-122">Resource Name</span></span>

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

### <span data-ttu-id="1f62b-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1f62b-123">-PassThru</span></span>
<span data-ttu-id="1f62b-124">Retorna verdadeiro se bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="1f62b-124">returns true if successful</span></span>

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

### <span data-ttu-id="1f62b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f62b-125">-ResourceGroupName</span></span>
<span data-ttu-id="1f62b-126">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="1f62b-126">Resource Group Name</span></span>

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

### <span data-ttu-id="1f62b-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1f62b-127">-ResourceId</span></span>
<span data-ttu-id="1f62b-128">ResourceId do Azure</span><span class="sxs-lookup"><span data-stu-id="1f62b-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="1f62b-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1f62b-129">-Confirm</span></span>
<span data-ttu-id="1f62b-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f62b-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f62b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f62b-131">-WhatIf</span></span>
<span data-ttu-id="1f62b-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1f62b-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1f62b-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1f62b-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f62b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f62b-134">CommonParameters</span></span>
<span data-ttu-id="1f62b-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f62b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f62b-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1f62b-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f62b-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1f62b-137">INPUTS</span></span>

### <span data-ttu-id="1f62b-138">System. String</span><span class="sxs-lookup"><span data-stu-id="1f62b-138">System.String</span></span>

### <span data-ttu-id="1f62b-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="1f62b-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="1f62b-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1f62b-140">OUTPUTS</span></span>

### <span data-ttu-id="1f62b-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1f62b-141">System.Boolean</span></span>

## <span data-ttu-id="1f62b-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1f62b-142">NOTES</span></span>

## <span data-ttu-id="1f62b-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1f62b-143">RELATED LINKS</span></span>
