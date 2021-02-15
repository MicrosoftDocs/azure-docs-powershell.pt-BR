---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/stop-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Stop-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Stop-AzDataBoxJob.md
ms.openlocfilehash: 8e069dfe13ed060c80f884b93317148e7e6ec646
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113884"
---
# <span data-ttu-id="1dc17-101">Stop-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="1dc17-101">Stop-AzDataBoxJob</span></span>

## <span data-ttu-id="1dc17-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1dc17-102">SYNOPSIS</span></span>
<span data-ttu-id="1dc17-103">Cancela um trabalho em andamento da caixa de dados se o trabalho estiver em estado cancelável.</span><span class="sxs-lookup"><span data-stu-id="1dc17-103">Cancels an ongoing databox job if the job is in cancellable state.</span></span>

## <span data-ttu-id="1dc17-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1dc17-104">SYNTAX</span></span>

### <span data-ttu-id="1dc17-105">GetByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="1dc17-105">GetByNameParameterSet (Default)</span></span>
```
Stop-AzDataBoxJob -ResourceGroupName <String> -Name <String> -Reason <String>
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1dc17-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1dc17-106">GetByResourceIdParameterSet</span></span>
```
Stop-AzDataBoxJob -Reason <String> -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1dc17-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1dc17-107">GetByInputObjectParameterSet</span></span>
```
Stop-AzDataBoxJob -Reason <String> -InputObject <PSDataBoxJob> [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1dc17-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="1dc17-108">DESCRIPTION</span></span>
<span data-ttu-id="1dc17-109">O cmdlet **Stop-AzDataBox Job** é usado para cancelar um trabalho de caixa de dados.</span><span class="sxs-lookup"><span data-stu-id="1dc17-109">The **Stop-AzDataBoxJob** cmdlet is used to cancel a databox job.</span></span>

## <span data-ttu-id="1dc17-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1dc17-110">EXAMPLES</span></span>

### <span data-ttu-id="1dc17-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1dc17-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzDataBoxJob -ResourceGroupName "TestRg" -name "test" -Reason "Random"
Confirm
"Removing Databox Job "test
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

```

<span data-ttu-id="1dc17-112">Cancela o trabalho da caixa de dados especificada</span><span class="sxs-lookup"><span data-stu-id="1dc17-112">Cancels the specified databox job</span></span>

### <span data-ttu-id="1dc17-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="1dc17-113">Example 2</span></span>
```powershell
PS C:\> Stop-AzDataBoxJob -ResourceGroupName "TestRg" -name "test" -Reason "Random" -Force

```

<span data-ttu-id="1dc17-114">Cancela o trabalho especificado da caixa de dados com força sem confirmação</span><span class="sxs-lookup"><span data-stu-id="1dc17-114">Cancels the specified databox job forcefully without confirmation</span></span>

### <span data-ttu-id="1dc17-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="1dc17-115">Example 3</span></span>
```powershell
PS C:\> Stop-AzDataBoxJob -ResourceId "/subscriptions/05b5dd1c-793d-41de-be9f-6f9ed142f695/resourceGroups/TestRg/providers/Microsoft.DataBox/jobs/test"

```

<span data-ttu-id="1dc17-116">Cancela o trabalho da caixa de dados especificada</span><span class="sxs-lookup"><span data-stu-id="1dc17-116">Cancels the specified databox job</span></span>

## <span data-ttu-id="1dc17-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1dc17-117">PARAMETERS</span></span>

### <span data-ttu-id="1dc17-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dc17-118">-DefaultProfile</span></span>
<span data-ttu-id="1dc17-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1dc17-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1dc17-120">-Forçar</span><span class="sxs-lookup"><span data-stu-id="1dc17-120">-Force</span></span>
<span data-ttu-id="1dc17-121">Forçar parada sem confirmação</span><span class="sxs-lookup"><span data-stu-id="1dc17-121">Force stop without confirmation</span></span>

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

### <span data-ttu-id="1dc17-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1dc17-122">-InputObject</span></span>
<span data-ttu-id="1dc17-123">InputObject do tipo PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="1dc17-123">InputObject of type PSDataBoxJob</span></span>

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

### <span data-ttu-id="1dc17-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="1dc17-124">-Name</span></span>
<span data-ttu-id="1dc17-125">Nome do trabalho da Caixa de Dados</span><span class="sxs-lookup"><span data-stu-id="1dc17-125">Databox Job Name</span></span>

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

### <span data-ttu-id="1dc17-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1dc17-126">-PassThru</span></span>
<span data-ttu-id="1dc17-127">Passthru</span><span class="sxs-lookup"><span data-stu-id="1dc17-127">PassThru</span></span>

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

### <span data-ttu-id="1dc17-128">-Motivo</span><span class="sxs-lookup"><span data-stu-id="1dc17-128">-Reason</span></span>
<span data-ttu-id="1dc17-129">Motivo do cancelamento</span><span class="sxs-lookup"><span data-stu-id="1dc17-129">Reason For Cancellation</span></span>

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

### <span data-ttu-id="1dc17-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dc17-130">-ResourceGroupName</span></span>
<span data-ttu-id="1dc17-131">Nome do grupo de recursos de trabalho da caixa de dados</span><span class="sxs-lookup"><span data-stu-id="1dc17-131">Databox Job Resource Group Name</span></span>

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

### <span data-ttu-id="1dc17-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1dc17-132">-ResourceId</span></span>
<span data-ttu-id="1dc17-133">ID do Recurso da Caixa de Dados</span><span class="sxs-lookup"><span data-stu-id="1dc17-133">Databox Resource Id</span></span>

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

### <span data-ttu-id="1dc17-134">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="1dc17-134">-Confirm</span></span>
<span data-ttu-id="1dc17-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1dc17-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1dc17-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dc17-136">-WhatIf</span></span>
<span data-ttu-id="1dc17-137">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="1dc17-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1dc17-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1dc17-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1dc17-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dc17-139">CommonParameters</span></span>
<span data-ttu-id="1dc17-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dc17-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dc17-141">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1dc17-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dc17-142">Entradas</span><span class="sxs-lookup"><span data-stu-id="1dc17-142">INPUTS</span></span>

### <span data-ttu-id="1dc17-143">System.String</span><span class="sxs-lookup"><span data-stu-id="1dc17-143">System.String</span></span>

## <span data-ttu-id="1dc17-144">Saídas</span><span class="sxs-lookup"><span data-stu-id="1dc17-144">OUTPUTS</span></span>

### <span data-ttu-id="1dc17-145">System.Void</span><span class="sxs-lookup"><span data-stu-id="1dc17-145">System.Void</span></span>

## <span data-ttu-id="1dc17-146">Notas</span><span class="sxs-lookup"><span data-stu-id="1dc17-146">NOTES</span></span>

## <span data-ttu-id="1dc17-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1dc17-147">RELATED LINKS</span></span>
