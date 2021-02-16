---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/remove-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Remove-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Remove-AzDataBoxJob.md
ms.openlocfilehash: 545b99168d421fd9839d42bc8eb0af198dc48042
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117771"
---
# <span data-ttu-id="0d56a-101">Remove-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="0d56a-101">Remove-AzDataBoxJob</span></span>

## <span data-ttu-id="0d56a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0d56a-102">SYNOPSIS</span></span>
<span data-ttu-id="0d56a-103">Exclui o trabalho da caixa de dados</span><span class="sxs-lookup"><span data-stu-id="0d56a-103">Deletes the databox job</span></span>

## <span data-ttu-id="0d56a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0d56a-104">SYNTAX</span></span>

### <span data-ttu-id="0d56a-105">GetByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0d56a-105">GetByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxJob -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d56a-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d56a-106">GetByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d56a-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d56a-107">GetByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxJob -InputObject <PSDataBoxJob> [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d56a-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="0d56a-108">DESCRIPTION</span></span>
<span data-ttu-id="0d56a-109">O cmdlet **Remove-AzDataBox Job é** usado para excluir um trabalho de caixa de dados concluído da lista de trabalhos da caixa de dados.</span><span class="sxs-lookup"><span data-stu-id="0d56a-109">The **Remove-AzDataBoxJob** cmdlet is used to delete a finished databox job from the list of databox jobs.</span></span>

## <span data-ttu-id="0d56a-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0d56a-110">EXAMPLES</span></span>

### <span data-ttu-id="0d56a-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0d56a-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxJob -ResourceGroupName TestRg -name test 
Confirm
"Cancelling Databox Job "test
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

```

<span data-ttu-id="0d56a-112">Exclui o trabalho da caixa de dados especificada</span><span class="sxs-lookup"><span data-stu-id="0d56a-112">Deletes the specified databox job</span></span>

### <span data-ttu-id="0d56a-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="0d56a-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzDataBoxJob -ResourceGroupName TestRg -name test -Force

```

<span data-ttu-id="0d56a-114">Exclui o trabalho da caixa de dados especificado com força sem confirmação</span><span class="sxs-lookup"><span data-stu-id="0d56a-114">Deletes the specified databox job forcefully without confirmation</span></span>

### <span data-ttu-id="0d56a-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="0d56a-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzDataBoxJob -ResourceId "/subscriptions/05b5dd1c-793d-41de-be9f-6f9ed142f695/resourceGroups/TestRg/providers/Microsoft.DataBox/jobs/test"

```

<span data-ttu-id="0d56a-116">Exclui o trabalho da caixa de dados especificada</span><span class="sxs-lookup"><span data-stu-id="0d56a-116">Deletes the specified databox job</span></span>

## <span data-ttu-id="0d56a-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0d56a-117">PARAMETERS</span></span>

### <span data-ttu-id="0d56a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d56a-118">-DefaultProfile</span></span>
<span data-ttu-id="0d56a-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0d56a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d56a-120">-Forçar</span><span class="sxs-lookup"><span data-stu-id="0d56a-120">-Force</span></span>
<span data-ttu-id="0d56a-121">Forçar a remoção sem confirmação</span><span class="sxs-lookup"><span data-stu-id="0d56a-121">Force remove without confirmation</span></span>

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

### <span data-ttu-id="0d56a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0d56a-122">-InputObject</span></span>
<span data-ttu-id="0d56a-123">InputObject do tipo PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="0d56a-123">InputObject of type PSDataBoxJob</span></span>

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

### <span data-ttu-id="0d56a-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="0d56a-124">-Name</span></span>
<span data-ttu-id="0d56a-125">Nome do trabalho da Caixa de Dados</span><span class="sxs-lookup"><span data-stu-id="0d56a-125">Databox Job Name</span></span>

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

### <span data-ttu-id="0d56a-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0d56a-126">-PassThru</span></span>
<span data-ttu-id="0d56a-127">Passthru</span><span class="sxs-lookup"><span data-stu-id="0d56a-127">PassThru</span></span>

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

### <span data-ttu-id="0d56a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d56a-128">-ResourceGroupName</span></span>
<span data-ttu-id="0d56a-129">Nome do grupo de recursos de trabalho da caixa de dados</span><span class="sxs-lookup"><span data-stu-id="0d56a-129">Databox Job Resource Group Name</span></span>

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

### <span data-ttu-id="0d56a-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0d56a-130">-ResourceId</span></span>
<span data-ttu-id="0d56a-131">ID do Recurso de Trabalho da Caixa de Dados</span><span class="sxs-lookup"><span data-stu-id="0d56a-131">Databox Job Resource Id</span></span>

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

### <span data-ttu-id="0d56a-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="0d56a-132">-Confirm</span></span>
<span data-ttu-id="0d56a-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d56a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d56a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d56a-134">-WhatIf</span></span>
<span data-ttu-id="0d56a-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="0d56a-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0d56a-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0d56a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d56a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d56a-137">CommonParameters</span></span>
<span data-ttu-id="0d56a-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d56a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d56a-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0d56a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d56a-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="0d56a-140">INPUTS</span></span>

### <span data-ttu-id="0d56a-141">System.String</span><span class="sxs-lookup"><span data-stu-id="0d56a-141">System.String</span></span>

## <span data-ttu-id="0d56a-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="0d56a-142">OUTPUTS</span></span>

### <span data-ttu-id="0d56a-143">System.Void</span><span class="sxs-lookup"><span data-stu-id="0d56a-143">System.Void</span></span>

## <span data-ttu-id="0d56a-144">Notas</span><span class="sxs-lookup"><span data-stu-id="0d56a-144">NOTES</span></span>

## <span data-ttu-id="0d56a-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0d56a-145">RELATED LINKS</span></span>
