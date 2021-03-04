---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/get-azmigratejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateJob.md
ms.openlocfilehash: 9521e069f0b472353403a16caffad86e1147c1fe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889255"
---
# <span data-ttu-id="6887a-101">Get-AzMigrateJob</span><span class="sxs-lookup"><span data-stu-id="6887a-101">Get-AzMigrateJob</span></span>

## <span data-ttu-id="6887a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6887a-102">SYNOPSIS</span></span>
<span data-ttu-id="6887a-103">Recupera o status de um trabalho do Azure Migrate.</span><span class="sxs-lookup"><span data-stu-id="6887a-103">Retrieves the status of an Azure Migrate job.</span></span>

## <span data-ttu-id="6887a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6887a-104">SYNTAX</span></span>

### <span data-ttu-id="6887a-105">ListByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6887a-105">ListByName (Default)</span></span>
```
Get-AzMigrateJob -ProjectName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6887a-106">GetById</span><span class="sxs-lookup"><span data-stu-id="6887a-106">GetById</span></span>
```
Get-AzMigrateJob -JobID <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6887a-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="6887a-107">GetByInputObject</span></span>
```
Get-AzMigrateJob -InputObject <IJob> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="6887a-108">GetByName</span><span class="sxs-lookup"><span data-stu-id="6887a-108">GetByName</span></span>
```
Get-AzMigrateJob -JobName <String> -ProjectName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6887a-109">ListById</span><span class="sxs-lookup"><span data-stu-id="6887a-109">ListById</span></span>
```
Get-AzMigrateJob -ProjectID <String> -ResourceGroupID <String> [-SubscriptionId <String>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="6887a-110">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6887a-110">DESCRIPTION</span></span>
<span data-ttu-id="6887a-111">O Get-AzMigrateJob cmdlet recupera o status de um trabalho do Azure Migrate.</span><span class="sxs-lookup"><span data-stu-id="6887a-111">The Get-AzMigrateJob cmdlet retrives the status of an Azure Migrate job.</span></span>

## <span data-ttu-id="6887a-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6887a-112">EXAMPLES</span></span>

### <span data-ttu-id="6887a-113">Exemplo 1: Get By Job Id</span><span class="sxs-lookup"><span data-stu-id="6887a-113">Example 1: Get By Job Id</span></span>
```powershell
PS C:\> Get-AzMigrateJob -JobID "/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/997e2a92-5afe-49c7-a81a-89660aec9b7b" 

ActivityId                       : 68af14b4-46ae-48d1-b3e9-cdcffb9e8a93 ActivityId: 74d1a396-1d37-4264-8a5b-b727aaef0171
AllowedAction                    : {}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          : 9/16/20 11:57:33 AM
Error                            : {}
FriendlyName                     : Associate replication policy
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/997e2a92-5afe-49c7-a81a-89660aec9b7b
Location                         :
Name                             : 997e2a92-5afe-49c7-a81a-89660aec9b7b
ScenarioName                     : AssociateProtectionProfile
StartTime                        : 9/16/20 11:57:32 AM
State                            : Succeeded
StateDescription                 : Completed
TargetInstanceType               : ProtectionProfile
TargetObjectId                   : 42752b89-5fad-52fd-bf93-679fbdb6fed9
TargetObjectName                 : migrateAzMigratePWSHTc8d1sitepolicy
Task                             : {CloudPairingPrerequisitesCheck, CloudPairingPrepareSite}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="6887a-114">Isso recupera um trabalho por meio da ID.</span><span class="sxs-lookup"><span data-stu-id="6887a-114">This retrieves a job by it's Id.</span></span>

