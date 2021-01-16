---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/stop-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Stop-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Stop-AzDataBoxJob.md
ms.openlocfilehash: 8e069dfe13ed060c80f884b93317148e7e6ec646
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433978"
---
# <span data-ttu-id="ef1fe-101">Stop-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="ef1fe-101">Stop-AzDataBoxJob</span></span>

## <span data-ttu-id="ef1fe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ef1fe-102">SYNOPSIS</span></span>
<span data-ttu-id="ef1fe-103">Cancela um trabalho em andamento do databox se o trabalho estiver em estado cancelável.</span><span class="sxs-lookup"><span data-stu-id="ef1fe-103">Cancels an ongoing databox job if the job is in cancellable state.</span></span>

## <span data-ttu-id="ef1fe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ef1fe-104">SYNTAX</span></span>

### <span data-ttu-id="ef1fe-105">GetByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="ef1fe-105">GetByNameParameterSet (Default)</span></span>
```
Stop-AzDataBoxJob -ResourceGroupName <String> -Name <String> -Reason <String>
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef1fe-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef1fe-106">GetByResourceIdParameterSet</span></span>
```
Stop-AzDataBoxJob -Reason <String> -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef1fe-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef1fe-107">GetByInputObjectParameterSet</span></span>
```
Stop-AzDataBoxJob -Reason <String> -InputObject <PSDataBoxJob> [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef1fe-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ef1fe-108">DESCRIPTION</span></span>
<span data-ttu-id="ef1fe-109">O cmdlet **Stop-AzDataBoxJob** é usado para cancelar um trabalho do databox.</span><span class="sxs-lookup"><span data-stu-id="ef1fe-109">The **Stop-AzDataBoxJob** cmdlet is used to cancel a databox job.</span></span>

## <span data-ttu-id="ef1fe-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ef1fe-110">EXAMPLES</span></span>

### <span data-ttu-id="ef1fe-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ef1fe-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzDataBoxJob -ResourceGroupName "TestRg" -name "test" -Reason "Random"
Confirm
"Removing Databox Job "test
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

```

<span data-ttu-id="ef1fe-112">Cancela o trabalho databox especificado</span><span class="sxs-lookup"><span data-stu-id="ef1fe-112">Cancels the specified databox job</span></span>

### <span data-ttu-id="ef1fe-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ef1fe-113">Example 2</span></span>
```powershell
PS C:\> Stop-AzDataBoxJob -ResourceGroupName "TestRg" -name "test" -Reason "Random" -Force

```

<span data-ttu-id="ef1fe-114">Cancela o trabalho do databox especificado à força sem confirmação</span><span class="sxs-lookup"><span data-stu-id="ef1fe-114">Cancels the specified databox job forcefully without confirmation</span></span>

### <span data-ttu-id="ef1fe-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="ef1fe-115">Example 3</span></span>
```powershell
PS C:\> Stop-AzDataBoxJob -ResourceId "/subscriptions/05b5dd1c-793d-41de-be9f-6f9ed142f695/resourceGroups/TestRg/providers/Microsoft.DataBox/jobs/test"

```

<span data-ttu-id="ef1fe-116">Cancela o trabalho databox especificado</span><span class="sxs-lookup"><span data-stu-id="ef1fe-116">Cancels the specified databox job</span></span>

## <span data-ttu-id="ef1fe-117">OS</span><span class="sxs-lookup"><span data-stu-id="ef1fe-117">PARAMETERS</span></span>

### <span data-ttu-id="ef1fe-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef1fe-118">-DefaultProfile</span></span>
<span data-ttu-id="ef1fe-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ef1fe-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef1fe-120">-Force</span><span class="sxs-lookup"><span data-stu-id="ef1fe-120">-Force</span></span>
<span data-ttu-id="ef1fe-121">Forçar parada sem confirmação</span><span class="sxs-lookup"><span data-stu-id="ef1fe-121">Force stop without confirmation</span></span>

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

### <span data-ttu-id="ef1fe-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef1fe-122">-InputObject</span></span>
<span data-ttu-id="ef1fe-123">InputObject do tipo PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="ef1fe-123">InputObject of type PSDataBoxJob</span></span>

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

### <span data-ttu-id="ef1fe-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="ef1fe-124">-Name</span></span>
<span data-ttu-id="ef1fe-125">Nome do trabalho Databox</span><span class="sxs-lookup"><span data-stu-id="ef1fe-125">Databox Job Name</span></span>

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

### <span data-ttu-id="ef1fe-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ef1fe-126">-PassThru</span></span>
<span data-ttu-id="ef1fe-127">PassThru</span><span class="sxs-lookup"><span data-stu-id="ef1fe-127">PassThru</span></span>

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

### <span data-ttu-id="ef1fe-128">-Motivo</span><span class="sxs-lookup"><span data-stu-id="ef1fe-128">-Reason</span></span>
<span data-ttu-id="ef1fe-129">Motivo do cancelamento</span><span class="sxs-lookup"><span data-stu-id="ef1fe-129">Reason For Cancellation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef1fe-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef1fe-130">-ResourceGroupName</span></span>
<span data-ttu-id="ef1fe-131">Nome do grupo de recursos de trabalho Databox</span><span class="sxs-lookup"><span data-stu-id="ef1fe-131">Databox Job Resource Group Name</span></span>

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

### <span data-ttu-id="ef1fe-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ef1fe-132">-ResourceId</span></span>
<span data-ttu-id="ef1fe-133">ID do recurso Databox</span><span class="sxs-lookup"><span data-stu-id="ef1fe-133">Databox Resource Id</span></span>

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

### <span data-ttu-id="ef1fe-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ef1fe-134">-Confirm</span></span>
<span data-ttu-id="ef1fe-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef1fe-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef1fe-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef1fe-136">-WhatIf</span></span>
<span data-ttu-id="ef1fe-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ef1fe-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ef1fe-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ef1fe-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef1fe-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef1fe-139">CommonParameters</span></span>
<span data-ttu-id="ef1fe-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef1fe-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef1fe-141">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ef1fe-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef1fe-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ef1fe-142">INPUTS</span></span>

### <span data-ttu-id="ef1fe-143">System. String</span><span class="sxs-lookup"><span data-stu-id="ef1fe-143">System.String</span></span>

## <span data-ttu-id="ef1fe-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ef1fe-144">OUTPUTS</span></span>

### <span data-ttu-id="ef1fe-145">System. void</span><span class="sxs-lookup"><span data-stu-id="ef1fe-145">System.Void</span></span>

## <span data-ttu-id="ef1fe-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ef1fe-146">NOTES</span></span>

## <span data-ttu-id="ef1fe-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ef1fe-147">RELATED LINKS</span></span>
