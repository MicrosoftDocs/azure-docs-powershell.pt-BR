---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/suspend-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Suspend-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Suspend-AzKustoCluster.md
ms.openlocfilehash: 17c730fb65e50aeeff33e616b7be596745d67ac0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941122"
---
# <span data-ttu-id="bb3f5-101">Suspend-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="bb3f5-101">Suspend-AzKustoCluster</span></span>

## <span data-ttu-id="bb3f5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bb3f5-102">SYNOPSIS</span></span>
<span data-ttu-id="bb3f5-103">Suspender um cluster existente do Kusto.</span><span class="sxs-lookup"><span data-stu-id="bb3f5-103">Suspend an existing Kusto cluster.</span></span>

## <span data-ttu-id="bb3f5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bb3f5-104">SYNTAX</span></span>

### <span data-ttu-id="bb3f5-105">ByNameAndResourceGroup (padrão)</span><span class="sxs-lookup"><span data-stu-id="bb3f5-105">ByNameAndResourceGroup (Default)</span></span>
```
Suspend-AzKustoCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb3f5-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="bb3f5-106">ByResourceId</span></span>
```
Suspend-AzKustoCluster [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb3f5-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="bb3f5-107">ByInputObject</span></span>
```
Suspend-AzKustoCluster [-InputObject] <PSKustoCluster> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb3f5-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bb3f5-108">DESCRIPTION</span></span>
<span data-ttu-id="bb3f5-109">Suspender um cluster existente do Kusto.</span><span class="sxs-lookup"><span data-stu-id="bb3f5-109">Suspend an existing Kusto cluster.</span></span>

## <span data-ttu-id="bb3f5-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bb3f5-110">EXAMPLES</span></span>

### <span data-ttu-id="bb3f5-111">Exemplo 1-suspender um cluster existente do Kusto por nome</span><span class="sxs-lookup"><span data-stu-id="bb3f5-111">Example 1 - Suspend an existing Kusto cluster by name</span></span>

```
PS C:\> Suspend-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster
```

<span data-ttu-id="bb3f5-112">O comando acima suspende o cluster Kusto chamado "mykustocluster" localizado no grupo de recursos "testrg".</span><span class="sxs-lookup"><span data-stu-id="bb3f5-112">The above command suspends the Kusto cluster named "mykustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="bb3f5-113">Exemplo 2-suspender um cluster de Kusto existente por tubulação</span><span class="sxs-lookup"><span data-stu-id="bb3f5-113">Example 2 - Suspend an existing Kusto cluster by piping</span></span>

```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster | Suspend-AzKustoCluster
```

<span data-ttu-id="bb3f5-114">O comando acima Obtém o cluster Kusto chamado "mykustocluster" localizado no grupo de recursos "testrg" usando o `Get-AzKustoCluster` cmdlet e, em seguida, canaliza o resultado para `Suspend-AzKustoCluster` suspendê-lo.</span><span class="sxs-lookup"><span data-stu-id="bb3f5-114">The above command gets the Kusto cluster named "mykustocluster" found in the resource group "testrg" using the `Get-AzKustoCluster` cmdlet, and then pipes the result to `Suspend-AzKustoCluster` to suspend it.</span></span>

## <span data-ttu-id="bb3f5-115">OS</span><span class="sxs-lookup"><span data-stu-id="bb3f5-115">PARAMETERS</span></span>

### <span data-ttu-id="bb3f5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb3f5-116">-DefaultProfile</span></span>
<span data-ttu-id="bb3f5-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bb3f5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb3f5-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bb3f5-118">-InputObject</span></span>
<span data-ttu-id="bb3f5-119">Objeto de cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="bb3f5-119">Kusto cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bb3f5-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="bb3f5-120">-Name</span></span>
<span data-ttu-id="bb3f5-121">Nome do cluster a ser suspenso.</span><span class="sxs-lookup"><span data-stu-id="bb3f5-121">Name of cluster to be suspend.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb3f5-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bb3f5-122">-PassThru</span></span>
<span data-ttu-id="bb3f5-123">Retorne se o cluster especificado foi suspenso ou não com êxito.</span><span class="sxs-lookup"><span data-stu-id="bb3f5-123">Return whether the specified cluster was successfully suspended or not.</span></span>

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

### <span data-ttu-id="bb3f5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb3f5-124">-ResourceGroupName</span></span>
<span data-ttu-id="bb3f5-125">Nome do grupo de recursos sob o qual o cluster existe.</span><span class="sxs-lookup"><span data-stu-id="bb3f5-125">Name of resource group under which the cluster exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb3f5-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bb3f5-126">-ResourceId</span></span>
<span data-ttu-id="bb3f5-127">ResourceId do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="bb3f5-127">Kusto cluster ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb3f5-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bb3f5-128">-Confirm</span></span>
<span data-ttu-id="bb3f5-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb3f5-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb3f5-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb3f5-130">-WhatIf</span></span>
<span data-ttu-id="bb3f5-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bb3f5-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb3f5-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bb3f5-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb3f5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb3f5-133">CommonParameters</span></span>
<span data-ttu-id="bb3f5-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb3f5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb3f5-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb3f5-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb3f5-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bb3f5-136">INPUTS</span></span>

### <span data-ttu-id="bb3f5-137">System. String</span><span class="sxs-lookup"><span data-stu-id="bb3f5-137">System.String</span></span>

### <span data-ttu-id="bb3f5-138">Microsoft. Azure. Commands. Kusto. Models. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="bb3f5-138">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="bb3f5-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bb3f5-139">OUTPUTS</span></span>

### <span data-ttu-id="bb3f5-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bb3f5-140">System.Boolean</span></span>

## <span data-ttu-id="bb3f5-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bb3f5-141">NOTES</span></span>

## <span data-ttu-id="bb3f5-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bb3f5-142">RELATED LINKS</span></span>
