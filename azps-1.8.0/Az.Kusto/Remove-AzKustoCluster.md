---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Remove-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Remove-AzKustoCluster.md
ms.openlocfilehash: 3556ff99dafe804ab78899f8b0eefc64db4ca82b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770568"
---
# <span data-ttu-id="b491c-101">Remove-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="b491c-101">Remove-AzKustoCluster</span></span>

## <span data-ttu-id="b491c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b491c-102">SYNOPSIS</span></span>
<span data-ttu-id="b491c-103">Exclui um cluster Kusto existente.</span><span class="sxs-lookup"><span data-stu-id="b491c-103">Deletes an existing Kusto cluster.</span></span>

## <span data-ttu-id="b491c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b491c-104">SYNTAX</span></span>

### <span data-ttu-id="b491c-105">ByNameAndResourceGroup (padrão)</span><span class="sxs-lookup"><span data-stu-id="b491c-105">ByNameAndResourceGroup (Default)</span></span>
```
Remove-AzKustoCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b491c-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b491c-106">ByResourceId</span></span>
```
Remove-AzKustoCluster [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b491c-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b491c-107">ByInputObject</span></span>
```
Remove-AzKustoCluster [-InputObject] <PSKustoCluster> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b491c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b491c-108">DESCRIPTION</span></span>
<span data-ttu-id="b491c-109">Exclui um cluster Kusto existente.</span><span class="sxs-lookup"><span data-stu-id="b491c-109">Deletes an existing Kusto cluster.</span></span>

## <span data-ttu-id="b491c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b491c-110">EXAMPLES</span></span>

### <span data-ttu-id="b491c-111">Exemplo 1-excluir um cluster existente do Kusto por nome</span><span class="sxs-lookup"><span data-stu-id="b491c-111">Example 1 - Delete an existing Kusto cluster by name</span></span>

```
PS C:\> Remove-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster
```

<span data-ttu-id="b491c-112">O comando acima exclui o cluster Kusto chamado "mykustocluster" no grupo de recursos "testrg".</span><span class="sxs-lookup"><span data-stu-id="b491c-112">The above command deletes the Kusto cluster named "mykustocluster" in the resource group "testrg".</span></span>

### <span data-ttu-id="b491c-113">Exemplo 2-excluir um cluster de Kusto existente por tubulação</span><span class="sxs-lookup"><span data-stu-id="b491c-113">Example 2 - Delete an existing Kusto cluster by piping</span></span>

```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster | Remove-AzKustoCluster
```

<span data-ttu-id="b491c-114">O comando acima Obtém o cluster Kusto chamado "mykustocluster" no grupo de recursos "testrg" usando o `Get-AzKustoCluster` cmdlet e, em seguida, canaliza o resultado para `Remove-AzKustoCluster` excluí-lo.</span><span class="sxs-lookup"><span data-stu-id="b491c-114">The above command gets the Kusto cluster named "mykustocluster" in the resource group "testrg" using the `Get-AzKustoCluster` cmdlet, and then pipes the result to `Remove-AzKustoCluster` to delete it.</span></span>

## <span data-ttu-id="b491c-115">OS</span><span class="sxs-lookup"><span data-stu-id="b491c-115">PARAMETERS</span></span>

### <span data-ttu-id="b491c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b491c-116">-DefaultProfile</span></span>
<span data-ttu-id="b491c-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b491c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b491c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b491c-118">-InputObject</span></span>
<span data-ttu-id="b491c-119">Objeto de cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="b491c-119">Kusto cluster object.</span></span>

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

### <span data-ttu-id="b491c-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="b491c-120">-Name</span></span>
<span data-ttu-id="b491c-121">Nome do cluster a ser removido.</span><span class="sxs-lookup"><span data-stu-id="b491c-121">Name of cluster to be removed.</span></span>

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

### <span data-ttu-id="b491c-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b491c-122">-PassThru</span></span>
<span data-ttu-id="b491c-123">Retorne se o cluster especificado foi excluído com êxito ou não.</span><span class="sxs-lookup"><span data-stu-id="b491c-123">Return whether the specified cluster was successfully deleted or not.</span></span>

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

### <span data-ttu-id="b491c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b491c-124">-ResourceGroupName</span></span>
<span data-ttu-id="b491c-125">Nome do grupo de recursos sob o qual o cluster existe.</span><span class="sxs-lookup"><span data-stu-id="b491c-125">Name of resource group under which the cluster exists.</span></span>

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

### <span data-ttu-id="b491c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b491c-126">-ResourceId</span></span>
<span data-ttu-id="b491c-127">ResourceId do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="b491c-127">Kusto cluster ResourceID.</span></span>

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

### <span data-ttu-id="b491c-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b491c-128">-Confirm</span></span>
<span data-ttu-id="b491c-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b491c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b491c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b491c-130">-WhatIf</span></span>
<span data-ttu-id="b491c-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b491c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b491c-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b491c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b491c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b491c-133">CommonParameters</span></span>
<span data-ttu-id="b491c-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b491c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b491c-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b491c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b491c-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b491c-136">INPUTS</span></span>

### <span data-ttu-id="b491c-137">System. String</span><span class="sxs-lookup"><span data-stu-id="b491c-137">System.String</span></span>

### <span data-ttu-id="b491c-138">Microsoft. Azure. Commands. Kusto. Models. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="b491c-138">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="b491c-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b491c-139">OUTPUTS</span></span>

### <span data-ttu-id="b491c-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b491c-140">System.Boolean</span></span>

## <span data-ttu-id="b491c-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b491c-141">NOTES</span></span>

## <span data-ttu-id="b491c-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b491c-142">RELATED LINKS</span></span>
