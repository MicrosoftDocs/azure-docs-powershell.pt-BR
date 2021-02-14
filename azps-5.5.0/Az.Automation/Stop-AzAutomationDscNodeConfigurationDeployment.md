---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/stop-azautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 3e5ec84dd3560c07fbf68c6f566b4691c1f6e512
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115532"
---
# <span data-ttu-id="c13dd-101">Stop-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="c13dd-101">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="c13dd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c13dd-102">SYNOPSIS</span></span>
<span data-ttu-id="c13dd-103">Interrompe uma implantação de configuração de nó DSC em Automação.</span><span class="sxs-lookup"><span data-stu-id="c13dd-103">Stops a DSC Node configuration deployment in Automation.</span></span> <span data-ttu-id="c13dd-104">Ele apenas interrompe o trabalho de implantação atual, mas não desaigna configurações de nó já atribuídas.</span><span class="sxs-lookup"><span data-stu-id="c13dd-104">It only stops the current deployment job but does not unassign already assigned node configurations.</span></span>

## <span data-ttu-id="c13dd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c13dd-105">SYNTAX</span></span>

### <span data-ttu-id="c13dd-106">ByJobId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c13dd-106">ByJobId (Default)</span></span>
```
Stop-AzAutomationDscNodeConfigurationDeployment -JobId <Guid> [-Force] [-PassThru]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c13dd-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c13dd-107">ByInputObject</span></span>
```
Stop-AzAutomationDscNodeConfigurationDeployment [-PassThru] -InputObject <NodeConfigurationDeployment>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c13dd-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="c13dd-108">DESCRIPTION</span></span>
<span data-ttu-id="c13dd-109">O cmdlet **Stop-AzAutomationDscNodeConfigurationDeployment** interrompe uma implantação de uma configuração de nó DSC (Configuração de Estado Desejada) no Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="c13dd-109">The **Stop-AzAutomationDscNodeConfigurationDeployment** cmdlet stops a deployment of a Desired State Configuration (DSC) node configuration in Azure Automation.</span></span> <span data-ttu-id="c13dd-110">Ela interrompe a atribuição de configuração de nó para grupos de nós, se ainda falta algum para ser atribuído, mas não desatribuição de nós já atribuídos.</span><span class="sxs-lookup"><span data-stu-id="c13dd-110">It stops assignment of node configuration to groups of nodes, if any are remaining to be assigned, but does not unassign already assigned nodes.</span></span> <span data-ttu-id="c13dd-111">Para não registro de um trabalho agendado, use o [Unregister-AzAutomationScheduledRunbook](./Unregister-AzAutomationScheduledRunbook.md) com o JobScheduleId para desmarcar um trabalho agendado existente.</span><span class="sxs-lookup"><span data-stu-id="c13dd-111">To unregister a scheduled job, please use the [Unregister-AzAutomationScheduledRunbook](./Unregister-AzAutomationScheduledRunbook.md) with the JobScheduleId to unassign an existing scheduled job.</span></span>

## <span data-ttu-id="c13dd-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c13dd-112">EXAMPLES</span></span>

### <span data-ttu-id="c13dd-113">Exemplo 1: Implantar uma configuração de nó DSC do Azure em Automação</span><span class="sxs-lookup"><span data-stu-id="c13dd-113">Example 1: Deploy an Azure DSC node configuration in Automation</span></span>
```
PS C:\> Stop-AzAutomationDscNodeConfigurationDeployment -AutomationAccountName "Contoso01" -ResourceGroupName "ResourceGroup01" -JobId 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="c13dd-114">O comando acima interrompe o trabalho de implantação de configuração do nó DSC com a jobId passada.</span><span class="sxs-lookup"><span data-stu-id="c13dd-114">The above command stops the DSC node configuration deployment job with the jobId passed in.</span></span>

## <span data-ttu-id="c13dd-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c13dd-115">PARAMETERS</span></span>

### <span data-ttu-id="c13dd-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c13dd-116">-AutomationAccountName</span></span>
<span data-ttu-id="c13dd-117">Especifica o nome da conta automação que contém a configuração DSC compilada por este cmdlet</span><span class="sxs-lookup"><span data-stu-id="c13dd-117">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c13dd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c13dd-118">-DefaultProfile</span></span>
<span data-ttu-id="c13dd-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="c13dd-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c13dd-120">-Forçar</span><span class="sxs-lookup"><span data-stu-id="c13dd-120">-Force</span></span>
<span data-ttu-id="c13dd-121">ps_force</span><span class="sxs-lookup"><span data-stu-id="c13dd-121">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByJobId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c13dd-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c13dd-122">-InputObject</span></span>
<span data-ttu-id="c13dd-123">Objeto de entrada para Piping</span><span class="sxs-lookup"><span data-stu-id="c13dd-123">Input object for Piping</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c13dd-124">-JobId</span><span class="sxs-lookup"><span data-stu-id="c13dd-124">-JobId</span></span>
<span data-ttu-id="c13dd-125">Especifica a ID do trabalho de um trabalho de implantação existente.</span><span class="sxs-lookup"><span data-stu-id="c13dd-125">Specifies the Job id of an existing deployment job.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ByJobId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c13dd-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c13dd-126">-PassThru</span></span>
<span data-ttu-id="c13dd-127">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="c13dd-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c13dd-128">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="c13dd-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c13dd-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c13dd-129">-ResourceGroupName</span></span>
<span data-ttu-id="c13dd-130">Especifica o nome de um grupo de recursos no qual este cmdlet compila uma configuração.</span><span class="sxs-lookup"><span data-stu-id="c13dd-130">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c13dd-131">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="c13dd-131">-Confirm</span></span>
<span data-ttu-id="c13dd-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c13dd-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c13dd-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c13dd-133">-WhatIf</span></span>
<span data-ttu-id="c13dd-134">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="c13dd-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c13dd-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c13dd-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c13dd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c13dd-136">CommonParameters</span></span>
<span data-ttu-id="c13dd-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c13dd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c13dd-138">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c13dd-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c13dd-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="c13dd-139">INPUTS</span></span>

### <span data-ttu-id="c13dd-140">System.Guid</span><span class="sxs-lookup"><span data-stu-id="c13dd-140">System.Guid</span></span>

### <span data-ttu-id="c13dd-141">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="c13dd-141">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

### <span data-ttu-id="c13dd-142">System.String</span><span class="sxs-lookup"><span data-stu-id="c13dd-142">System.String</span></span>

## <span data-ttu-id="c13dd-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="c13dd-143">OUTPUTS</span></span>

### <span data-ttu-id="c13dd-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c13dd-144">System.Boolean</span></span>

## <span data-ttu-id="c13dd-145">Notas</span><span class="sxs-lookup"><span data-stu-id="c13dd-145">NOTES</span></span>

## <span data-ttu-id="c13dd-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c13dd-146">RELATED LINKS</span></span>

[<span data-ttu-id="c13dd-147">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="c13dd-147">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="c13dd-148">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="c13dd-148">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="c13dd-149">Start-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="c13dd-149">Start-AzAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="c13dd-150">Get-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="c13dd-150">Get-AzAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="c13dd-151">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="c13dd-151">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md)
