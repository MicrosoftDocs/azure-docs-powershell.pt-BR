---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/remove-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Remove-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Remove-AzDataBoxJob.md
ms.openlocfilehash: 545b99168d421fd9839d42bc8eb0af198dc48042
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112860"
---
# <span data-ttu-id="f1eca-101">Remove-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="f1eca-101">Remove-AzDataBoxJob</span></span>

## <span data-ttu-id="f1eca-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f1eca-102">SYNOPSIS</span></span>
<span data-ttu-id="f1eca-103">Exclui o trabalho databox</span><span class="sxs-lookup"><span data-stu-id="f1eca-103">Deletes the databox job</span></span>

## <span data-ttu-id="f1eca-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f1eca-104">SYNTAX</span></span>

### <span data-ttu-id="f1eca-105">GetByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="f1eca-105">GetByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxJob -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1eca-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1eca-106">GetByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1eca-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1eca-107">GetByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxJob -InputObject <PSDataBoxJob> [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1eca-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f1eca-108">DESCRIPTION</span></span>
<span data-ttu-id="f1eca-109">O cmdlet **Remove-AzDataBoxJob** é usado para excluir um trabalho do databox concluído da lista de trabalhos do databox.</span><span class="sxs-lookup"><span data-stu-id="f1eca-109">The **Remove-AzDataBoxJob** cmdlet is used to delete a finished databox job from the list of databox jobs.</span></span>

## <span data-ttu-id="f1eca-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f1eca-110">EXAMPLES</span></span>

### <span data-ttu-id="f1eca-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f1eca-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxJob -ResourceGroupName TestRg -name test 
Confirm
"Cancelling Databox Job "test
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

```

<span data-ttu-id="f1eca-112">Exclui o trabalho databox especificado</span><span class="sxs-lookup"><span data-stu-id="f1eca-112">Deletes the specified databox job</span></span>

### <span data-ttu-id="f1eca-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="f1eca-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzDataBoxJob -ResourceGroupName TestRg -name test -Force

```

<span data-ttu-id="f1eca-114">Exclui o trabalho databox especificado à força sem confirmação</span><span class="sxs-lookup"><span data-stu-id="f1eca-114">Deletes the specified databox job forcefully without confirmation</span></span>

### <span data-ttu-id="f1eca-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="f1eca-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzDataBoxJob -ResourceId "/subscriptions/05b5dd1c-793d-41de-be9f-6f9ed142f695/resourceGroups/TestRg/providers/Microsoft.DataBox/jobs/test"

```

<span data-ttu-id="f1eca-116">Exclui o trabalho databox especificado</span><span class="sxs-lookup"><span data-stu-id="f1eca-116">Deletes the specified databox job</span></span>

## <span data-ttu-id="f1eca-117">OS</span><span class="sxs-lookup"><span data-stu-id="f1eca-117">PARAMETERS</span></span>

### <span data-ttu-id="f1eca-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1eca-118">-DefaultProfile</span></span>
<span data-ttu-id="f1eca-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f1eca-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1eca-120">-Force</span><span class="sxs-lookup"><span data-stu-id="f1eca-120">-Force</span></span>
<span data-ttu-id="f1eca-121">Forçar remoção sem confirmação</span><span class="sxs-lookup"><span data-stu-id="f1eca-121">Force remove without confirmation</span></span>

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

### <span data-ttu-id="f1eca-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f1eca-122">-InputObject</span></span>
<span data-ttu-id="f1eca-123">InputObject do tipo PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="f1eca-123">InputObject of type PSDataBoxJob</span></span>

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

### <span data-ttu-id="f1eca-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="f1eca-124">-Name</span></span>
<span data-ttu-id="f1eca-125">Nome do trabalho Databox</span><span class="sxs-lookup"><span data-stu-id="f1eca-125">Databox Job Name</span></span>

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

### <span data-ttu-id="f1eca-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f1eca-126">-PassThru</span></span>
<span data-ttu-id="f1eca-127">PassThru</span><span class="sxs-lookup"><span data-stu-id="f1eca-127">PassThru</span></span>

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

### <span data-ttu-id="f1eca-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1eca-128">-ResourceGroupName</span></span>
<span data-ttu-id="f1eca-129">Nome do grupo de recursos de trabalho Databox</span><span class="sxs-lookup"><span data-stu-id="f1eca-129">Databox Job Resource Group Name</span></span>

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

### <span data-ttu-id="f1eca-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f1eca-130">-ResourceId</span></span>
<span data-ttu-id="f1eca-131">ID do recurso do trabalho Databox</span><span class="sxs-lookup"><span data-stu-id="f1eca-131">Databox Job Resource Id</span></span>

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

### <span data-ttu-id="f1eca-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f1eca-132">-Confirm</span></span>
<span data-ttu-id="f1eca-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1eca-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1eca-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1eca-134">-WhatIf</span></span>
<span data-ttu-id="f1eca-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f1eca-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f1eca-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f1eca-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1eca-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1eca-137">CommonParameters</span></span>
<span data-ttu-id="f1eca-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1eca-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1eca-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f1eca-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1eca-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f1eca-140">INPUTS</span></span>

### <span data-ttu-id="f1eca-141">System. String</span><span class="sxs-lookup"><span data-stu-id="f1eca-141">System.String</span></span>

## <span data-ttu-id="f1eca-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f1eca-142">OUTPUTS</span></span>

### <span data-ttu-id="f1eca-143">System. void</span><span class="sxs-lookup"><span data-stu-id="f1eca-143">System.Void</span></span>

## <span data-ttu-id="f1eca-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f1eca-144">NOTES</span></span>

## <span data-ttu-id="f1eca-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f1eca-145">RELATED LINKS</span></span>
