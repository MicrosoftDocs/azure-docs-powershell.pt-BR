---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeShare.md
ms.openlocfilehash: ac3282d8249eecbb6e8c7bd1fb23a5ab0f55ed95
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433951"
---
# <span data-ttu-id="7d2dc-101">Remove-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="7d2dc-101">Remove-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="7d2dc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7d2dc-102">SYNOPSIS</span></span>
<span data-ttu-id="7d2dc-103">Remove um compartilhamento do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7d2dc-103">Removes a share from the device.</span></span>

## <span data-ttu-id="7d2dc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7d2dc-104">SYNTAX</span></span>

### <span data-ttu-id="7d2dc-105">DeleteByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="7d2dc-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d2dc-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d2dc-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeShare [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d2dc-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d2dc-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeShare [-InputObject] <PSDataBoxEdgeShare> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d2dc-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7d2dc-108">DESCRIPTION</span></span>
<span data-ttu-id="7d2dc-109">O cmdlet **Remove-AzDataBoxEdgeEdgeShare** remove os compartilhamentos de borda associados de um dispositivo de borda de caixa de dados.</span><span class="sxs-lookup"><span data-stu-id="7d2dc-109">The **Remove-AzDataBoxEdgeEdgeShare** cmdlet removes the associated edge shares for a Data Box Edge device.</span></span>

## <span data-ttu-id="7d2dc-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7d2dc-110">EXAMPLES</span></span>

### <span data-ttu-id="7d2dc-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7d2dc-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name shareName
```

## <span data-ttu-id="7d2dc-112">OS</span><span class="sxs-lookup"><span data-stu-id="7d2dc-112">PARAMETERS</span></span>

### <span data-ttu-id="7d2dc-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7d2dc-113">-AsJob</span></span>
<span data-ttu-id="7d2dc-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="7d2dc-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7d2dc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d2dc-115">-DefaultProfile</span></span>
<span data-ttu-id="7d2dc-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7d2dc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d2dc-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="7d2dc-117">-DeviceName</span></span>
<span data-ttu-id="7d2dc-118">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="7d2dc-118">Device Name</span></span>

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

### <span data-ttu-id="7d2dc-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7d2dc-119">-InputObject</span></span>
<span data-ttu-id="7d2dc-120">Objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="7d2dc-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d2dc-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="7d2dc-121">-Name</span></span>
<span data-ttu-id="7d2dc-122">Nome do recurso</span><span class="sxs-lookup"><span data-stu-id="7d2dc-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d2dc-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7d2dc-123">-PassThru</span></span>
<span data-ttu-id="7d2dc-124">Retorna verdadeiro se bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="7d2dc-124">returns true if successful</span></span>

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

### <span data-ttu-id="7d2dc-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d2dc-125">-ResourceGroupName</span></span>
<span data-ttu-id="7d2dc-126">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="7d2dc-126">Resource Group Name</span></span>

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

### <span data-ttu-id="7d2dc-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d2dc-127">-ResourceId</span></span>
<span data-ttu-id="7d2dc-128">ResourceId do Azure</span><span class="sxs-lookup"><span data-stu-id="7d2dc-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="7d2dc-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7d2dc-129">-Confirm</span></span>
<span data-ttu-id="7d2dc-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d2dc-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d2dc-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d2dc-131">-WhatIf</span></span>
<span data-ttu-id="7d2dc-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7d2dc-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7d2dc-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7d2dc-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d2dc-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d2dc-134">CommonParameters</span></span>
<span data-ttu-id="7d2dc-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d2dc-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d2dc-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7d2dc-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d2dc-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7d2dc-137">INPUTS</span></span>

### <span data-ttu-id="7d2dc-138">System. String</span><span class="sxs-lookup"><span data-stu-id="7d2dc-138">System.String</span></span>

### <span data-ttu-id="7d2dc-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="7d2dc-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="7d2dc-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7d2dc-140">OUTPUTS</span></span>

### <span data-ttu-id="7d2dc-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7d2dc-141">System.Boolean</span></span>

## <span data-ttu-id="7d2dc-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7d2dc-142">NOTES</span></span>

## <span data-ttu-id="7d2dc-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7d2dc-143">RELATED LINKS</span></span>
