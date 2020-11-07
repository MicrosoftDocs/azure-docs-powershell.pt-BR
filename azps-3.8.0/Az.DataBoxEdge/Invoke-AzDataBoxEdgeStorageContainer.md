---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/invoke-azdataboxedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeStorageContainer.md
ms.openlocfilehash: f897c2adfe4154aeff5bd370437ea8b23e4efd36
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943402"
---
# <span data-ttu-id="944ab-101">Invoke-AzDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="944ab-101">Invoke-AzDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="944ab-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="944ab-102">SYNOPSIS</span></span>
<span data-ttu-id="944ab-103">Invoca ações específicas em um contêiner de armazenamento</span><span class="sxs-lookup"><span data-stu-id="944ab-103">Invokes specific actions on a storage container</span></span>

## <span data-ttu-id="944ab-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="944ab-104">SYNTAX</span></span>

### <span data-ttu-id="944ab-105">InvokeByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="944ab-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-RefreshData] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="944ab-106">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="944ab-106">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeStorageContainer [-ResourceId] <String> [-RefreshData] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="944ab-107">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="944ab-107">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeStorageContainer [-RefreshData] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 -InputObject <PSDataBoxEdgeStorageContainer> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="944ab-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="944ab-108">DESCRIPTION</span></span>
<span data-ttu-id="944ab-109">O cmdlet **Invoke-AzDataBoxEdgeStorageContainer** invoca ações para atualizar os dados em um contêiner de armazenamento em um dispositivo de borda de caixa de dados.</span><span class="sxs-lookup"><span data-stu-id="944ab-109">The **Invoke-AzDataBoxEdgeStorageContainer** cmdlet invokes actions to refresh the data on a storage container on a Data Box Edge device.</span></span> 

## <span data-ttu-id="944ab-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="944ab-110">EXAMPLES</span></span>

### <span data-ttu-id="944ab-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="944ab-111">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccount1 -Name container1 -PassThru
PS C:\> true
```

### <span data-ttu-id="944ab-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="944ab-112">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccount1 -Name container1 | Invoke-AzDataBoxEdgeStorageContainer
```

## <span data-ttu-id="944ab-113">OS</span><span class="sxs-lookup"><span data-stu-id="944ab-113">PARAMETERS</span></span>

### <span data-ttu-id="944ab-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="944ab-114">-AsJob</span></span>
<span data-ttu-id="944ab-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="944ab-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="944ab-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="944ab-116">-DefaultProfile</span></span>
<span data-ttu-id="944ab-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="944ab-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="944ab-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="944ab-118">-DeviceName</span></span>
<span data-ttu-id="944ab-119">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="944ab-119">Device Name</span></span>

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

### <span data-ttu-id="944ab-120">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="944ab-120">-EdgeStorageAccountName</span></span>
<span data-ttu-id="944ab-121">Nome do recurso</span><span class="sxs-lookup"><span data-stu-id="944ab-121">Resource Name</span></span>

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

### <span data-ttu-id="944ab-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="944ab-122">-InputObject</span></span>
<span data-ttu-id="944ab-123">Fornecer objeto EdgeStorageAccount existente</span><span class="sxs-lookup"><span data-stu-id="944ab-123">Provide existing EdgeStorageAccount Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer
Parameter Sets: InvokeByInputObjectParameterSet
Aliases: EdgeContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="944ab-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="944ab-124">-Name</span></span>
<span data-ttu-id="944ab-125">Nome do recurso</span><span class="sxs-lookup"><span data-stu-id="944ab-125">Resource Name</span></span>

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

### <span data-ttu-id="944ab-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="944ab-126">-PassThru</span></span>
<span data-ttu-id="944ab-127">Retorna verdadeiro se bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="944ab-127">returns true if successful</span></span>

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

### <span data-ttu-id="944ab-128">-RefreshData</span><span class="sxs-lookup"><span data-stu-id="944ab-128">-RefreshData</span></span>
<span data-ttu-id="944ab-129">Atualizar metadados de contêiner com os dados da nuvem</span><span class="sxs-lookup"><span data-stu-id="944ab-129">Refresh Container Metadata with the data from the cloud</span></span>

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

### <span data-ttu-id="944ab-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="944ab-130">-ResourceGroupName</span></span>
<span data-ttu-id="944ab-131">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="944ab-131">Resource Group Name</span></span>

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

### <span data-ttu-id="944ab-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="944ab-132">-ResourceId</span></span>
<span data-ttu-id="944ab-133">ResourceId do Azure</span><span class="sxs-lookup"><span data-stu-id="944ab-133">Azure ResourceId</span></span>

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

### <span data-ttu-id="944ab-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="944ab-134">-Confirm</span></span>
<span data-ttu-id="944ab-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="944ab-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="944ab-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="944ab-136">-WhatIf</span></span>
<span data-ttu-id="944ab-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="944ab-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="944ab-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="944ab-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="944ab-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="944ab-139">CommonParameters</span></span>
<span data-ttu-id="944ab-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="944ab-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="944ab-141">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="944ab-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="944ab-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="944ab-142">INPUTS</span></span>

### <span data-ttu-id="944ab-143">System. String</span><span class="sxs-lookup"><span data-stu-id="944ab-143">System.String</span></span>

### <span data-ttu-id="944ab-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="944ab-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="944ab-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="944ab-145">OUTPUTS</span></span>

### <span data-ttu-id="944ab-146">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="944ab-146">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="944ab-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="944ab-147">NOTES</span></span>

## <span data-ttu-id="944ab-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="944ab-148">RELATED LINKS</span></span>
