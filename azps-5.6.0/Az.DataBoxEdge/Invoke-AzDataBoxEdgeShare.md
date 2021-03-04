---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/invoke-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeShare.md
ms.openlocfilehash: a135a9bf994e2837351347a4cc741ed20b406a28
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891855"
---
# <span data-ttu-id="35791-101">Invoke-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="35791-101">Invoke-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="35791-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35791-102">SYNOPSIS</span></span>
<span data-ttu-id="35791-103">Invoca ações específicas em um compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="35791-103">Invokes specific actions on a share.</span></span>

## <span data-ttu-id="35791-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="35791-104">SYNTAX</span></span>

### <span data-ttu-id="35791-105">InvokeByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="35791-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-RefreshData] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="35791-106">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="35791-106">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeShare -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-RefreshData] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35791-107">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="35791-107">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeShare [-AsJob] [-DefaultProfile <IAzureContextContainer>] -InputObject <PSDataBoxEdgeShare>
 [-RefreshData] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35791-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="35791-108">DESCRIPTION</span></span>
<span data-ttu-id="35791-109">O cmdlet **Invoke-AzDataBoxEdgeShare** invoca a ação para atualizar dados em um compartilhamento em um dispositivo de Borda da Caixa de Dados.</span><span class="sxs-lookup"><span data-stu-id="35791-109">The **Invoke-AzDataBoxEdgeShare** cmdlet invokes action to refresh data on a share on a Data Box Edge device.</span></span>

## <span data-ttu-id="35791-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="35791-110">EXAMPLES</span></span>

### <span data-ttu-id="35791-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="35791-111">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share1 -PassThru
PS C:\> true
```

### <span data-ttu-id="35791-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="35791-112">Example 2</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share1 | Invoke-AzDataBoxEdgeShare
```

## <span data-ttu-id="35791-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="35791-113">PARAMETERS</span></span>

### <span data-ttu-id="35791-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="35791-114">-AsJob</span></span>
<span data-ttu-id="35791-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="35791-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="35791-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35791-116">-DefaultProfile</span></span>
<span data-ttu-id="35791-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="35791-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35791-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="35791-118">-DeviceName</span></span>
<span data-ttu-id="35791-119">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="35791-119">Device Name</span></span>

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

### <span data-ttu-id="35791-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35791-120">-InputObject</span></span>
<span data-ttu-id="35791-121">Objeto Input</span><span class="sxs-lookup"><span data-stu-id="35791-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare
Parameter Sets: InvokeByInputObjectParameterSet
Aliases: EdgeShare

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35791-122">-Name</span><span class="sxs-lookup"><span data-stu-id="35791-122">-Name</span></span>
<span data-ttu-id="35791-123">Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="35791-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases: EdgeShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35791-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="35791-124">-PassThru</span></span>
<span data-ttu-id="35791-125">retorna true se bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="35791-125">returns true if successful</span></span>

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

### <span data-ttu-id="35791-126">-RefreshData</span><span class="sxs-lookup"><span data-stu-id="35791-126">-RefreshData</span></span>
<span data-ttu-id="35791-127">Atualizar Metadados do Compartilhamento com os dados da nuvem</span><span class="sxs-lookup"><span data-stu-id="35791-127">Refresh Share Metadata with the data from the cloud</span></span>

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

### <span data-ttu-id="35791-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35791-128">-ResourceGroupName</span></span>
<span data-ttu-id="35791-129">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="35791-129">Resource Group Name</span></span>

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

### <span data-ttu-id="35791-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="35791-130">-ResourceId</span></span>
<span data-ttu-id="35791-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="35791-131">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35791-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="35791-132">-Confirm</span></span>
<span data-ttu-id="35791-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35791-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35791-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35791-134">-WhatIf</span></span>
<span data-ttu-id="35791-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="35791-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="35791-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="35791-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35791-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35791-137">CommonParameters</span></span>
<span data-ttu-id="35791-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35791-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35791-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="35791-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35791-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="35791-140">INPUTS</span></span>

### <span data-ttu-id="35791-141">System.String</span><span class="sxs-lookup"><span data-stu-id="35791-141">System.String</span></span>

### <span data-ttu-id="35791-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="35791-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="35791-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="35791-143">OUTPUTS</span></span>

### <span data-ttu-id="35791-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="35791-144">System.Boolean</span></span>

## <span data-ttu-id="35791-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="35791-145">NOTES</span></span>

## <span data-ttu-id="35791-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="35791-146">RELATED LINKS</span></span>