### <span data-ttu-id="6887a-115">Exemplo 2: Lista por grupo de recursos e projeto</span><span class="sxs-lookup"><span data-stu-id="6887a-115">Example 2: List by resource group and project</span></span>
```powershell
PS C:\> Get-AzMigrateJob -ResourceGroupName 'azmigratepwshtestasr13072020' -ProjectName 'AzMigrateTestProjectPWSH'

ActivityId                       :
AllowedAction                    : {}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         :
EndTime                          : 9/21/20 4:13:40 PM
Error                            : {}
FriendlyName                     : Update the virtual machine
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/1c89e38e-34ec-4903-aa7c-115201bf2de1
Location                         :
Name                             : 1c89e38e-34ec-4903-aa7c-115201bf2de1
ScenarioName                     : UpdateVmProperties
StartTime                        : 9/21/20 4:13:34 PM
State                            : Succeeded
StateDescription                 : Completed
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 593b735d-2a34-53b2-b8ed-e33da5650703
TargetObjectName                 : rb-w2k12r2-1
Task                             : {}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="6887a-116">Isso obtém todos os trabalhos em um projeto.</span><span class="sxs-lookup"><span data-stu-id="6887a-116">This gets all jobs in a project.</span></span>

### <span data-ttu-id="6887a-117">Exemplo 3: Obter por grupo de recursos, projeto e nome de trabalho</span><span class="sxs-lookup"><span data-stu-id="6887a-117">Example 3: Get by resource group, project and job name</span></span>
```powershell
PS C:\> Get-AzMigrateJob -ResourceGroupName 'azmigratepwshtestasr13072020' -ProjectName 'AzMigrateTestProjectPWSH' -JobName 7ae1ee7c-442c-499d-8b0e-81d52a42b71e

ActivityId                       : 6986b7e5-0f1f-49d8-8b4b-77e6f66bcb92 ActivityId: eb73c6a1-7c66-469f-a853-d896aa38cc0f
AllowedAction                    : {}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          : 8/21/20 6:41:48 AM
Error                            : {}
FriendlyName                     : Create replication policy
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/7ae1ee7c-442c-499d-8b0e-81d52a42b71e
Location                         :
Name                             : 7ae1ee7c-442c-499d-8b0e-81d52a42b71e
ScenarioName                     : AddProtectionProfile
StartTime                        : 8/21/20 6:41:48 AM
State                            : Succeeded
StateDescription                 : Completed
TargetInstanceType               : ProtectionProfile
TargetObjectId                   : 18b2ccec-e39a-517b-ae5d-dd395e9f4f96
TargetObjectName                 : samplePolicy3
Task                             : {AddProtectionProfilePreflightsCheckTask, AddProtectionProfileTask}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="6887a-118">Isso obtém um trabalho específico.</span><span class="sxs-lookup"><span data-stu-id="6887a-118">This gets a specific job.</span></span>

## <span data-ttu-id="6887a-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6887a-119">PARAMETERS</span></span>

### <span data-ttu-id="6887a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6887a-120">-DefaultProfile</span></span>
<span data-ttu-id="6887a-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6887a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6887a-122">-Filter</span><span class="sxs-lookup"><span data-stu-id="6887a-122">-Filter</span></span>
<span data-ttu-id="6887a-123">Opções de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="6887a-123">OData filter options.</span></span>

