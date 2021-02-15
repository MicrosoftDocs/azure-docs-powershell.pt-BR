---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeDevice.md
ms.openlocfilehash: 69a484734dfde2459cf05f6eea763a8433b15827
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111986"
---
# <span data-ttu-id="1566c-101">Remove-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="1566c-101">Remove-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="1566c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1566c-102">SYNOPSIS</span></span>
<span data-ttu-id="1566c-103">Remove um dispositivo de borda de caixa de dados.</span><span class="sxs-lookup"><span data-stu-id="1566c-103">Removes a Data Box Edge device.</span></span>

## <span data-ttu-id="1566c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1566c-104">SYNTAX</span></span>

### <span data-ttu-id="1566c-105">DeleteByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="1566c-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1566c-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1566c-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeDevice -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1566c-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1566c-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeDevice -InputObject <PSDataBoxEdgeDevice> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1566c-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="1566c-108">DESCRIPTION</span></span>
<span data-ttu-id="1566c-109">O cmdlet **Remove-AzDataBoxEdgeDevice** remove a configuração de um dispositivo de Borda de Caixa de Dados.</span><span class="sxs-lookup"><span data-stu-id="1566c-109">The **Remove-AzDataBoxEdgeDevice** cmdlet removes the configuration for a Data Box Edge device.</span></span>
<span data-ttu-id="1566c-110">Observe que o dispositivo só pode ser excluído depois que você tiver feito o pedido e antes que o dispositivo seja preparado pela Microsoft para envio.</span><span class="sxs-lookup"><span data-stu-id="1566c-110">Note that the device can only be deleted after you have placed the order and before the device is prepared by Microsoft for shipment.</span></span>

<span data-ttu-id="1566c-111">Consultar a documentação sobre a exclusão do recurso antes de usar este [cmdlet](https://docs.microsoft.com/en-us/azure/databox-online/data-box-edge-return-device#delete-the-resource)</span><span class="sxs-lookup"><span data-stu-id="1566c-111">Refer the documentation on Deleting the resource before using this [cmdlet](https://docs.microsoft.com/en-us/azure/databox-online/data-box-edge-return-device#delete-the-resource)</span></span>

## <span data-ttu-id="1566c-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1566c-112">EXAMPLES</span></span>

### <span data-ttu-id="1566c-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1566c-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeDevice ResourceGroupName resourceGroupName -Name deviceName
```

## <span data-ttu-id="1566c-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1566c-114">PARAMETERS</span></span>

### <span data-ttu-id="1566c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1566c-115">-AsJob</span></span>
<span data-ttu-id="1566c-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="1566c-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1566c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1566c-117">-DefaultProfile</span></span>
<span data-ttu-id="1566c-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1566c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1566c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1566c-119">-InputObject</span></span>
<span data-ttu-id="1566c-120">Objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="1566c-120">Input Object</span></span>

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

### <span data-ttu-id="1566c-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="1566c-121">-Name</span></span>
<span data-ttu-id="1566c-122">Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="1566c-122">Resource Name</span></span>

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

### <span data-ttu-id="1566c-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1566c-123">-PassThru</span></span>
<span data-ttu-id="1566c-124">retorna verdadeiro se for bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="1566c-124">returns true if successful</span></span>

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

### <span data-ttu-id="1566c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1566c-125">-ResourceGroupName</span></span>
<span data-ttu-id="1566c-126">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="1566c-126">Resource Group Name</span></span>

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

### <span data-ttu-id="1566c-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1566c-127">-ResourceId</span></span>
<span data-ttu-id="1566c-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="1566c-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="1566c-129">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="1566c-129">-Confirm</span></span>
<span data-ttu-id="1566c-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1566c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1566c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1566c-131">-WhatIf</span></span>
<span data-ttu-id="1566c-132">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="1566c-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1566c-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1566c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1566c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1566c-134">CommonParameters</span></span>
<span data-ttu-id="1566c-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1566c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1566c-136">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1566c-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1566c-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="1566c-137">INPUTS</span></span>

### <span data-ttu-id="1566c-138">System.String</span><span class="sxs-lookup"><span data-stu-id="1566c-138">System.String</span></span>

### <span data-ttu-id="1566c-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="1566c-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="1566c-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="1566c-140">OUTPUTS</span></span>

### <span data-ttu-id="1566c-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1566c-141">System.Boolean</span></span>

## <span data-ttu-id="1566c-142">Notas</span><span class="sxs-lookup"><span data-stu-id="1566c-142">NOTES</span></span>

## <span data-ttu-id="1566c-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1566c-143">RELATED LINKS</span></span>
