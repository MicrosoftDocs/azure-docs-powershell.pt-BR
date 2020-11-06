---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Stop-AzureRmAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Stop-AzureRmAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 3ddaf0d4ae609305bf9740fbbe38a5fddd414e18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440218"
---
# <span data-ttu-id="f55a5-101">Stop-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="f55a5-101">Stop-AzureRmAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="f55a5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f55a5-102">SYNOPSIS</span></span>
<span data-ttu-id="f55a5-103">Interrompe a implantação da configuração do nó DSC na automação.</span><span class="sxs-lookup"><span data-stu-id="f55a5-103">Stops a DSC Node configuration deployment in Automation.</span></span> <span data-ttu-id="f55a5-104">Ele somente interrompe o trabalho de implantação atual, mas não atribui configurações de nó já atribuídas.</span><span class="sxs-lookup"><span data-stu-id="f55a5-104">It only stops the current deployment job but does not unassign already assigned node configurations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f55a5-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f55a5-105">SYNTAX</span></span>

### <span data-ttu-id="f55a5-106">ByJobId (padrão)</span><span class="sxs-lookup"><span data-stu-id="f55a5-106">ByJobId (Default)</span></span>
```
Stop-AzureRmAutomationDscNodeConfigurationDeployment -JobId <Guid> [-Force] [-PassThru]
 [-ResourceGroupName] <String> -AutomationAccountName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f55a5-107">ByByInputObject</span><span class="sxs-lookup"><span data-stu-id="f55a5-107">ByByInputObject</span></span>
```
Stop-AzureRmAutomationDscNodeConfigurationDeployment [-PassThru] -InputObject <NodeConfigurationDeployment>
 [-ResourceGroupName] <String> -AutomationAccountName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f55a5-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f55a5-108">DESCRIPTION</span></span>
<span data-ttu-id="f55a5-109">O cmdlet **Stop-AzureRmAutomationDscNodeConfigurationDeployment** interrompe a implantação de uma configuração de nó de configuração de estado desejado (DSC) na automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="f55a5-109">The **Stop-AzureRmAutomationDscNodeConfigurationDeployment** cmdlet stops a deployment of a Desired State Configuration (DSC) node configuration in Azure Automation.</span></span> <span data-ttu-id="f55a5-110">Ele interrompe a atribuição de configuração de nó a grupos de nós, se houver algum restante para ser atribuído, mas não atribua nós já atribuídos.</span><span class="sxs-lookup"><span data-stu-id="f55a5-110">It stops assignment of node configuration to groups of nodes, if any are remaining to be assigned, but does not unassign already assigned nodes.</span></span> <span data-ttu-id="f55a5-111">Para cancelar o registro de um trabalho agendado, use o [Unregister-AzureRmAutomationScheduledRunbook](./Unregister-AzureRmAutomationScheduledRunbook.md) com o JobScheduleId para cancelar a atribuição de um trabalho agendado existente.</span><span class="sxs-lookup"><span data-stu-id="f55a5-111">To unregister a scheduled job, please use the [Unregister-AzureRmAutomationScheduledRunbook](./Unregister-AzureRmAutomationScheduledRunbook.md) with the JobScheduleId to unassign an existing scheduled job.</span></span>

## <span data-ttu-id="f55a5-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f55a5-112">EXAMPLES</span></span>

### <span data-ttu-id="f55a5-113">Exemplo 1: implantar uma configuração de nó DSC do Azure na automação</span><span class="sxs-lookup"><span data-stu-id="f55a5-113">Example 1: Deploy an Azure DSC node configuration in Automation</span></span>
```
PS C:\> Stop-AzureRmAutomationDscNodeConfigurationDeployment -AutomationAccountName "Contoso01" -ResourceGroupName "ResourceGroup01" -JobId 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="f55a5-114">O comando acima interrompe o trabalho de implantação da configuração do nó DSC com a jobId transmitida.</span><span class="sxs-lookup"><span data-stu-id="f55a5-114">The above command stops the DSC node configuration deployment job with the jobId passed in.</span></span>

## <span data-ttu-id="f55a5-115">OS</span><span class="sxs-lookup"><span data-stu-id="f55a5-115">PARAMETERS</span></span>

### <span data-ttu-id="f55a5-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f55a5-116">-AutomationAccountName</span></span>
<span data-ttu-id="f55a5-117">Especifica o nome da conta de automação que contém a configuração DSC que esse cmdlet compila.</span><span class="sxs-lookup"><span data-stu-id="f55a5-117">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f55a5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f55a5-118">-ResourceGroupName</span></span>
<span data-ttu-id="f55a5-119">Especifica o nome de um grupo de recursos em que esse cmdlet compila uma configuração.</span><span class="sxs-lookup"><span data-stu-id="f55a5-119">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="f55a5-120">-JobId</span><span class="sxs-lookup"><span data-stu-id="f55a5-120">-JobId</span></span>
<span data-ttu-id="f55a5-121">Especifica a ID do trabalho de um trabalho de implantação existente.</span><span class="sxs-lookup"><span data-stu-id="f55a5-121">Specifies the Job id of an existing deployment job.</span></span>

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

### <span data-ttu-id="f55a5-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f55a5-122">-PassThru</span></span>
<span data-ttu-id="f55a5-123">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="f55a5-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f55a5-124">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="f55a5-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f55a5-125">-Force</span><span class="sxs-lookup"><span data-stu-id="f55a5-125">-Force</span></span>
<span data-ttu-id="f55a5-126">ps_force</span><span class="sxs-lookup"><span data-stu-id="f55a5-126">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByJobId
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f55a5-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f55a5-127">-Confirm</span></span>
<span data-ttu-id="f55a5-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f55a5-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f55a5-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f55a5-129">-WhatIf</span></span>
<span data-ttu-id="f55a5-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f55a5-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f55a5-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f55a5-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f55a5-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f55a5-132">-DefaultProfile</span></span>
<span data-ttu-id="f55a5-133">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f55a5-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f55a5-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f55a5-134">-InputObject</span></span>
<span data-ttu-id="f55a5-135">Objeto de entrada para tubulação.</span><span class="sxs-lookup"><span data-stu-id="f55a5-135">Input object for Piping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment
Parameter Sets: ByByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f55a5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f55a5-136">CommonParameters</span></span>
<span data-ttu-id="f55a5-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f55a5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f55a5-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f55a5-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f55a5-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f55a5-139">INPUTS</span></span>

## <span data-ttu-id="f55a5-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f55a5-140">OUTPUTS</span></span>

## <span data-ttu-id="f55a5-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f55a5-141">NOTES</span></span>

## <span data-ttu-id="f55a5-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f55a5-142">RELATED LINKS</span></span>

[<span data-ttu-id="f55a5-143">Start-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="f55a5-143">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)

[<span data-ttu-id="f55a5-144">Import-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="f55a5-144">Import-AzureRmAutomationDscNodeConfiguration</span></span>](./Import-AzureRmAutomationDscNodeConfiguration.md)

[<span data-ttu-id="f55a5-145">Start-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="f55a5-145">Start-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="f55a5-146">Get-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="f55a5-146">Get-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="f55a5-147">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="f55a5-147">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule.md)
