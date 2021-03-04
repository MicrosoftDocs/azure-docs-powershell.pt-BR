---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/remove-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeShare.md
ms.openlocfilehash: 93229e52c81c544704bb5195ce54480f03fa825b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892294"
---
# <span data-ttu-id="48a14-101">Remove-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="48a14-101">Remove-AzStackEdgeShare</span></span>

## <span data-ttu-id="48a14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48a14-102">SYNOPSIS</span></span>
<span data-ttu-id="48a14-103">Remove um compartilhamento do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="48a14-103">Removes a share from the device.</span></span>

## <span data-ttu-id="48a14-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="48a14-104">SYNTAX</span></span>

### <span data-ttu-id="48a14-105">DeleteByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="48a14-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48a14-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="48a14-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeShare [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48a14-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="48a14-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeShare [-InputObject] <PSStackEdgeShare> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48a14-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="48a14-108">DESCRIPTION</span></span>
<span data-ttu-id="48a14-109">O cmdlet **Remove-AzStackEdgeEdgeShare** remove os compartilhamentos de borda associados para um dispositivo de Borda de Pilha.</span><span class="sxs-lookup"><span data-stu-id="48a14-109">The **Remove-AzStackEdgeEdgeShare** cmdlet removes the associated edge shares for a Stack Edge device.</span></span>

## <span data-ttu-id="48a14-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="48a14-110">EXAMPLES</span></span>

### <span data-ttu-id="48a14-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="48a14-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name shareName
```

## <span data-ttu-id="48a14-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="48a14-112">PARAMETERS</span></span>

### <span data-ttu-id="48a14-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="48a14-113">-AsJob</span></span>
<span data-ttu-id="48a14-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="48a14-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="48a14-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48a14-115">-DefaultProfile</span></span>
<span data-ttu-id="48a14-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="48a14-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48a14-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="48a14-117">-DeviceName</span></span>
<span data-ttu-id="48a14-118">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="48a14-118">Device Name</span></span>

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

### <span data-ttu-id="48a14-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48a14-119">-InputObject</span></span>
<span data-ttu-id="48a14-120">Objeto Input</span><span class="sxs-lookup"><span data-stu-id="48a14-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: EdgeShare

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="48a14-121">-Name</span><span class="sxs-lookup"><span data-stu-id="48a14-121">-Name</span></span>
<span data-ttu-id="48a14-122">Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="48a14-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: EdgeShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48a14-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="48a14-123">-PassThru</span></span>
<span data-ttu-id="48a14-124">retorna true se bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="48a14-124">returns true if successful</span></span>

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

### <span data-ttu-id="48a14-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48a14-125">-ResourceGroupName</span></span>
<span data-ttu-id="48a14-126">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="48a14-126">Resource Group Name</span></span>

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

### <span data-ttu-id="48a14-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="48a14-127">-ResourceId</span></span>
<span data-ttu-id="48a14-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="48a14-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="48a14-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="48a14-129">-Confirm</span></span>
<span data-ttu-id="48a14-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48a14-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48a14-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48a14-131">-WhatIf</span></span>
<span data-ttu-id="48a14-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="48a14-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="48a14-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="48a14-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48a14-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48a14-134">CommonParameters</span></span>
<span data-ttu-id="48a14-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48a14-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48a14-136">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="48a14-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48a14-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="48a14-137">INPUTS</span></span>

### <span data-ttu-id="48a14-138">System.String</span><span class="sxs-lookup"><span data-stu-id="48a14-138">System.String</span></span>

### <span data-ttu-id="48a14-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="48a14-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="48a14-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="48a14-140">OUTPUTS</span></span>

### <span data-ttu-id="48a14-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="48a14-141">System.Boolean</span></span>

## <span data-ttu-id="48a14-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="48a14-142">NOTES</span></span>

## <span data-ttu-id="48a14-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="48a14-143">RELATED LINKS</span></span>
