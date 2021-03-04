---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/invoke-azstackedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeStorageContainer.md
ms.openlocfilehash: ce4c80146524f57e48570b9739f78635e3e21b32
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889137"
---
# <span data-ttu-id="7bd42-101">Invoke-AzStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="7bd42-101">Invoke-AzStackEdgeStorageContainer</span></span>

## <span data-ttu-id="7bd42-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7bd42-102">SYNOPSIS</span></span>
<span data-ttu-id="7bd42-103">Invoca ações específicas em um contêiner de armazenamento</span><span class="sxs-lookup"><span data-stu-id="7bd42-103">Invokes specific actions on a storage container</span></span>

## <span data-ttu-id="7bd42-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7bd42-104">SYNTAX</span></span>

### <span data-ttu-id="7bd42-105">InvokeByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7bd42-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-RefreshData] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bd42-106">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7bd42-106">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeStorageContainer [-ResourceId] <String> [-RefreshData] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bd42-107">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7bd42-107">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzStackEdgeStorageContainer [-RefreshData] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 -InputObject <PSStackEdgeStorageContainer> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7bd42-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7bd42-108">DESCRIPTION</span></span>
<span data-ttu-id="7bd42-109">O cmdlet **Invoke-AzStackEdgeStorageContainer** invoca ações para atualizar os dados em um contêiner de armazenamento em um dispositivo de Borda de Pilha.</span><span class="sxs-lookup"><span data-stu-id="7bd42-109">The **Invoke-AzStackEdgeStorageContainer** cmdlet invokes actions to refresh the data on a storage container on a Stack Edge device.</span></span> 

## <span data-ttu-id="7bd42-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7bd42-110">EXAMPLES</span></span>

### <span data-ttu-id="7bd42-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7bd42-111">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccount1 -Name container1 -PassThru
PS C:\> true
```

### <span data-ttu-id="7bd42-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="7bd42-112">Example 2</span></span>
```powershell
PS C:\> Get-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccount1 -Name container1 | Invoke-AzStackEdgeStorageContainer
```

## <span data-ttu-id="7bd42-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7bd42-113">PARAMETERS</span></span>

### <span data-ttu-id="7bd42-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7bd42-114">-AsJob</span></span>
<span data-ttu-id="7bd42-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="7bd42-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7bd42-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bd42-116">-DefaultProfile</span></span>
<span data-ttu-id="7bd42-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7bd42-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7bd42-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="7bd42-118">-DeviceName</span></span>
<span data-ttu-id="7bd42-119">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="7bd42-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bd42-120">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7bd42-120">-EdgeStorageAccountName</span></span>
<span data-ttu-id="7bd42-121">Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="7bd42-121">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bd42-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7bd42-122">-InputObject</span></span>
<span data-ttu-id="7bd42-123">Fornecer objeto EdgeStorageAccount existente</span><span class="sxs-lookup"><span data-stu-id="7bd42-123">Provide existing EdgeStorageAccount Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer
Parameter Sets: InvokeByInputObjectParameterSet
Aliases: EdgeStorageContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7bd42-124">-Name</span><span class="sxs-lookup"><span data-stu-id="7bd42-124">-Name</span></span>
<span data-ttu-id="7bd42-125">Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="7bd42-125">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases: EdgeContainerName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bd42-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7bd42-126">-PassThru</span></span>
<span data-ttu-id="7bd42-127">retorna true se bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="7bd42-127">returns true if successful</span></span>

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

### <span data-ttu-id="7bd42-128">-RefreshData</span><span class="sxs-lookup"><span data-stu-id="7bd42-128">-RefreshData</span></span>
<span data-ttu-id="7bd42-129">Atualizar metadados de contêiner com os dados da nuvem</span><span class="sxs-lookup"><span data-stu-id="7bd42-129">Refresh Container Metadata with the data from the cloud</span></span>

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

### <span data-ttu-id="7bd42-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bd42-130">-ResourceGroupName</span></span>
<span data-ttu-id="7bd42-131">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="7bd42-131">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bd42-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7bd42-132">-ResourceId</span></span>
<span data-ttu-id="7bd42-133">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="7bd42-133">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bd42-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7bd42-134">-Confirm</span></span>
<span data-ttu-id="7bd42-135">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7bd42-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bd42-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bd42-136">-WhatIf</span></span>
<span data-ttu-id="7bd42-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7bd42-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7bd42-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7bd42-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bd42-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bd42-139">CommonParameters</span></span>
<span data-ttu-id="7bd42-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bd42-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bd42-141">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7bd42-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bd42-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7bd42-142">INPUTS</span></span>

### <span data-ttu-id="7bd42-143">System.String</span><span class="sxs-lookup"><span data-stu-id="7bd42-143">System.String</span></span>

### <span data-ttu-id="7bd42-144">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="7bd42-144">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="7bd42-145">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7bd42-145">OUTPUTS</span></span>

### <span data-ttu-id="7bd42-146">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="7bd42-146">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="7bd42-147">NOTES</span><span class="sxs-lookup"><span data-stu-id="7bd42-147">NOTES</span></span>

## <span data-ttu-id="7bd42-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7bd42-148">RELATED LINKS</span></span>
