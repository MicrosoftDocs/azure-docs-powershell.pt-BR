---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHost.md
ms.openlocfilehash: 21c623187e72406d1120e225bf567a48bb2e6f30
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889300"
---
# <span data-ttu-id="9b848-101">Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="9b848-101">Remove-AzHost</span></span>

## <span data-ttu-id="9b848-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b848-102">SYNOPSIS</span></span>
<span data-ttu-id="9b848-103">Remove um host.</span><span class="sxs-lookup"><span data-stu-id="9b848-103">Removes a host.</span></span>

## <span data-ttu-id="9b848-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9b848-104">SYNTAX</span></span>

### <span data-ttu-id="9b848-105">DefaultParameter (Padrão)</span><span class="sxs-lookup"><span data-stu-id="9b848-105">DefaultParameter (Default)</span></span>
```
Remove-AzHost [-ResourceGroupName] <String> [-HostGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b848-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="9b848-106">ResourceIdParameter</span></span>
```
Remove-AzHost [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9b848-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="9b848-107">ObjectParameter</span></span>
```
Remove-AzHost [-InputObject] <PSHost> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9b848-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9b848-108">DESCRIPTION</span></span>
<span data-ttu-id="9b848-109">Este cmdlet excluirá um Host</span><span class="sxs-lookup"><span data-stu-id="9b848-109">This cmdlet will delete a Host</span></span>

## <span data-ttu-id="9b848-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9b848-110">EXAMPLES</span></span>

### <span data-ttu-id="9b848-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9b848-111">Example 1</span></span>
```
PS C:\> Get-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName | Remove-AzHost
```

<span data-ttu-id="9b848-112">Este comando obtém e remove o host determinado.</span><span class="sxs-lookup"><span data-stu-id="9b848-112">This command gets and removes the given host.</span></span>

### <span data-ttu-id="9b848-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="9b848-113">Example 2</span></span>
```
PS C:\> Remove-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName
```

<span data-ttu-id="9b848-114">Este comando remove o host determinado.</span><span class="sxs-lookup"><span data-stu-id="9b848-114">This command removes the given host.</span></span>

## <span data-ttu-id="9b848-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9b848-115">PARAMETERS</span></span>

### <span data-ttu-id="9b848-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9b848-116">-AsJob</span></span>
<span data-ttu-id="9b848-117">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="9b848-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9b848-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b848-118">-DefaultProfile</span></span>
<span data-ttu-id="9b848-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9b848-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b848-120">-HostGroupName</span><span class="sxs-lookup"><span data-stu-id="9b848-120">-HostGroupName</span></span>
<span data-ttu-id="9b848-121">O nome do grupo host.</span><span class="sxs-lookup"><span data-stu-id="9b848-121">The name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b848-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9b848-122">-InputObject</span></span>
<span data-ttu-id="9b848-123">O objeto local do host.</span><span class="sxs-lookup"><span data-stu-id="9b848-123">The local object of the host.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSHost
Parameter Sets: ObjectParameter
Aliases: Host

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b848-124">-Name</span><span class="sxs-lookup"><span data-stu-id="9b848-124">-Name</span></span>
<span data-ttu-id="9b848-125">O nome do host.</span><span class="sxs-lookup"><span data-stu-id="9b848-125">The name of the host.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: HostName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b848-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b848-126">-ResourceGroupName</span></span>
<span data-ttu-id="9b848-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9b848-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="9b848-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9b848-128">-ResourceId</span></span>
<span data-ttu-id="9b848-129">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="9b848-129">The ID of the resource.</span></span>

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

### <span data-ttu-id="9b848-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9b848-130">-Confirm</span></span>
<span data-ttu-id="9b848-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b848-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b848-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b848-132">-WhatIf</span></span>
<span data-ttu-id="9b848-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9b848-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b848-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9b848-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b848-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b848-135">CommonParameters</span></span>
<span data-ttu-id="9b848-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b848-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b848-137">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9b848-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b848-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9b848-138">INPUTS</span></span>

### <span data-ttu-id="9b848-139">System.String</span><span class="sxs-lookup"><span data-stu-id="9b848-139">System.String</span></span>

### <span data-ttu-id="9b848-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span><span class="sxs-lookup"><span data-stu-id="9b848-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span></span>

## <span data-ttu-id="9b848-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9b848-141">OUTPUTS</span></span>

### <span data-ttu-id="9b848-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="9b848-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="9b848-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="9b848-143">NOTES</span></span>

## <span data-ttu-id="9b848-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9b848-144">RELATED LINKS</span></span>
