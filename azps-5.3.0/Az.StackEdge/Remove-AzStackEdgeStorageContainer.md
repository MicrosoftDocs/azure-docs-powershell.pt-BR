---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageContainer.md
ms.openlocfilehash: c1e76da1fc01ea1698c56e40fd3bd46f6378ea07
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98264670"
---
# <span data-ttu-id="68f1e-101">Remove-AzStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="68f1e-101">Remove-AzStackEdgeStorageContainer</span></span>

## <span data-ttu-id="68f1e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="68f1e-102">SYNOPSIS</span></span>
<span data-ttu-id="68f1e-103">Remove um contêiner de armazenamento da conta de armazenamento de borda em um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="68f1e-103">Removes a storage container for the Edge Storage account on a device.</span></span>

## <span data-ttu-id="68f1e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="68f1e-104">SYNTAX</span></span>

### <span data-ttu-id="68f1e-105">DeleteByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="68f1e-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68f1e-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="68f1e-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeStorageContainer -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68f1e-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="68f1e-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeStorageContainer -InputObject <PSStackEdgeStorageContainer> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68f1e-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="68f1e-108">DESCRIPTION</span></span>
<span data-ttu-id="68f1e-109">O cmdlet **Remove-AzStackEdgeStorageContainer** remove um contêiner de armazenamento associado para a conta de armazenamento de borda em um dispositivo de borda de pilha.</span><span class="sxs-lookup"><span data-stu-id="68f1e-109">The **Remove-AzStackEdgeStorageContainer** cmdlet removes an associated storage container for the Edge Storage account on a Stack Edge device.</span></span> <span data-ttu-id="68f1e-110">Você pode especificar o nome do contêiner de armazenamento a ser removido como um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="68f1e-110">You can specify the name of the storage container to be removed as a parameter.</span></span>

## <span data-ttu-id="68f1e-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="68f1e-111">EXAMPLES</span></span>

### <span data-ttu-id="68f1e-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="68f1e-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccountname -Name container1
```

## <span data-ttu-id="68f1e-113">OS</span><span class="sxs-lookup"><span data-stu-id="68f1e-113">PARAMETERS</span></span>

### <span data-ttu-id="68f1e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="68f1e-114">-AsJob</span></span>
<span data-ttu-id="68f1e-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="68f1e-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="68f1e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68f1e-116">-DefaultProfile</span></span>
<span data-ttu-id="68f1e-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="68f1e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68f1e-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="68f1e-118">-DeviceName</span></span>
<span data-ttu-id="68f1e-119">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="68f1e-119">Device Name</span></span>

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

### <span data-ttu-id="68f1e-120">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="68f1e-120">-EdgeStorageAccountName</span></span>
<span data-ttu-id="68f1e-121">Fornecer o nome de EdgeStorageAccount existente</span><span class="sxs-lookup"><span data-stu-id="68f1e-121">Provide existing EdgeStorageAccount's Name</span></span>

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

### <span data-ttu-id="68f1e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="68f1e-122">-InputObject</span></span>
<span data-ttu-id="68f1e-123">Objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="68f1e-123">Input Object</span></span>

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

### <span data-ttu-id="68f1e-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="68f1e-124">-Name</span></span>
<span data-ttu-id="68f1e-125">Nome do recurso</span><span class="sxs-lookup"><span data-stu-id="68f1e-125">Resource Name</span></span>

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

### <span data-ttu-id="68f1e-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="68f1e-126">-PassThru</span></span>
<span data-ttu-id="68f1e-127">Retorna verdadeiro se bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="68f1e-127">returns true if successful</span></span>

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

### <span data-ttu-id="68f1e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68f1e-128">-ResourceGroupName</span></span>
<span data-ttu-id="68f1e-129">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="68f1e-129">Resource Group Name</span></span>

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

### <span data-ttu-id="68f1e-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="68f1e-130">-ResourceId</span></span>
<span data-ttu-id="68f1e-131">ResourceId do Azure</span><span class="sxs-lookup"><span data-stu-id="68f1e-131">Azure ResourceId</span></span>

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

### <span data-ttu-id="68f1e-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="68f1e-132">-Confirm</span></span>
<span data-ttu-id="68f1e-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68f1e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68f1e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68f1e-134">-WhatIf</span></span>
<span data-ttu-id="68f1e-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="68f1e-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="68f1e-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="68f1e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68f1e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68f1e-137">CommonParameters</span></span>
<span data-ttu-id="68f1e-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68f1e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68f1e-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="68f1e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68f1e-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="68f1e-140">INPUTS</span></span>

### <span data-ttu-id="68f1e-141">System. String</span><span class="sxs-lookup"><span data-stu-id="68f1e-141">System.String</span></span>

### <span data-ttu-id="68f1e-142">Microsoft. Azure. PowerShell. cmdlets. StackEdge. Models. PSStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="68f1e-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="68f1e-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="68f1e-143">OUTPUTS</span></span>

### <span data-ttu-id="68f1e-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="68f1e-144">System.Boolean</span></span>

## <span data-ttu-id="68f1e-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="68f1e-145">NOTES</span></span>

## <span data-ttu-id="68f1e-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="68f1e-146">RELATED LINKS</span></span>
