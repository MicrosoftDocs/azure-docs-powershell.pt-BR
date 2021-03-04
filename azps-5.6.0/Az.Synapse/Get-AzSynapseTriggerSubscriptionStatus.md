---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsetriggersubscriptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerSubscriptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerSubscriptionStatus.md
ms.openlocfilehash: c0c1b83f177b568e7058b973b788a633cfefe48c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887652"
---
# <span data-ttu-id="6de34-101">Get-AzSynapseTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="6de34-101">Get-AzSynapseTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="6de34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6de34-102">SYNOPSIS</span></span>
<span data-ttu-id="6de34-103">Obter o status da assinatura do gatilho de evento para os eventos de serviço externo especificados.</span><span class="sxs-lookup"><span data-stu-id="6de34-103">Get the status of the subscription for the event trigger to the specified external service events.</span></span>

## <span data-ttu-id="6de34-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6de34-104">SYNTAX</span></span>

### <span data-ttu-id="6de34-105">GetByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6de34-105">GetByName (Default)</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6de34-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="6de34-106">GetByObject</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6de34-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="6de34-107">GetByInputObject</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -InputObject <PSTriggerResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6de34-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6de34-108">DESCRIPTION</span></span>
<span data-ttu-id="6de34-109">O cmdlet **Get-AzSynapseTriggerSubscriptionStatus** obtém o status da assinatura do gatilho de eventos para os eventos de serviço externo especificados.</span><span class="sxs-lookup"><span data-stu-id="6de34-109">The **Get-AzSynapseTriggerSubscriptionStatus** cmdlet gets the status of the subscription for the event trigger to the specified external service events.</span></span> <span data-ttu-id="6de34-110">O gatilho não pode ser iniciado até que o status retornado seja "Habilitado".</span><span class="sxs-lookup"><span data-stu-id="6de34-110">The trigger can't be started until the returned status is "Enabled".</span></span>

## <span data-ttu-id="6de34-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6de34-111">EXAMPLES</span></span>

### <span data-ttu-id="6de34-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6de34-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseTriggerSubscriptionStatus -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="6de34-113">Este comando obterá o status da subscrição do gatilho chamado ContosoTrigger para os eventos de serviço externos.</span><span class="sxs-lookup"><span data-stu-id="6de34-113">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events.</span></span>

### <span data-ttu-id="6de34-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="6de34-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseTriggerSubscriptionStatus -Name ContosoTrigger
```

<span data-ttu-id="6de34-115">Este comando obterá o status da subscrição do gatilho chamado ContosoTrigger para os eventos de serviço externos por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="6de34-115">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events through pipeline.</span></span>

### <span data-ttu-id="6de34-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="6de34-116">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Get-AzSynapseTriggerSubscriptionStatus
```

<span data-ttu-id="6de34-117">Este comando obterá o status da subscrição do gatilho chamado ContosoTrigger para os eventos de serviço externos por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="6de34-117">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events through pipeline.</span></span>

## <span data-ttu-id="6de34-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6de34-118">PARAMETERS</span></span>

### <span data-ttu-id="6de34-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6de34-119">-DefaultProfile</span></span>
<span data-ttu-id="6de34-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6de34-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6de34-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6de34-121">-InputObject</span></span>
<span data-ttu-id="6de34-122">O objeto trigger.</span><span class="sxs-lookup"><span data-stu-id="6de34-122">The trigger object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource
Parameter Sets: GetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6de34-123">-Name</span><span class="sxs-lookup"><span data-stu-id="6de34-123">-Name</span></span>
<span data-ttu-id="6de34-124">O nome do gatilho.</span><span class="sxs-lookup"><span data-stu-id="6de34-124">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName, GetByObject
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6de34-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6de34-125">-WorkspaceName</span></span>
<span data-ttu-id="6de34-126">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="6de34-126">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6de34-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="6de34-127">-WorkspaceObject</span></span>
<span data-ttu-id="6de34-128">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="6de34-128">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6de34-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6de34-129">CommonParameters</span></span>
<span data-ttu-id="6de34-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6de34-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6de34-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6de34-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6de34-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6de34-132">INPUTS</span></span>

### <span data-ttu-id="6de34-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="6de34-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="6de34-134">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="6de34-134">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="6de34-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6de34-135">OUTPUTS</span></span>

### <span data-ttu-id="6de34-136">Microsoft.Azure.Commands.Synapse.Models.PSTriggerSubscriptionOperationStatus</span><span class="sxs-lookup"><span data-stu-id="6de34-136">Microsoft.Azure.Commands.Synapse.Models.PSTriggerSubscriptionOperationStatus</span></span>

## <span data-ttu-id="6de34-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="6de34-137">NOTES</span></span>

## <span data-ttu-id="6de34-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6de34-138">RELATED LINKS</span></span>
