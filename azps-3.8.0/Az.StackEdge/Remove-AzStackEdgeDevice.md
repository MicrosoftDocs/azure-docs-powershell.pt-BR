---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeDevice.md
ms.openlocfilehash: 431726e1bcbc0045cb1b9958ce9513638259bd8f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942320"
---
# <span data-ttu-id="a3d47-101">Remove-AzStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="a3d47-101">Remove-AzStackEdgeDevice</span></span>

## <span data-ttu-id="a3d47-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a3d47-102">SYNOPSIS</span></span>
<span data-ttu-id="a3d47-103">Remove um dispositivo de borda de pilha.</span><span class="sxs-lookup"><span data-stu-id="a3d47-103">Removes a Stack Edge device.</span></span>

## <span data-ttu-id="a3d47-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a3d47-104">SYNTAX</span></span>

### <span data-ttu-id="a3d47-105">DeleteByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="a3d47-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3d47-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3d47-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeDevice -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3d47-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3d47-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3d47-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a3d47-108">DESCRIPTION</span></span>
<span data-ttu-id="a3d47-109">O cmdlet **Remove-AzStackEdgeDevice** remove a configuração de um dispositivo de borda de pilha.</span><span class="sxs-lookup"><span data-stu-id="a3d47-109">The **Remove-AzStackEdgeDevice** cmdlet removes the configuration for a Stack Edge device.</span></span>
<span data-ttu-id="a3d47-110">Observe que o dispositivo só pode ser excluído depois que você tiver feito o pedido e antes que o dispositivo seja preparado pela Microsoft para remessa.</span><span class="sxs-lookup"><span data-stu-id="a3d47-110">Note that the device can only be deleted after you have placed the order and before the device is prepared by Microsoft for shipment.</span></span>

<span data-ttu-id="a3d47-111">Consulte a documentação sobre como excluir o recurso antes de usar este [cmdlet](https://docs.microsoft.com/en-us/azure/databox-online/data-box-edge-return-device#delete-the-resource)</span><span class="sxs-lookup"><span data-stu-id="a3d47-111">Refer the documentation on Deleting the resource before using this [cmdlet](https://docs.microsoft.com/en-us/azure/databox-online/data-box-edge-return-device#delete-the-resource)</span></span>

## <span data-ttu-id="a3d47-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a3d47-112">EXAMPLES</span></span>

### <span data-ttu-id="a3d47-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a3d47-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeDevice ResourceGroupName resourceGroupName -Name deviceName
```

## <span data-ttu-id="a3d47-114">OS</span><span class="sxs-lookup"><span data-stu-id="a3d47-114">PARAMETERS</span></span>

### <span data-ttu-id="a3d47-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a3d47-115">-AsJob</span></span>
<span data-ttu-id="a3d47-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="a3d47-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a3d47-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3d47-117">-DefaultProfile</span></span>
<span data-ttu-id="a3d47-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a3d47-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3d47-119">-Deviceobject</span><span class="sxs-lookup"><span data-stu-id="a3d47-119">-DeviceObject</span></span>
<span data-ttu-id="a3d47-120">Objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="a3d47-120">Input Object</span></span>

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

### <span data-ttu-id="a3d47-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="a3d47-121">-Name</span></span>
<span data-ttu-id="a3d47-122">Nome do recurso</span><span class="sxs-lookup"><span data-stu-id="a3d47-122">Resource Name</span></span>

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

### <span data-ttu-id="a3d47-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a3d47-123">-PassThru</span></span>
<span data-ttu-id="a3d47-124">Retorna verdadeiro se bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="a3d47-124">returns true if successful</span></span>

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

### <span data-ttu-id="a3d47-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3d47-125">-ResourceGroupName</span></span>
<span data-ttu-id="a3d47-126">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="a3d47-126">Resource Group Name</span></span>

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

### <span data-ttu-id="a3d47-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a3d47-127">-ResourceId</span></span>
<span data-ttu-id="a3d47-128">ResourceId do Azure</span><span class="sxs-lookup"><span data-stu-id="a3d47-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="a3d47-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a3d47-129">-Confirm</span></span>
<span data-ttu-id="a3d47-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3d47-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3d47-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3d47-131">-WhatIf</span></span>
<span data-ttu-id="a3d47-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a3d47-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a3d47-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a3d47-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3d47-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3d47-134">CommonParameters</span></span>
<span data-ttu-id="a3d47-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3d47-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3d47-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a3d47-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3d47-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a3d47-137">INPUTS</span></span>

### <span data-ttu-id="a3d47-138">System. String</span><span class="sxs-lookup"><span data-stu-id="a3d47-138">System.String</span></span>

### <span data-ttu-id="a3d47-139">Microsoft. Azure. PowerShell. cmdlets. StackEdge. Models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="a3d47-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="a3d47-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a3d47-140">OUTPUTS</span></span>

### <span data-ttu-id="a3d47-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a3d47-141">System.Boolean</span></span>

## <span data-ttu-id="a3d47-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a3d47-142">NOTES</span></span>

## <span data-ttu-id="a3d47-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a3d47-143">RELATED LINKS</span></span>