```yaml
Type: System.String
Parameter Sets: ListById, ListByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6887a-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6887a-124">-InputObject</span></span>
<span data-ttu-id="6887a-125">Especifica o objeto de trabalho do servidor de réplica.</span><span class="sxs-lookup"><span data-stu-id="6887a-125">Specifies the job object of the replicating server.</span></span>
<span data-ttu-id="6887a-126">Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="6887a-126">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob
Parameter Sets: GetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6887a-127">-JobID</span><span class="sxs-lookup"><span data-stu-id="6887a-127">-JobID</span></span>
<span data-ttu-id="6887a-128">Especifica a ID do trabalho para a qual os detalhes precisam ser recuperados.</span><span class="sxs-lookup"><span data-stu-id="6887a-128">Specifies the job id for which the details needs to be retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: GetById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6887a-129">-JobName</span><span class="sxs-lookup"><span data-stu-id="6887a-129">-JobName</span></span>
<span data-ttu-id="6887a-130">Identificador de trabalho</span><span class="sxs-lookup"><span data-stu-id="6887a-130">Job identifier</span></span>

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

### <span data-ttu-id="6887a-131">-ProjectID</span><span class="sxs-lookup"><span data-stu-id="6887a-131">-ProjectID</span></span>
<span data-ttu-id="6887a-132">Especifica o Projeto de Migração do Azure no qual os servidores estão sendo replicados.</span><span class="sxs-lookup"><span data-stu-id="6887a-132">Specifies the Azure Migrate Project in which servers are replicating.</span></span>

```yaml
Type: System.String
Parameter Sets: ListById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6887a-133">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="6887a-133">-ProjectName</span></span>
<span data-ttu-id="6887a-134">O nome do projeto de migração.</span><span class="sxs-lookup"><span data-stu-id="6887a-134">The name of the migrate project.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName, ListByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6887a-135">-ResourceGroupID</span><span class="sxs-lookup"><span data-stu-id="6887a-135">-ResourceGroupID</span></span>
<span data-ttu-id="6887a-136">Especifica o Grupo de Recursos do Projeto migrar do Azure na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="6887a-136">Specifies the Resource Group of the Azure Migrate Project in the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ListById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6887a-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6887a-137">-ResourceGroupName</span></span>
<span data-ttu-id="6887a-138">O nome do grupo de recursos onde o cofre de serviços de recuperação está presente.</span><span class="sxs-lookup"><span data-stu-id="6887a-138">The name of the resource group where the recovery services vault is present.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName, ListByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6887a-139">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6887a-139">-SubscriptionId</span></span>
<span data-ttu-id="6887a-140">ID da Assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="6887a-140">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6887a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6887a-141">CommonParameters</span></span>
<span data-ttu-id="6887a-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6887a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6887a-143">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6887a-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6887a-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6887a-144">INPUTS</span></span>

## <span data-ttu-id="6887a-145">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6887a-145">OUTPUTS</span></span>

### <span data-ttu-id="6887a-146">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span><span class="sxs-lookup"><span data-stu-id="6887a-146">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="6887a-147">NOTES</span><span class="sxs-lookup"><span data-stu-id="6887a-147">NOTES</span></span>

<span data-ttu-id="6887a-148">ALIASES</span><span class="sxs-lookup"><span data-stu-id="6887a-148">ALIASES</span></span>

