---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHostGroup.md
ms.openlocfilehash: f05855c7fa677c384e9d8d0c5385d6014d80d312
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889299"
---
# <span data-ttu-id="75b24-101">Remove-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="75b24-101">Remove-AzHostGroup</span></span>

## <span data-ttu-id="75b24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75b24-102">SYNOPSIS</span></span>
<span data-ttu-id="75b24-103">Remove um grupo de host.</span><span class="sxs-lookup"><span data-stu-id="75b24-103">Removes a host group.</span></span>

## <span data-ttu-id="75b24-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="75b24-104">SYNTAX</span></span>

### <span data-ttu-id="75b24-105">DefaultParameter (Padrão)</span><span class="sxs-lookup"><span data-stu-id="75b24-105">DefaultParameter (Default)</span></span>
```
Remove-AzHostGroup [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75b24-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="75b24-106">ResourceIdParameter</span></span>
```
Remove-AzHostGroup [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75b24-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="75b24-107">ObjectParameter</span></span>
```
Remove-AzHostGroup [-InputObject] <PSHostGroup> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75b24-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="75b24-108">DESCRIPTION</span></span>
<span data-ttu-id="75b24-109">Este cmdlet excluirá um grupo host</span><span class="sxs-lookup"><span data-stu-id="75b24-109">This cmdlet will delete a Host group</span></span>

## <span data-ttu-id="75b24-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="75b24-110">EXAMPLES</span></span>

### <span data-ttu-id="75b24-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="75b24-111">Example 1</span></span>
```
PS C:\> Get-AzHostGroup -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName | Remove-AzHostGroup
```

<span data-ttu-id="75b24-112">Este comando obtém e remove o grupo de host determinado.</span><span class="sxs-lookup"><span data-stu-id="75b24-112">This command gets and removes the given host group.</span></span>

### <span data-ttu-id="75b24-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="75b24-113">Example 2</span></span>
```
PS C:\> Remove-AzHostGroup -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName
```

<span data-ttu-id="75b24-114">Este comando remove o grupo de host determinado.</span><span class="sxs-lookup"><span data-stu-id="75b24-114">This command removes the given host group.</span></span>

## <span data-ttu-id="75b24-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="75b24-115">PARAMETERS</span></span>

### <span data-ttu-id="75b24-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="75b24-116">-AsJob</span></span>
<span data-ttu-id="75b24-117">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="75b24-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="75b24-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75b24-118">-DefaultProfile</span></span>
<span data-ttu-id="75b24-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="75b24-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75b24-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="75b24-120">-InputObject</span></span>
<span data-ttu-id="75b24-121">O objeto local do grupo host.</span><span class="sxs-lookup"><span data-stu-id="75b24-121">The local object of the host group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup
Parameter Sets: ObjectParameter
Aliases: HostGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75b24-122">-Name</span><span class="sxs-lookup"><span data-stu-id="75b24-122">-Name</span></span>
<span data-ttu-id="75b24-123">O nome do grupo host.</span><span class="sxs-lookup"><span data-stu-id="75b24-123">The name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: HostGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75b24-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75b24-124">-ResourceGroupName</span></span>
<span data-ttu-id="75b24-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="75b24-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75b24-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="75b24-126">-ResourceId</span></span>
<span data-ttu-id="75b24-127">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="75b24-127">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75b24-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="75b24-128">-Confirm</span></span>
<span data-ttu-id="75b24-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75b24-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75b24-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75b24-130">-WhatIf</span></span>
<span data-ttu-id="75b24-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="75b24-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75b24-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="75b24-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75b24-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75b24-133">CommonParameters</span></span>
<span data-ttu-id="75b24-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75b24-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75b24-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="75b24-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75b24-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="75b24-136">INPUTS</span></span>

### <span data-ttu-id="75b24-137">System.String</span><span class="sxs-lookup"><span data-stu-id="75b24-137">System.String</span></span>

### <span data-ttu-id="75b24-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="75b24-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="75b24-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="75b24-139">OUTPUTS</span></span>

### <span data-ttu-id="75b24-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="75b24-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="75b24-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="75b24-141">NOTES</span></span>

## <span data-ttu-id="75b24-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="75b24-142">RELATED LINKS</span></span>
