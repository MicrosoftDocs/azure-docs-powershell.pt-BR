---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/powershell/module/az.databox/stop-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Stop-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Stop-AzDataBoxJob.md
ms.openlocfilehash: 60fdd8223f073ffd6de76db659e6bd989f48fada
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891475"
---
# <span data-ttu-id="842e1-101">Stop-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="842e1-101">Stop-AzDataBoxJob</span></span>

## <span data-ttu-id="842e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="842e1-102">SYNOPSIS</span></span>
<span data-ttu-id="842e1-103">Cancela um trabalho de caixa de dados em andamento se o trabalho estiver em estado cancelável.</span><span class="sxs-lookup"><span data-stu-id="842e1-103">Cancels an ongoing databox job if the job is in cancellable state.</span></span>

## <span data-ttu-id="842e1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="842e1-104">SYNTAX</span></span>

### <span data-ttu-id="842e1-105">GetByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="842e1-105">GetByNameParameterSet (Default)</span></span>
```
Stop-AzDataBoxJob -ResourceGroupName <String> -Name <String> -Reason <String>
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="842e1-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="842e1-106">GetByResourceIdParameterSet</span></span>
```
Stop-AzDataBoxJob -Reason <String> -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="842e1-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="842e1-107">GetByInputObjectParameterSet</span></span>
```
Stop-AzDataBoxJob -Reason <String> -InputObject <PSDataBoxJob> [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="842e1-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="842e1-108">DESCRIPTION</span></span>
<span data-ttu-id="842e1-109">O cmdlet **Stop-AzDataBoxJob** é usado para cancelar um trabalho de caixa de dados.</span><span class="sxs-lookup"><span data-stu-id="842e1-109">The **Stop-AzDataBoxJob** cmdlet is used to cancel a databox job.</span></span>

## <span data-ttu-id="842e1-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="842e1-110">EXAMPLES</span></span>

### <span data-ttu-id="842e1-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="842e1-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzDataBoxJob -ResourceGroupName "TestRg" -name "test" -Reason "Random"
Confirm
"Removing Databox Job "test
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

```

<span data-ttu-id="842e1-112">Cancela o trabalho de caixa de dados especificada</span><span class="sxs-lookup"><span data-stu-id="842e1-112">Cancels the specified databox job</span></span>

### <span data-ttu-id="842e1-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="842e1-113">Example 2</span></span>
```powershell
PS C:\> Stop-AzDataBoxJob -ResourceGroupName "TestRg" -name "test" -Reason "Random" -Force

```

<span data-ttu-id="842e1-114">Cancela o trabalho de caixa de dados especificado com força sem confirmação</span><span class="sxs-lookup"><span data-stu-id="842e1-114">Cancels the specified databox job forcefully without confirmation</span></span>

### <span data-ttu-id="842e1-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="842e1-115">Example 3</span></span>
```powershell
PS C:\> Stop-AzDataBoxJob -ResourceId "/subscriptions/05b5dd1c-793d-41de-be9f-6f9ed142f695/resourceGroups/TestRg/providers/Microsoft.DataBox/jobs/test"

```

<span data-ttu-id="842e1-116">Cancela o trabalho de caixa de dados especificada</span><span class="sxs-lookup"><span data-stu-id="842e1-116">Cancels the specified databox job</span></span>

## <span data-ttu-id="842e1-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="842e1-117">PARAMETERS</span></span>

### <span data-ttu-id="842e1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="842e1-118">-DefaultProfile</span></span>
<span data-ttu-id="842e1-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="842e1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="842e1-120">-Force</span><span class="sxs-lookup"><span data-stu-id="842e1-120">-Force</span></span>
<span data-ttu-id="842e1-121">Forçar parada sem confirmação</span><span class="sxs-lookup"><span data-stu-id="842e1-121">Force stop without confirmation</span></span>

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

### <span data-ttu-id="842e1-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="842e1-122">-InputObject</span></span>
<span data-ttu-id="842e1-123">InputObject do tipo PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="842e1-123">InputObject of type PSDataBoxJob</span></span>

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

### <span data-ttu-id="842e1-124">-Name</span><span class="sxs-lookup"><span data-stu-id="842e1-124">-Name</span></span>
<span data-ttu-id="842e1-125">Nome do Trabalho da Caixa de Dados</span><span class="sxs-lookup"><span data-stu-id="842e1-125">Databox Job Name</span></span>

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

### <span data-ttu-id="842e1-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="842e1-126">-PassThru</span></span>
<span data-ttu-id="842e1-127">PassThru</span><span class="sxs-lookup"><span data-stu-id="842e1-127">PassThru</span></span>

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

### <span data-ttu-id="842e1-128">-Reason</span><span class="sxs-lookup"><span data-stu-id="842e1-128">-Reason</span></span>
<span data-ttu-id="842e1-129">Motivo do cancelamento</span><span class="sxs-lookup"><span data-stu-id="842e1-129">Reason For Cancellation</span></span>

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

### <span data-ttu-id="842e1-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="842e1-130">-ResourceGroupName</span></span>
<span data-ttu-id="842e1-131">Nome do Grupo de Recursos de Trabalho da Caixa de Dados</span><span class="sxs-lookup"><span data-stu-id="842e1-131">Databox Job Resource Group Name</span></span>

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

### <span data-ttu-id="842e1-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="842e1-132">-ResourceId</span></span>
<span data-ttu-id="842e1-133">ID do Recurso de Caixa de Dados</span><span class="sxs-lookup"><span data-stu-id="842e1-133">Databox Resource Id</span></span>

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

### <span data-ttu-id="842e1-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="842e1-134">-Confirm</span></span>
<span data-ttu-id="842e1-135">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="842e1-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="842e1-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="842e1-136">-WhatIf</span></span>
<span data-ttu-id="842e1-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="842e1-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="842e1-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="842e1-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="842e1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="842e1-139">CommonParameters</span></span>
<span data-ttu-id="842e1-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="842e1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="842e1-141">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="842e1-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="842e1-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="842e1-142">INPUTS</span></span>

### <span data-ttu-id="842e1-143">System.String</span><span class="sxs-lookup"><span data-stu-id="842e1-143">System.String</span></span>

## <span data-ttu-id="842e1-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="842e1-144">OUTPUTS</span></span>

### <span data-ttu-id="842e1-145">System.Void</span><span class="sxs-lookup"><span data-stu-id="842e1-145">System.Void</span></span>

## <span data-ttu-id="842e1-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="842e1-146">NOTES</span></span>

## <span data-ttu-id="842e1-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="842e1-147">RELATED LINKS</span></span>
