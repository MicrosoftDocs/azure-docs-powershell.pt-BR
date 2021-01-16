---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/invoke-azstackedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeStorageContainer.md
ms.openlocfilehash: d7e8c65a54adae1de7b7f3ba1ed2d67139638846
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261753"
---
# <span data-ttu-id="6b426-101">Invoke-AzStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="6b426-101">Invoke-AzStackEdgeStorageContainer</span></span>

## <span data-ttu-id="6b426-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6b426-102">SYNOPSIS</span></span>
<span data-ttu-id="6b426-103">Invoca ações específicas em um contêiner de armazenamento</span><span class="sxs-lookup"><span data-stu-id="6b426-103">Invokes specific actions on a storage container</span></span>

## <span data-ttu-id="6b426-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6b426-104">SYNTAX</span></span>

### <span data-ttu-id="6b426-105">InvokeByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="6b426-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-RefreshData] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b426-106">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b426-106">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeStorageContainer [-ResourceId] <String> [-RefreshData] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b426-107">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b426-107">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzStackEdgeStorageContainer [-RefreshData] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 -InputObject <PSStackEdgeStorageContainer> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b426-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6b426-108">DESCRIPTION</span></span>
<span data-ttu-id="6b426-109">O cmdlet **Invoke-AzStackEdgeStorageContainer** invoca ações para atualizar os dados em um contêiner de armazenamento em um dispositivo de borda de pilha.</span><span class="sxs-lookup"><span data-stu-id="6b426-109">The **Invoke-AzStackEdgeStorageContainer** cmdlet invokes actions to refresh the data on a storage container on a Stack Edge device.</span></span> 

## <span data-ttu-id="6b426-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6b426-110">EXAMPLES</span></span>

### <span data-ttu-id="6b426-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6b426-111">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccount1 -Name container1 -PassThru
PS C:\> true
```

### <span data-ttu-id="6b426-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="6b426-112">Example 2</span></span>
```powershell
PS C:\> Get-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccount1 -Name container1 | Invoke-AzStackEdgeStorageContainer
```

## <span data-ttu-id="6b426-113">OS</span><span class="sxs-lookup"><span data-stu-id="6b426-113">PARAMETERS</span></span>

### <span data-ttu-id="6b426-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6b426-114">-AsJob</span></span>
<span data-ttu-id="6b426-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="6b426-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6b426-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b426-116">-DefaultProfile</span></span>
<span data-ttu-id="6b426-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6b426-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b426-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="6b426-118">-DeviceName</span></span>
<span data-ttu-id="6b426-119">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="6b426-119">Device Name</span></span>

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

### <span data-ttu-id="6b426-120">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="6b426-120">-EdgeStorageAccountName</span></span>
<span data-ttu-id="6b426-121">Nome do recurso</span><span class="sxs-lookup"><span data-stu-id="6b426-121">Resource Name</span></span>

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

### <span data-ttu-id="6b426-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6b426-122">-InputObject</span></span>
<span data-ttu-id="6b426-123">Fornecer objeto EdgeStorageAccount existente</span><span class="sxs-lookup"><span data-stu-id="6b426-123">Provide existing EdgeStorageAccount Object</span></span>

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

### <span data-ttu-id="6b426-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="6b426-124">-Name</span></span>
<span data-ttu-id="6b426-125">Nome do recurso</span><span class="sxs-lookup"><span data-stu-id="6b426-125">Resource Name</span></span>

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

### <span data-ttu-id="6b426-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6b426-126">-PassThru</span></span>
<span data-ttu-id="6b426-127">Retorna verdadeiro se bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="6b426-127">returns true if successful</span></span>

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

### <span data-ttu-id="6b426-128">-RefreshData</span><span class="sxs-lookup"><span data-stu-id="6b426-128">-RefreshData</span></span>
<span data-ttu-id="6b426-129">Atualizar metadados de contêiner com os dados da nuvem</span><span class="sxs-lookup"><span data-stu-id="6b426-129">Refresh Container Metadata with the data from the cloud</span></span>

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

### <span data-ttu-id="6b426-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b426-130">-ResourceGroupName</span></span>
<span data-ttu-id="6b426-131">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="6b426-131">Resource Group Name</span></span>

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

### <span data-ttu-id="6b426-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6b426-132">-ResourceId</span></span>
<span data-ttu-id="6b426-133">ResourceId do Azure</span><span class="sxs-lookup"><span data-stu-id="6b426-133">Azure ResourceId</span></span>

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

### <span data-ttu-id="6b426-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6b426-134">-Confirm</span></span>
<span data-ttu-id="6b426-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b426-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b426-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b426-136">-WhatIf</span></span>
<span data-ttu-id="6b426-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6b426-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6b426-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6b426-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b426-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b426-139">CommonParameters</span></span>
<span data-ttu-id="6b426-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b426-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b426-141">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6b426-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b426-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6b426-142">INPUTS</span></span>

### <span data-ttu-id="6b426-143">System. String</span><span class="sxs-lookup"><span data-stu-id="6b426-143">System.String</span></span>

### <span data-ttu-id="6b426-144">Microsoft. Azure. PowerShell. cmdlets. StackEdge. Models. PSStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="6b426-144">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="6b426-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6b426-145">OUTPUTS</span></span>

### <span data-ttu-id="6b426-146">Microsoft. Azure. PowerShell. cmdlets. StackEdge. Models. PSStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="6b426-146">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="6b426-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6b426-147">NOTES</span></span>

## <span data-ttu-id="6b426-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6b426-148">RELATED LINKS</span></span>
