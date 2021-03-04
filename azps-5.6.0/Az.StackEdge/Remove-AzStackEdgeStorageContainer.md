---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/remove-azstackedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageContainer.md
ms.openlocfilehash: 6a07031c376e406be1d957a33475af799b229b8f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892289"
---
# <span data-ttu-id="c0319-101">Remove-AzStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c0319-101">Remove-AzStackEdgeStorageContainer</span></span>

## <span data-ttu-id="c0319-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0319-102">SYNOPSIS</span></span>
<span data-ttu-id="c0319-103">Remove um contêiner de armazenamento para a conta de Armazenamento de Borda em um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c0319-103">Removes a storage container for the Edge Storage account on a device.</span></span>

## <span data-ttu-id="c0319-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c0319-104">SYNTAX</span></span>

### <span data-ttu-id="c0319-105">DeleteByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c0319-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0319-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0319-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeStorageContainer -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0319-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0319-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeStorageContainer -InputObject <PSStackEdgeStorageContainer> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0319-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c0319-108">DESCRIPTION</span></span>
<span data-ttu-id="c0319-109">O cmdlet **Remove-AzStackEdgeStorageContainer** remove um contêiner de armazenamento associado para a conta de Armazenamento de Borda em um dispositivo de Borda de Pilha.</span><span class="sxs-lookup"><span data-stu-id="c0319-109">The **Remove-AzStackEdgeStorageContainer** cmdlet removes an associated storage container for the Edge Storage account on a Stack Edge device.</span></span> <span data-ttu-id="c0319-110">Você pode especificar o nome do contêiner de armazenamento a ser removido como parâmetro.</span><span class="sxs-lookup"><span data-stu-id="c0319-110">You can specify the name of the storage container to be removed as a parameter.</span></span>

## <span data-ttu-id="c0319-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c0319-111">EXAMPLES</span></span>

### <span data-ttu-id="c0319-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c0319-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccountname -Name container1
```

## <span data-ttu-id="c0319-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c0319-113">PARAMETERS</span></span>

### <span data-ttu-id="c0319-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c0319-114">-AsJob</span></span>
<span data-ttu-id="c0319-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="c0319-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c0319-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0319-116">-DefaultProfile</span></span>
<span data-ttu-id="c0319-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c0319-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0319-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="c0319-118">-DeviceName</span></span>
<span data-ttu-id="c0319-119">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="c0319-119">Device Name</span></span>

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

### <span data-ttu-id="c0319-120">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c0319-120">-EdgeStorageAccountName</span></span>
<span data-ttu-id="c0319-121">Fornecer o nome de EdgeStorageAccount existente</span><span class="sxs-lookup"><span data-stu-id="c0319-121">Provide existing EdgeStorageAccount's Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0319-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0319-122">-InputObject</span></span>
<span data-ttu-id="c0319-123">Objeto Input</span><span class="sxs-lookup"><span data-stu-id="c0319-123">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: EdgeStorageContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0319-124">-Name</span><span class="sxs-lookup"><span data-stu-id="c0319-124">-Name</span></span>
<span data-ttu-id="c0319-125">Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="c0319-125">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: EdgeContainerName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0319-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c0319-126">-PassThru</span></span>
<span data-ttu-id="c0319-127">retorna true se bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="c0319-127">returns true if successful</span></span>

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

### <span data-ttu-id="c0319-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0319-128">-ResourceGroupName</span></span>
<span data-ttu-id="c0319-129">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="c0319-129">Resource Group Name</span></span>

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

### <span data-ttu-id="c0319-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0319-130">-ResourceId</span></span>
<span data-ttu-id="c0319-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0319-131">Azure ResourceId</span></span>

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

### <span data-ttu-id="c0319-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c0319-132">-Confirm</span></span>
<span data-ttu-id="c0319-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0319-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0319-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0319-134">-WhatIf</span></span>
<span data-ttu-id="c0319-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c0319-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c0319-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c0319-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0319-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0319-137">CommonParameters</span></span>
<span data-ttu-id="c0319-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0319-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0319-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c0319-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0319-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c0319-140">INPUTS</span></span>

### <span data-ttu-id="c0319-141">System.String</span><span class="sxs-lookup"><span data-stu-id="c0319-141">System.String</span></span>

### <span data-ttu-id="c0319-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c0319-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="c0319-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c0319-143">OUTPUTS</span></span>

### <span data-ttu-id="c0319-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c0319-144">System.Boolean</span></span>

## <span data-ttu-id="c0319-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="c0319-145">NOTES</span></span>

## <span data-ttu-id="c0319-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c0319-146">RELATED LINKS</span></span>
