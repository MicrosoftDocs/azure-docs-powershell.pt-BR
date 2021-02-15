---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsetriggersubscriptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerSubscriptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerSubscriptionStatus.md
ms.openlocfilehash: b18a308b94bdb486945186c67c3a905bcb0408d3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114369"
---
# <span data-ttu-id="18569-101">Get-AzSynapseTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="18569-101">Get-AzSynapseTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="18569-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="18569-102">SYNOPSIS</span></span>
<span data-ttu-id="18569-103">Obter o status da assinatura do gatilho do evento para os eventos de serviço externo especificados.</span><span class="sxs-lookup"><span data-stu-id="18569-103">Get the status of the subscription for the event trigger to the specified external service events.</span></span>

## <span data-ttu-id="18569-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="18569-104">SYNTAX</span></span>

### <span data-ttu-id="18569-105">GetByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="18569-105">GetByName (Default)</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18569-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="18569-106">GetByObject</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18569-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="18569-107">GetByInputObject</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -InputObject <PSTriggerResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18569-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="18569-108">DESCRIPTION</span></span>
<span data-ttu-id="18569-109">O cmdlet **Get-AzSynapseTriscriptionStatus** obtém o status da assinatura do gatilho do evento para os eventos de serviço externo especificados.</span><span class="sxs-lookup"><span data-stu-id="18569-109">The **Get-AzSynapseTriggerSubscriptionStatus** cmdlet gets the status of the subscription for the event trigger to the specified external service events.</span></span> <span data-ttu-id="18569-110">O gatilho não pode ser iniciado até que o status retornado seja "Habilitado".</span><span class="sxs-lookup"><span data-stu-id="18569-110">The trigger can't be started until the returned status is "Enabled".</span></span>

## <span data-ttu-id="18569-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="18569-111">EXAMPLES</span></span>

### <span data-ttu-id="18569-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="18569-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseTriggerSubscriptionStatus -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="18569-113">Esse comando obterá o status da assinatura do gatilho chamado ContosoTrigregação para os eventos de serviço externo.</span><span class="sxs-lookup"><span data-stu-id="18569-113">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events.</span></span>

### <span data-ttu-id="18569-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="18569-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseTriggerSubscriptionStatus -Name ContosoTrigger
```

<span data-ttu-id="18569-115">Esse comando obterá o status da assinatura do gatilho chamado ContosoTri pipeline para os eventos de serviço externo.</span><span class="sxs-lookup"><span data-stu-id="18569-115">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events through pipeline.</span></span>

### <span data-ttu-id="18569-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="18569-116">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Get-AzSynapseTriggerSubscriptionStatus
```

<span data-ttu-id="18569-117">Esse comando obterá o status da assinatura do gatilho chamado ContosoTri pipeline para os eventos de serviço externo.</span><span class="sxs-lookup"><span data-stu-id="18569-117">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events through pipeline.</span></span>

## <span data-ttu-id="18569-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="18569-118">PARAMETERS</span></span>

### <span data-ttu-id="18569-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18569-119">-DefaultProfile</span></span>
<span data-ttu-id="18569-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="18569-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18569-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="18569-121">-InputObject</span></span>
<span data-ttu-id="18569-122">O objeto de gatilho.</span><span class="sxs-lookup"><span data-stu-id="18569-122">The trigger object.</span></span>

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

### <span data-ttu-id="18569-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="18569-123">-Name</span></span>
<span data-ttu-id="18569-124">O nome do gatilho.</span><span class="sxs-lookup"><span data-stu-id="18569-124">The trigger name.</span></span>

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

### <span data-ttu-id="18569-125">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="18569-125">-WorkspaceName</span></span>
<span data-ttu-id="18569-126">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="18569-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="18569-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="18569-127">-WorkspaceObject</span></span>
<span data-ttu-id="18569-128">objeto de entrada de espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="18569-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="18569-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18569-129">CommonParameters</span></span>
<span data-ttu-id="18569-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18569-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18569-131">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="18569-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18569-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="18569-132">INPUTS</span></span>

### <span data-ttu-id="18569-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="18569-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="18569-134">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="18569-134">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="18569-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="18569-135">OUTPUTS</span></span>

### <span data-ttu-id="18569-136">Microsoft.Azure.Commands.Synapse.Models.PSTrioperationStatus</span><span class="sxs-lookup"><span data-stu-id="18569-136">Microsoft.Azure.Commands.Synapse.Models.PSTriggerSubscriptionOperationStatus</span></span>

## <span data-ttu-id="18569-137">Notas</span><span class="sxs-lookup"><span data-stu-id="18569-137">NOTES</span></span>

## <span data-ttu-id="18569-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="18569-138">RELATED LINKS</span></span>