<span data-ttu-id="6887a-149">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="6887a-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6887a-150">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="6887a-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6887a-151">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6887a-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6887a-152">INPUTOBJECT <IJob> : Especifica o objeto de trabalho do servidor de réplica.</span><span class="sxs-lookup"><span data-stu-id="6887a-152">INPUTOBJECT <IJob>: Specifies the job object of the replicating server.</span></span>
  - <span data-ttu-id="6887a-153">`[Location <String>]`: Localização do Recurso</span><span class="sxs-lookup"><span data-stu-id="6887a-153">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="6887a-154">`[ActivityId <String>]`: A ID da atividade.</span><span class="sxs-lookup"><span data-stu-id="6887a-154">`[ActivityId <String>]`: The activity id.</span></span>
  - <span data-ttu-id="6887a-155">`[AllowedAction <String[]>]`: A ação Permitido do trabalho.</span><span class="sxs-lookup"><span data-stu-id="6887a-155">`[AllowedAction <String[]>]`: The Allowed action the job.</span></span>
  - <span data-ttu-id="6887a-156">`[CustomDetailAffectedObjectDetail <IJobDetailsAffectedObjectDetails>]`: As propriedades de objeto afetadas, como servidor de origem, nuvem de origem, servidor de destino, nuvem de destino etc. com base nos detalhes do objeto de fluxo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="6887a-156">`[CustomDetailAffectedObjectDetail <IJobDetailsAffectedObjectDetails>]`: The affected object properties like source server, source cloud, target server, target cloud etc. based on the workflow object details.</span></span>
    - <span data-ttu-id="6887a-157">`[(Any) <String>]`: Isso indica que qualquer propriedade pode ser adicionada a esse objeto.</span><span class="sxs-lookup"><span data-stu-id="6887a-157">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="6887a-158">`[EndTime <DateTime?>]`: A hora de término.</span><span class="sxs-lookup"><span data-stu-id="6887a-158">`[EndTime <DateTime?>]`: The end time.</span></span>
  - <span data-ttu-id="6887a-159">`[Error <IJobErrorDetails[]>]`: Os erros.</span><span class="sxs-lookup"><span data-stu-id="6887a-159">`[Error <IJobErrorDetails[]>]`: The errors.</span></span>
    - <span data-ttu-id="6887a-160">`[CreationTime <DateTime?>]`: O tempo de criação do erro de trabalho.</span><span class="sxs-lookup"><span data-stu-id="6887a-160">`[CreationTime <DateTime?>]`: The creation time of job error.</span></span>
    - <span data-ttu-id="6887a-161">`[ErrorLevel <String>]`: Nível de erro.</span><span class="sxs-lookup"><span data-stu-id="6887a-161">`[ErrorLevel <String>]`: Error level of error.</span></span>
    - <span data-ttu-id="6887a-162">`[ProviderErrorDetailErrorCode <Int32?>]`: O código de erro.</span><span class="sxs-lookup"><span data-stu-id="6887a-162">`[ProviderErrorDetailErrorCode <Int32?>]`: The Error code.</span></span>
    - <span data-ttu-id="6887a-163">`[ProviderErrorDetailErrorId <String>]`: A ID de erro do provedor.</span><span class="sxs-lookup"><span data-stu-id="6887a-163">`[ProviderErrorDetailErrorId <String>]`: The Provider error Id.</span></span>
    - <span data-ttu-id="6887a-164">`[ProviderErrorDetailErrorMessage <String>]`: A mensagem De erro.</span><span class="sxs-lookup"><span data-stu-id="6887a-164">`[ProviderErrorDetailErrorMessage <String>]`: The Error message.</span></span>
    - <span data-ttu-id="6887a-165">`[ProviderErrorDetailPossibleCaus <String>]`: As possíveis causas do erro.</span><span class="sxs-lookup"><span data-stu-id="6887a-165">`[ProviderErrorDetailPossibleCaus <String>]`: The possible causes for the error.</span></span>
    - <span data-ttu-id="6887a-166">`[ProviderErrorDetailRecommendedAction <String>]`: A ação recomendada para resolver o erro.</span><span class="sxs-lookup"><span data-stu-id="6887a-166">`[ProviderErrorDetailRecommendedAction <String>]`: The recommended action to resolve the error.</span></span>
    - <span data-ttu-id="6887a-167">`[ServiceErrorDetailActivityId <String>]`: ID de atividade.</span><span class="sxs-lookup"><span data-stu-id="6887a-167">`[ServiceErrorDetailActivityId <String>]`: Activity Id.</span></span>
    - <span data-ttu-id="6887a-168">`[ServiceErrorDetailCode <String>]`: Código de erro.</span><span class="sxs-lookup"><span data-stu-id="6887a-168">`[ServiceErrorDetailCode <String>]`: Error code.</span></span>
    - <span data-ttu-id="6887a-169">`[ServiceErrorDetailMessage <String>]`: Mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="6887a-169">`[ServiceErrorDetailMessage <String>]`: Error message.</span></span>
    - <span data-ttu-id="6887a-170">`[ServiceErrorDetailPossibleCaus <String>]`: Possíveis causas de erro.</span><span class="sxs-lookup"><span data-stu-id="6887a-170">`[ServiceErrorDetailPossibleCaus <String>]`: Possible causes of error.</span></span>
    - <span data-ttu-id="6887a-171">`[ServiceErrorDetailRecommendedAction <String>]`: Ação recomendada para resolver o erro.</span><span class="sxs-lookup"><span data-stu-id="6887a-171">`[ServiceErrorDetailRecommendedAction <String>]`: Recommended action to resolve error.</span></span>
    - <span data-ttu-id="6887a-172">`[TaskId <String>]`: A ID da tarefa.</span><span class="sxs-lookup"><span data-stu-id="6887a-172">`[TaskId <String>]`: The Id of the task.</span></span>
  - <span data-ttu-id="6887a-173">`[FriendlyName <String>]`: DisplayName.</span><span class="sxs-lookup"><span data-stu-id="6887a-173">`[FriendlyName <String>]`: The DisplayName.</span></span>
  - <span data-ttu-id="6887a-174">`[ScenarioName <String>]`: ScenarioName.</span><span class="sxs-lookup"><span data-stu-id="6887a-174">`[ScenarioName <String>]`: The ScenarioName.</span></span>
  - <span data-ttu-id="6887a-175">`[StartTime <DateTime?>]`: A hora de início.</span><span class="sxs-lookup"><span data-stu-id="6887a-175">`[StartTime <DateTime?>]`: The start time.</span></span>
  - <span data-ttu-id="6887a-176">`[State <String>]`: o status do Trabalho.</span><span class="sxs-lookup"><span data-stu-id="6887a-176">`[State <String>]`: The status of the Job.</span></span> <span data-ttu-id="6887a-177">É um desses valores - NotStarted, InProgress, Succeeded, Failed, Cancelled, Suspended ou Other.</span><span class="sxs-lookup"><span data-stu-id="6887a-177">It is one of these values - NotStarted, InProgress, Succeeded, Failed, Cancelled, Suspended or Other.</span></span>
  - <span data-ttu-id="6887a-178">`[StateDescription <String>]`: A descrição do estado do trabalho.</span><span class="sxs-lookup"><span data-stu-id="6887a-178">`[StateDescription <String>]`: The description of the state of the Job.</span></span> <span data-ttu-id="6887a-179">Por exemplo: - Para o estado bem-sucedido, a descrição pode ser Completed, PartiallySucceeded, CompletedWithInformation ou Skipped.</span><span class="sxs-lookup"><span data-stu-id="6887a-179">For e.g. - For Succeeded state, description can be Completed, PartiallySucceeded, CompletedWithInformation or Skipped.</span></span>
  - <span data-ttu-id="6887a-180">`[TargetInstanceType <String>]`: O tipo do objeto afetado que é da classe {Microsoft.Azure.SiteRecovery.V2015_11_10.AffectedObjectType}.</span><span class="sxs-lookup"><span data-stu-id="6887a-180">`[TargetInstanceType <String>]`: The type of the affected object which is of {Microsoft.Azure.SiteRecovery.V2015_11_10.AffectedObjectType} class.</span></span>
  - <span data-ttu-id="6887a-181">`[TargetObjectId <String>]`: A ID do objeto afetado.</span><span class="sxs-lookup"><span data-stu-id="6887a-181">`[TargetObjectId <String>]`: The affected Object Id.</span></span>
  - <span data-ttu-id="6887a-182">`[TargetObjectName <String>]`: O nome do objeto afetado.</span><span class="sxs-lookup"><span data-stu-id="6887a-182">`[TargetObjectName <String>]`: The name of the affected object.</span></span>
  - <span data-ttu-id="6887a-183">`[Task <IAsrTask[]>]`: As tarefas.</span><span class="sxs-lookup"><span data-stu-id="6887a-183">`[Task <IAsrTask[]>]`: The tasks.</span></span>
    - <span data-ttu-id="6887a-184">`[AllowedAction <String[]>]`: o estado/ações aplicáveis a essa tarefa.</span><span class="sxs-lookup"><span data-stu-id="6887a-184">`[AllowedAction <String[]>]`: The state/actions applicable on this task.</span></span>
    - <span data-ttu-id="6887a-185">`[CustomDetailInstanceType <String>]`: O tipo de detalhes da tarefa.</span><span class="sxs-lookup"><span data-stu-id="6887a-185">`[CustomDetailInstanceType <String>]`: The type of task details.</span></span>
    - <span data-ttu-id="6887a-186">`[EndTime <DateTime?>]`: A hora de término.</span><span class="sxs-lookup"><span data-stu-id="6887a-186">`[EndTime <DateTime?>]`: The end time.</span></span>
    - <span data-ttu-id="6887a-187">`[Error <IJobErrorDetails[]>]`: Os detalhes do erro da tarefa.</span><span class="sxs-lookup"><span data-stu-id="6887a-187">`[Error <IJobErrorDetails[]>]`: The task error details.</span></span>
    - <span data-ttu-id="6887a-188">`[FriendlyName <String>]`: O nome.</span><span class="sxs-lookup"><span data-stu-id="6887a-188">`[FriendlyName <String>]`: The name.</span></span>
    - <span data-ttu-id="6887a-189">`[GroupTaskCustomDetailChildTask <IAsrTask[]>]`: As tarefas filho.</span><span class="sxs-lookup"><span data-stu-id="6887a-189">`[GroupTaskCustomDetailChildTask <IAsrTask[]>]`: The child tasks.</span></span>
    - <span data-ttu-id="6887a-190">`[GroupTaskCustomDetailInstanceType <String>]`: O tipo de detalhes da tarefa.</span><span class="sxs-lookup"><span data-stu-id="6887a-190">`[GroupTaskCustomDetailInstanceType <String>]`: The type of task details.</span></span>
    - <span data-ttu-id="6887a-191">`[Name <String>]`: O nome exclusivo da tarefa.</span><span class="sxs-lookup"><span data-stu-id="6887a-191">`[Name <String>]`: The unique Task name.</span></span>
    - <span data-ttu-id="6887a-192">`[StartTime <DateTime?>]`: A hora de início.</span><span class="sxs-lookup"><span data-stu-id="6887a-192">`[StartTime <DateTime?>]`: The start time.</span></span>
    - <span data-ttu-id="6887a-193">`[State <String>]`: O Estado.</span><span class="sxs-lookup"><span data-stu-id="6887a-193">`[State <String>]`: The State.</span></span> <span data-ttu-id="6887a-194">É um desses valores - NotStarted, InProgress, Succeeded, Failed, Cancelled, Suspended ou Other.</span><span class="sxs-lookup"><span data-stu-id="6887a-194">It is one of these values - NotStarted, InProgress, Succeeded, Failed, Cancelled, Suspended or Other.</span></span>
    - <span data-ttu-id="6887a-195">`[StateDescription <String>]`: A descrição do estado da tarefa.</span><span class="sxs-lookup"><span data-stu-id="6887a-195">`[StateDescription <String>]`: The description of the task state.</span></span> <span data-ttu-id="6887a-196">Por exemplo: Para o estado bem-sucedido, a descrição pode ser Concluída, ParcialmenteSucedida, ConcluídaComInformation ou Ignorada.</span><span class="sxs-lookup"><span data-stu-id="6887a-196">For example - For Succeeded state, description can be Completed, PartiallySucceeded, CompletedWithInformation or Skipped.</span></span>
    - <span data-ttu-id="6887a-197">`[TaskId <String>]`: A ID.</span><span class="sxs-lookup"><span data-stu-id="6887a-197">`[TaskId <String>]`: The Id.</span></span>
    - <span data-ttu-id="6887a-198">`[TaskType <String>]`: O tipo de tarefa.</span><span class="sxs-lookup"><span data-stu-id="6887a-198">`[TaskType <String>]`: The type of task.</span></span> <span data-ttu-id="6887a-199">Os detalhes na propriedade CustomDetails dependem desse tipo.</span><span class="sxs-lookup"><span data-stu-id="6887a-199">Details in CustomDetails property depend on this type.</span></span>

## <span data-ttu-id="6887a-200">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6887a-200">RELATED LINKS</span></span>

