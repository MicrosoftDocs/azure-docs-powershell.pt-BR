---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/remove-azstackedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeDevice.md
ms.openlocfilehash: 174fe29d45d20b1b1e0ed0c3935bfd99ad2e1a87
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892300"
---
# <span data-ttu-id="dc127-101">Remove-AzStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="dc127-101">Remove-AzStackEdgeDevice</span></span>

## <span data-ttu-id="dc127-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc127-102">SYNOPSIS</span></span>
<span data-ttu-id="dc127-103">Remove um dispositivo de Borda de Pilha.</span><span class="sxs-lookup"><span data-stu-id="dc127-103">Removes a Stack Edge device.</span></span>

## <span data-ttu-id="dc127-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="dc127-104">SYNTAX</span></span>

### <span data-ttu-id="dc127-105">DeleteByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="dc127-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc127-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc127-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeDevice -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc127-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc127-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc127-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="dc127-108">DESCRIPTION</span></span>
<span data-ttu-id="dc127-109">O cmdlet **Remove-AzStackEdgeDevice** remove a configuração de um dispositivo de Borda de Pilha.</span><span class="sxs-lookup"><span data-stu-id="dc127-109">The **Remove-AzStackEdgeDevice** cmdlet removes the configuration for a Stack Edge device.</span></span>
<span data-ttu-id="dc127-110">Observe que o dispositivo só pode ser excluído depois que você tiver feito o pedido e antes de o dispositivo ser preparado pela Microsoft para envio.</span><span class="sxs-lookup"><span data-stu-id="dc127-110">Note that the device can only be deleted after you have placed the order and before the device is prepared by Microsoft for shipment.</span></span>

<span data-ttu-id="dc127-111">Consulte a documentação sobre Como excluir o recurso antes de usar este [cmdlet](https://docs.microsoft.com/azure/databox-online/data-box-edge-return-device#delete-the-resource)</span><span class="sxs-lookup"><span data-stu-id="dc127-111">Refer the documentation on Deleting the resource before using this [cmdlet](https://docs.microsoft.com/azure/databox-online/data-box-edge-return-device#delete-the-resource)</span></span>

## <span data-ttu-id="dc127-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dc127-112">EXAMPLES</span></span>

### <span data-ttu-id="dc127-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="dc127-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeDevice ResourceGroupName resourceGroupName -Name deviceName
```

## <span data-ttu-id="dc127-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="dc127-114">PARAMETERS</span></span>

### <span data-ttu-id="dc127-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dc127-115">-AsJob</span></span>
<span data-ttu-id="dc127-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="dc127-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dc127-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc127-117">-DefaultProfile</span></span>
<span data-ttu-id="dc127-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dc127-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc127-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="dc127-119">-DeviceObject</span></span>
<span data-ttu-id="dc127-120">Objeto Input</span><span class="sxs-lookup"><span data-stu-id="dc127-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc127-121">-Name</span><span class="sxs-lookup"><span data-stu-id="dc127-121">-Name</span></span>
<span data-ttu-id="dc127-122">Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="dc127-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: DeviceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc127-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dc127-123">-PassThru</span></span>
<span data-ttu-id="dc127-124">retorna true se bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="dc127-124">returns true if successful</span></span>

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

### <span data-ttu-id="dc127-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc127-125">-ResourceGroupName</span></span>
<span data-ttu-id="dc127-126">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="dc127-126">Resource Group Name</span></span>

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

### <span data-ttu-id="dc127-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dc127-127">-ResourceId</span></span>
<span data-ttu-id="dc127-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="dc127-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="dc127-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dc127-129">-Confirm</span></span>
<span data-ttu-id="dc127-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc127-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc127-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc127-131">-WhatIf</span></span>
<span data-ttu-id="dc127-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="dc127-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dc127-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dc127-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc127-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc127-134">CommonParameters</span></span>
<span data-ttu-id="dc127-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc127-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc127-136">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dc127-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc127-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dc127-137">INPUTS</span></span>

### <span data-ttu-id="dc127-138">System.String</span><span class="sxs-lookup"><span data-stu-id="dc127-138">System.String</span></span>

### <span data-ttu-id="dc127-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="dc127-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="dc127-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="dc127-140">OUTPUTS</span></span>

### <span data-ttu-id="dc127-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="dc127-141">System.Boolean</span></span>

## <span data-ttu-id="dc127-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="dc127-142">NOTES</span></span>

## <span data-ttu-id="dc127-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dc127-143">RELATED LINKS</span></span>
