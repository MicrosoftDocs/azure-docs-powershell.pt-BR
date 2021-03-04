---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/invoke-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeShare.md
ms.openlocfilehash: fc920e04ce3e031e25b0c27ec0998266f077840c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892020"
---
# <span data-ttu-id="6088c-101">Invoke-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="6088c-101">Invoke-AzStackEdgeShare</span></span>

## <span data-ttu-id="6088c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6088c-102">SYNOPSIS</span></span>
<span data-ttu-id="6088c-103">Invoca ações específicas em um compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="6088c-103">Invokes specific actions on a share.</span></span>

## <span data-ttu-id="6088c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6088c-104">SYNTAX</span></span>

### <span data-ttu-id="6088c-105">InvokeByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6088c-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-RefreshData] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6088c-106">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6088c-106">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeShare -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-RefreshData]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6088c-107">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6088c-107">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzStackEdgeShare [-AsJob] [-DefaultProfile <IAzureContextContainer>] -InputObject <PSStackEdgeShare>
 [-RefreshData] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6088c-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6088c-108">DESCRIPTION</span></span>
<span data-ttu-id="6088c-109">O cmdlet **Invoke-AzStackEdgeShare** invoca a ação para atualizar dados em um compartilhamento em um dispositivo de Borda de Pilha.</span><span class="sxs-lookup"><span data-stu-id="6088c-109">The **Invoke-AzStackEdgeShare** cmdlet invokes action to refresh data on a share on a Stack Edge device.</span></span>

## <span data-ttu-id="6088c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6088c-110">EXAMPLES</span></span>

### <span data-ttu-id="6088c-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6088c-111">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share1 -PassThru
PS C:\> true
```

### <span data-ttu-id="6088c-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="6088c-112">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share1 | Invoke-AzStackEdgeShare
```

## <span data-ttu-id="6088c-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6088c-113">PARAMETERS</span></span>

### <span data-ttu-id="6088c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6088c-114">-AsJob</span></span>
<span data-ttu-id="6088c-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="6088c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6088c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6088c-116">-DefaultProfile</span></span>
<span data-ttu-id="6088c-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6088c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6088c-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="6088c-118">-DeviceName</span></span>
<span data-ttu-id="6088c-119">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="6088c-119">Device Name</span></span>

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

### <span data-ttu-id="6088c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6088c-120">-InputObject</span></span>
<span data-ttu-id="6088c-121">Objeto Input</span><span class="sxs-lookup"><span data-stu-id="6088c-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare
Parameter Sets: InvokeByInputObjectParameterSet
Aliases: EdgeShare

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6088c-122">-Name</span><span class="sxs-lookup"><span data-stu-id="6088c-122">-Name</span></span>
<span data-ttu-id="6088c-123">Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="6088c-123">Resource Name</span></span>

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

### <span data-ttu-id="6088c-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6088c-124">-PassThru</span></span>
<span data-ttu-id="6088c-125">retorna true se bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="6088c-125">returns true if successful</span></span>

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

### <span data-ttu-id="6088c-126">-RefreshData</span><span class="sxs-lookup"><span data-stu-id="6088c-126">-RefreshData</span></span>
<span data-ttu-id="6088c-127">Atualizar Metadados do Compartilhamento com os dados da nuvem</span><span class="sxs-lookup"><span data-stu-id="6088c-127">Refresh Share Metadata with the data from the cloud</span></span>

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

### <span data-ttu-id="6088c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6088c-128">-ResourceGroupName</span></span>
<span data-ttu-id="6088c-129">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="6088c-129">Resource Group Name</span></span>

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

### <span data-ttu-id="6088c-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6088c-130">-ResourceId</span></span>
<span data-ttu-id="6088c-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="6088c-131">Azure ResourceId</span></span>

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

### <span data-ttu-id="6088c-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6088c-132">-Confirm</span></span>
<span data-ttu-id="6088c-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6088c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6088c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6088c-134">-WhatIf</span></span>
<span data-ttu-id="6088c-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6088c-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6088c-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6088c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6088c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6088c-137">CommonParameters</span></span>
<span data-ttu-id="6088c-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6088c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6088c-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6088c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6088c-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6088c-140">INPUTS</span></span>

### <span data-ttu-id="6088c-141">System.String</span><span class="sxs-lookup"><span data-stu-id="6088c-141">System.String</span></span>

### <span data-ttu-id="6088c-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="6088c-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="6088c-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6088c-143">OUTPUTS</span></span>

### <span data-ttu-id="6088c-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6088c-144">System.Boolean</span></span>

## <span data-ttu-id="6088c-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="6088c-145">NOTES</span></span>

## <span data-ttu-id="6088c-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6088c-146">RELATED LINKS</span></span>
