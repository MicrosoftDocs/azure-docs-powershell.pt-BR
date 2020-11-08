---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/invoke-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeShare.md
ms.openlocfilehash: c3fa71b6fb54f359f035f4f6c2f18789ff24b3ac
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114184"
---
# <span data-ttu-id="736a8-101">Invoke-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="736a8-101">Invoke-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="736a8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="736a8-102">SYNOPSIS</span></span>
<span data-ttu-id="736a8-103">Invoca ações específicas em um compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="736a8-103">Invokes specific actions on a share.</span></span>

## <span data-ttu-id="736a8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="736a8-104">SYNTAX</span></span>

### <span data-ttu-id="736a8-105">InvokeByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="736a8-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-RefreshData] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="736a8-106">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="736a8-106">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeShare -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-RefreshData] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="736a8-107">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="736a8-107">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeShare [-AsJob] [-DefaultProfile <IAzureContextContainer>] -InputObject <PSDataBoxEdgeShare>
 [-RefreshData] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="736a8-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="736a8-108">DESCRIPTION</span></span>
<span data-ttu-id="736a8-109">O cmdlet **Invoke-AzDataBoxEdgeShare** invoca uma ação para atualizar dados em um compartilhamento em um dispositivo de borda de caixa de dados.</span><span class="sxs-lookup"><span data-stu-id="736a8-109">The **Invoke-AzDataBoxEdgeShare** cmdlet invokes action to refresh data on a share on a Data Box Edge device.</span></span>

## <span data-ttu-id="736a8-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="736a8-110">EXAMPLES</span></span>

### <span data-ttu-id="736a8-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="736a8-111">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share1 -PassThru
PS C:\> true
```

### <span data-ttu-id="736a8-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="736a8-112">Example 2</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share1 | Invoke-AzDataBoxEdgeShare
```

## <span data-ttu-id="736a8-113">OS</span><span class="sxs-lookup"><span data-stu-id="736a8-113">PARAMETERS</span></span>

### <span data-ttu-id="736a8-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="736a8-114">-AsJob</span></span>
<span data-ttu-id="736a8-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="736a8-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="736a8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="736a8-116">-DefaultProfile</span></span>
<span data-ttu-id="736a8-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="736a8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="736a8-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="736a8-118">-DeviceName</span></span>
<span data-ttu-id="736a8-119">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="736a8-119">Device Name</span></span>

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

### <span data-ttu-id="736a8-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="736a8-120">-InputObject</span></span>
<span data-ttu-id="736a8-121">Objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="736a8-121">Input Object</span></span>

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

### <span data-ttu-id="736a8-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="736a8-122">-Name</span></span>
<span data-ttu-id="736a8-123">Nome do recurso</span><span class="sxs-lookup"><span data-stu-id="736a8-123">Resource Name</span></span>

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

### <span data-ttu-id="736a8-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="736a8-124">-PassThru</span></span>
<span data-ttu-id="736a8-125">Retorna verdadeiro se bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="736a8-125">returns true if successful</span></span>

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

### <span data-ttu-id="736a8-126">-RefreshData</span><span class="sxs-lookup"><span data-stu-id="736a8-126">-RefreshData</span></span>
<span data-ttu-id="736a8-127">Atualizar metadados de compartilhamento com os dados da nuvem</span><span class="sxs-lookup"><span data-stu-id="736a8-127">Refresh Share Metadata with the data from the cloud</span></span>

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

### <span data-ttu-id="736a8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="736a8-128">-ResourceGroupName</span></span>
<span data-ttu-id="736a8-129">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="736a8-129">Resource Group Name</span></span>

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

### <span data-ttu-id="736a8-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="736a8-130">-ResourceId</span></span>
<span data-ttu-id="736a8-131">ResourceId do Azure</span><span class="sxs-lookup"><span data-stu-id="736a8-131">Azure ResourceId</span></span>

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

### <span data-ttu-id="736a8-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="736a8-132">-Confirm</span></span>
<span data-ttu-id="736a8-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="736a8-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="736a8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="736a8-134">-WhatIf</span></span>
<span data-ttu-id="736a8-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="736a8-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="736a8-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="736a8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="736a8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="736a8-137">CommonParameters</span></span>
<span data-ttu-id="736a8-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="736a8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="736a8-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="736a8-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="736a8-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="736a8-140">INPUTS</span></span>

### <span data-ttu-id="736a8-141">System. String</span><span class="sxs-lookup"><span data-stu-id="736a8-141">System.String</span></span>

### <span data-ttu-id="736a8-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="736a8-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="736a8-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="736a8-143">OUTPUTS</span></span>

### <span data-ttu-id="736a8-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="736a8-144">System.Boolean</span></span>

## <span data-ttu-id="736a8-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="736a8-145">NOTES</span></span>

## <span data-ttu-id="736a8-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="736a8-146">RELATED LINKS</span></span>
