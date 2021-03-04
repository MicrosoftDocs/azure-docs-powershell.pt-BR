---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/powershell/module/az.databox/remove-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Remove-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Remove-AzDataBoxJob.md
ms.openlocfilehash: 5a9415b5590b6f78c5ca703dba8293c153de819d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891395"
---
# <span data-ttu-id="5a7b1-101">Remove-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="5a7b1-101">Remove-AzDataBoxJob</span></span>

## <span data-ttu-id="5a7b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a7b1-102">SYNOPSIS</span></span>
<span data-ttu-id="5a7b1-103">Exclui o trabalho da caixa de dados</span><span class="sxs-lookup"><span data-stu-id="5a7b1-103">Deletes the databox job</span></span>

## <span data-ttu-id="5a7b1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="5a7b1-104">SYNTAX</span></span>

### <span data-ttu-id="5a7b1-105">GetByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5a7b1-105">GetByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxJob -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a7b1-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a7b1-106">GetByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a7b1-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a7b1-107">GetByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxJob -InputObject <PSDataBoxJob> [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a7b1-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="5a7b1-108">DESCRIPTION</span></span>
<span data-ttu-id="5a7b1-109">O cmdlet **Remove-AzDataBoxJob** é usado para excluir um trabalho de caixa de dados concluído da lista de trabalhos da caixa de dados.</span><span class="sxs-lookup"><span data-stu-id="5a7b1-109">The **Remove-AzDataBoxJob** cmdlet is used to delete a finished databox job from the list of databox jobs.</span></span>

## <span data-ttu-id="5a7b1-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5a7b1-110">EXAMPLES</span></span>

### <span data-ttu-id="5a7b1-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5a7b1-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxJob -ResourceGroupName TestRg -name test 
Confirm
"Cancelling Databox Job "test
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

```

<span data-ttu-id="5a7b1-112">Exclui o trabalho de caixa de dados especificada</span><span class="sxs-lookup"><span data-stu-id="5a7b1-112">Deletes the specified databox job</span></span>

### <span data-ttu-id="5a7b1-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="5a7b1-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzDataBoxJob -ResourceGroupName TestRg -name test -Force

```

<span data-ttu-id="5a7b1-114">Exclui o trabalho de caixa de dados especificado com força sem confirmação</span><span class="sxs-lookup"><span data-stu-id="5a7b1-114">Deletes the specified databox job forcefully without confirmation</span></span>

### <span data-ttu-id="5a7b1-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="5a7b1-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzDataBoxJob -ResourceId "/subscriptions/05b5dd1c-793d-41de-be9f-6f9ed142f695/resourceGroups/TestRg/providers/Microsoft.DataBox/jobs/test"

```

<span data-ttu-id="5a7b1-116">Exclui o trabalho de caixa de dados especificada</span><span class="sxs-lookup"><span data-stu-id="5a7b1-116">Deletes the specified databox job</span></span>

## <span data-ttu-id="5a7b1-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="5a7b1-117">PARAMETERS</span></span>

### <span data-ttu-id="5a7b1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a7b1-118">-DefaultProfile</span></span>
<span data-ttu-id="5a7b1-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5a7b1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a7b1-120">-Force</span><span class="sxs-lookup"><span data-stu-id="5a7b1-120">-Force</span></span>
<span data-ttu-id="5a7b1-121">Forçar a remoção sem confirmação</span><span class="sxs-lookup"><span data-stu-id="5a7b1-121">Force remove without confirmation</span></span>

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

### <span data-ttu-id="5a7b1-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a7b1-122">-InputObject</span></span>
<span data-ttu-id="5a7b1-123">InputObject do tipo PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="5a7b1-123">InputObject of type PSDataBoxJob</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a7b1-124">-Name</span><span class="sxs-lookup"><span data-stu-id="5a7b1-124">-Name</span></span>
<span data-ttu-id="5a7b1-125">Nome do Trabalho da Caixa de Dados</span><span class="sxs-lookup"><span data-stu-id="5a7b1-125">Databox Job Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a7b1-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5a7b1-126">-PassThru</span></span>
<span data-ttu-id="5a7b1-127">PassThru</span><span class="sxs-lookup"><span data-stu-id="5a7b1-127">PassThru</span></span>

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

### <span data-ttu-id="5a7b1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a7b1-128">-ResourceGroupName</span></span>
<span data-ttu-id="5a7b1-129">Nome do Grupo de Recursos de Trabalho da Caixa de Dados</span><span class="sxs-lookup"><span data-stu-id="5a7b1-129">Databox Job Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a7b1-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a7b1-130">-ResourceId</span></span>
<span data-ttu-id="5a7b1-131">ID do Recurso de Trabalho da Caixa de Dados</span><span class="sxs-lookup"><span data-stu-id="5a7b1-131">Databox Job Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a7b1-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5a7b1-132">-Confirm</span></span>
<span data-ttu-id="5a7b1-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a7b1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a7b1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a7b1-134">-WhatIf</span></span>
<span data-ttu-id="5a7b1-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5a7b1-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5a7b1-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5a7b1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a7b1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a7b1-137">CommonParameters</span></span>
<span data-ttu-id="5a7b1-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a7b1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a7b1-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5a7b1-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a7b1-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5a7b1-140">INPUTS</span></span>

### <span data-ttu-id="5a7b1-141">System.String</span><span class="sxs-lookup"><span data-stu-id="5a7b1-141">System.String</span></span>

## <span data-ttu-id="5a7b1-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="5a7b1-142">OUTPUTS</span></span>

### <span data-ttu-id="5a7b1-143">System.Void</span><span class="sxs-lookup"><span data-stu-id="5a7b1-143">System.Void</span></span>

## <span data-ttu-id="5a7b1-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="5a7b1-144">NOTES</span></span>

## <span data-ttu-id="5a7b1-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5a7b1-145">RELATED LINKS</span></span>
