---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/stop-azautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 3e5ec84dd3560c07fbf68c6f566b4691c1f6e512
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940468"
---
# <span data-ttu-id="5c4b8-101">Stop-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="5c4b8-101">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="5c4b8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5c4b8-102">SYNOPSIS</span></span>
<span data-ttu-id="5c4b8-103">Interrompe a implantação da configuração do nó DSC na automação.</span><span class="sxs-lookup"><span data-stu-id="5c4b8-103">Stops a DSC Node configuration deployment in Automation.</span></span> <span data-ttu-id="5c4b8-104">Ele somente interrompe o trabalho de implantação atual, mas não atribui configurações de nó já atribuídas.</span><span class="sxs-lookup"><span data-stu-id="5c4b8-104">It only stops the current deployment job but does not unassign already assigned node configurations.</span></span>

## <span data-ttu-id="5c4b8-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5c4b8-105">SYNTAX</span></span>

### <span data-ttu-id="5c4b8-106">ByJobId (padrão)</span><span class="sxs-lookup"><span data-stu-id="5c4b8-106">ByJobId (Default)</span></span>
```
Stop-AzAutomationDscNodeConfigurationDeployment -JobId <Guid> [-Force] [-PassThru]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c4b8-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5c4b8-107">ByInputObject</span></span>
```
Stop-AzAutomationDscNodeConfigurationDeployment [-PassThru] -InputObject <NodeConfigurationDeployment>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c4b8-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5c4b8-108">DESCRIPTION</span></span>
<span data-ttu-id="5c4b8-109">O cmdlet **Stop-AzAutomationDscNodeConfigurationDeployment** interrompe a implantação de uma configuração de nó de configuração de estado desejado (DSC) na automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="5c4b8-109">The **Stop-AzAutomationDscNodeConfigurationDeployment** cmdlet stops a deployment of a Desired State Configuration (DSC) node configuration in Azure Automation.</span></span> <span data-ttu-id="5c4b8-110">Ele interrompe a atribuição de configuração de nó a grupos de nós, se houver algum restante para ser atribuído, mas não atribua nós já atribuídos.</span><span class="sxs-lookup"><span data-stu-id="5c4b8-110">It stops assignment of node configuration to groups of nodes, if any are remaining to be assigned, but does not unassign already assigned nodes.</span></span> <span data-ttu-id="5c4b8-111">Para cancelar o registro de um trabalho agendado, use o [Unregister-AzAutomationScheduledRunbook](./Unregister-AzAutomationScheduledRunbook.md) com o JobScheduleId para cancelar a atribuição de um trabalho agendado existente.</span><span class="sxs-lookup"><span data-stu-id="5c4b8-111">To unregister a scheduled job, please use the [Unregister-AzAutomationScheduledRunbook](./Unregister-AzAutomationScheduledRunbook.md) with the JobScheduleId to unassign an existing scheduled job.</span></span>

## <span data-ttu-id="5c4b8-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5c4b8-112">EXAMPLES</span></span>

### <span data-ttu-id="5c4b8-113">Exemplo 1: implantar uma configuração de nó DSC do Azure na automação</span><span class="sxs-lookup"><span data-stu-id="5c4b8-113">Example 1: Deploy an Azure DSC node configuration in Automation</span></span>
```
PS C:\> Stop-AzAutomationDscNodeConfigurationDeployment -AutomationAccountName "Contoso01" -ResourceGroupName "ResourceGroup01" -JobId 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="5c4b8-114">O comando acima interrompe o trabalho de implantação da configuração do nó DSC com a jobId transmitida.</span><span class="sxs-lookup"><span data-stu-id="5c4b8-114">The above command stops the DSC node configuration deployment job with the jobId passed in.</span></span>

## <span data-ttu-id="5c4b8-115">OS</span><span class="sxs-lookup"><span data-stu-id="5c4b8-115">PARAMETERS</span></span>

### <span data-ttu-id="5c4b8-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5c4b8-116">-AutomationAccountName</span></span>
<span data-ttu-id="5c4b8-117">Especifica o nome da conta de automação que contém a configuração DSC que esse cmdlet compila</span><span class="sxs-lookup"><span data-stu-id="5c4b8-117">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles</span></span>

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

### <span data-ttu-id="5c4b8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c4b8-118">-DefaultProfile</span></span>
<span data-ttu-id="5c4b8-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="5c4b8-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5c4b8-120">-Force</span><span class="sxs-lookup"><span data-stu-id="5c4b8-120">-Force</span></span>
<span data-ttu-id="5c4b8-121">ps_force</span><span class="sxs-lookup"><span data-stu-id="5c4b8-121">ps_force</span></span>

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

### <span data-ttu-id="5c4b8-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5c4b8-122">-InputObject</span></span>
<span data-ttu-id="5c4b8-123">Objeto de entrada para tubulação</span><span class="sxs-lookup"><span data-stu-id="5c4b8-123">Input object for Piping</span></span>

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

### <span data-ttu-id="5c4b8-124">-JobId</span><span class="sxs-lookup"><span data-stu-id="5c4b8-124">-JobId</span></span>
<span data-ttu-id="5c4b8-125">Especifica a ID do trabalho de um trabalho de implantação existente.</span><span class="sxs-lookup"><span data-stu-id="5c4b8-125">Specifies the Job id of an existing deployment job.</span></span>

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

### <span data-ttu-id="5c4b8-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5c4b8-126">-PassThru</span></span>
<span data-ttu-id="5c4b8-127">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="5c4b8-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5c4b8-128">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="5c4b8-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5c4b8-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c4b8-129">-ResourceGroupName</span></span>
<span data-ttu-id="5c4b8-130">Especifica o nome de um grupo de recursos em que esse cmdlet compila uma configuração.</span><span class="sxs-lookup"><span data-stu-id="5c4b8-130">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="5c4b8-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5c4b8-131">-Confirm</span></span>
<span data-ttu-id="5c4b8-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c4b8-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c4b8-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c4b8-133">-WhatIf</span></span>
<span data-ttu-id="5c4b8-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5c4b8-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c4b8-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5c4b8-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c4b8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c4b8-136">CommonParameters</span></span>
<span data-ttu-id="5c4b8-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c4b8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c4b8-138">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c4b8-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c4b8-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5c4b8-139">INPUTS</span></span>

### <span data-ttu-id="5c4b8-140">System. GUID</span><span class="sxs-lookup"><span data-stu-id="5c4b8-140">System.Guid</span></span>

### <span data-ttu-id="5c4b8-141">Microsoft. Azure. Commands. Automation. Model. NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="5c4b8-141">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

### <span data-ttu-id="5c4b8-142">System. String</span><span class="sxs-lookup"><span data-stu-id="5c4b8-142">System.String</span></span>

## <span data-ttu-id="5c4b8-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5c4b8-143">OUTPUTS</span></span>

### <span data-ttu-id="5c4b8-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5c4b8-144">System.Boolean</span></span>

## <span data-ttu-id="5c4b8-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5c4b8-145">NOTES</span></span>

## <span data-ttu-id="5c4b8-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5c4b8-146">RELATED LINKS</span></span>

[<span data-ttu-id="5c4b8-147">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="5c4b8-147">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="5c4b8-148">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c4b8-148">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="5c4b8-149">Start-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="5c4b8-149">Start-AzAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="5c4b8-150">Get-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="5c4b8-150">Get-AzAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="5c4b8-151">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="5c4b8-151">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md)
