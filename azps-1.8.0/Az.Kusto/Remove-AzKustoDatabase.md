---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Remove-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Remove-AzKustoDatabase.md
ms.openlocfilehash: 141c601b5a903462b15bbeb45d410db24608323f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770566"
---
# <span data-ttu-id="5f20e-101">Remove-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="5f20e-101">Remove-AzKustoDatabase</span></span>

## <span data-ttu-id="5f20e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5f20e-102">SYNOPSIS</span></span>
<span data-ttu-id="5f20e-103">Exclui um banco de dados do Kusto existente.</span><span class="sxs-lookup"><span data-stu-id="5f20e-103">Deletes an existing Kusto database.</span></span>

## <span data-ttu-id="5f20e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5f20e-104">SYNTAX</span></span>

### <span data-ttu-id="5f20e-105">ByNameAndResourceGroup (padrão)</span><span class="sxs-lookup"><span data-stu-id="5f20e-105">ByNameAndResourceGroup (Default)</span></span>
```
Remove-AzKustoDatabase [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f20e-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5f20e-106">ByResourceId</span></span>
```
Remove-AzKustoDatabase [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f20e-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5f20e-107">ByInputObject</span></span>
```
Remove-AzKustoDatabase [-InputObject] <PSKustoDatabase> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f20e-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5f20e-108">DESCRIPTION</span></span>
<span data-ttu-id="5f20e-109">Exclui um banco de dados do Kusto existente.</span><span class="sxs-lookup"><span data-stu-id="5f20e-109">Deletes an existing Kusto database.</span></span>

## <span data-ttu-id="5f20e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5f20e-110">EXAMPLES</span></span>

### <span data-ttu-id="5f20e-111">Exemplo 1-excluir um banco de dados do Kusto existente por nome</span><span class="sxs-lookup"><span data-stu-id="5f20e-111">Example 1 - Delete an existing Kusto database by name</span></span>

```
PS C:\> Remove-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase
```

<span data-ttu-id="5f20e-112">O comando acima exclui o banco de dados Kusto chamado "mykustodatabase" no cluster "mykustocluster" localizado no grupo de recursos "testrg".</span><span class="sxs-lookup"><span data-stu-id="5f20e-112">The above command deletes the Kusto database named "mykustodatabase" in the cluster "mykustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="5f20e-113">Exemplo 2-excluir um banco de dados do Kusto existente por tubulação</span><span class="sxs-lookup"><span data-stu-id="5f20e-113">Example 2 - Delete an existing Kusto database by piping</span></span>

```
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase | Remove-AzKustoDatabase
```

<span data-ttu-id="5f20e-114">O comando acima Obtém o banco de dados Kusto chamado "mykustodatabase" no cluster "mykustocluster" localizado no grupo de recursos "testrg" usando o `Get-AzKustoDatabase` cmdlet e canaliza o resultado para `Remove-AzKustoDatabase` excluí-lo.</span><span class="sxs-lookup"><span data-stu-id="5f20e-114">The above command gets the Kusto database named "mykustodatabase" in the cluster "mykustocluster" found in the resource group "testrg" using the `Get-AzKustoDatabase` cmdlet, and then pipes the result to `Remove-AzKustoDatabase` to delete it.</span></span>

## <span data-ttu-id="5f20e-115">OS</span><span class="sxs-lookup"><span data-stu-id="5f20e-115">PARAMETERS</span></span>

### <span data-ttu-id="5f20e-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="5f20e-116">-ClusterName</span></span>
<span data-ttu-id="5f20e-117">Nome do cluster sob o qual o banco de dados existe.</span><span class="sxs-lookup"><span data-stu-id="5f20e-117">Name of the cluster under which the database exists.</span></span>

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

### <span data-ttu-id="5f20e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f20e-118">-DefaultProfile</span></span>
<span data-ttu-id="5f20e-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5f20e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f20e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5f20e-120">-InputObject</span></span>
<span data-ttu-id="5f20e-121">Objeto de banco de dados Kusto.</span><span class="sxs-lookup"><span data-stu-id="5f20e-121">Kusto database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5f20e-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="5f20e-122">-Name</span></span>
<span data-ttu-id="5f20e-123">Nome do banco de dados a ser removido.</span><span class="sxs-lookup"><span data-stu-id="5f20e-123">Name of database to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f20e-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5f20e-124">-PassThru</span></span>
<span data-ttu-id="5f20e-125">Retorna se o banco de dados especificado foi suspenso ou não com êxito.</span><span class="sxs-lookup"><span data-stu-id="5f20e-125">Return whether the specified database was successfully suspended or not.</span></span>

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

### <span data-ttu-id="5f20e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f20e-126">-ResourceGroupName</span></span>
<span data-ttu-id="5f20e-127">Nome do grupo de recursos sob o qual o cluster existe.</span><span class="sxs-lookup"><span data-stu-id="5f20e-127">Name of resource group under which the cluster exists.</span></span>

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

### <span data-ttu-id="5f20e-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5f20e-128">-ResourceId</span></span>
<span data-ttu-id="5f20e-129">ResourceId de banco de dados Kusto.</span><span class="sxs-lookup"><span data-stu-id="5f20e-129">Kusto database ResourceID.</span></span>

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

### <span data-ttu-id="5f20e-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5f20e-130">-Confirm</span></span>
<span data-ttu-id="5f20e-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f20e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f20e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f20e-132">-WhatIf</span></span>
<span data-ttu-id="5f20e-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5f20e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f20e-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5f20e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f20e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f20e-135">CommonParameters</span></span>
<span data-ttu-id="5f20e-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f20e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f20e-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f20e-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f20e-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5f20e-138">INPUTS</span></span>

### <span data-ttu-id="5f20e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="5f20e-139">System.String</span></span>

### <span data-ttu-id="5f20e-140">Microsoft. Azure. Commands. Kusto. Models. PSKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="5f20e-140">Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase</span></span>

## <span data-ttu-id="5f20e-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5f20e-141">OUTPUTS</span></span>

### <span data-ttu-id="5f20e-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5f20e-142">System.Boolean</span></span>

## <span data-ttu-id="5f20e-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5f20e-143">NOTES</span></span>

## <span data-ttu-id="5f20e-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5f20e-144">RELATED LINKS</span></span>
