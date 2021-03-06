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
# Get-AzMigrateJob

## SYNOPSIS
Recupera o status de um trabalho do Azure Migrate.

## SINTAXE

### ListByName (Padrão)
```
Get-AzMigrateJob -ProjectName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetById
```
Get-AzMigrateJob -JobID <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetByInputObject
```
Get-AzMigrateJob -InputObject <IJob> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### GetByName
```
Get-AzMigrateJob -JobName <String> -ProjectName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### ListById
```
Get-AzMigrateJob -ProjectID <String> -ResourceGroupID <String> [-SubscriptionId <String>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## DESCRIPTION
O Get-AzMigrateJob cmdlet recupera o status de um trabalho do Azure Migrate.

## EXEMPLOS

### Exemplo 1: Get By Job Id
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

Isso recupera um trabalho por meio da ID.

### Exemplo 2: Lista por grupo de recursos e projeto
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

Isso obtém todos os trabalhos em um projeto.

### Exemplo 3: Obter por grupo de recursos, projeto e nome de trabalho
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

Isso obtém um trabalho específico.

## PARÂMETROS

### -DefaultProfile
As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.

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

### -Filter
Opções de filtro OData.

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

### -InputObject
Especifica o objeto de trabalho do servidor de réplica.
Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.

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

### -JobID
Especifica a ID do trabalho para a qual os detalhes precisam ser recuperados.

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

### -JobName
Identificador de trabalho

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

### -ProjectID
Especifica o Projeto de Migração do Azure no qual os servidores estão sendo replicados.

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

### -ProjectName
O nome do projeto de migração.

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

### -ResourceGroupID
Especifica o Grupo de Recursos do Projeto migrar do Azure na assinatura atual.

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

### -ResourceGroupName
O nome do grupo de recursos onde o cofre de serviços de recuperação está presente.

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

### -SubscriptionId
ID da Assinatura do Azure.

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

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## SAÍDAS

### Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob

## NOTES

ALIASES

PROPRIEDADES DE PARÂMETRO COMPLEXO

Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas. Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.


INPUTOBJECT <IJob> : Especifica o objeto de trabalho do servidor de réplica.
  - `[Location <String>]`: Localização do Recurso
  - `[ActivityId <String>]`: A ID da atividade.
  - `[AllowedAction <String[]>]`: A ação Permitido do trabalho.
  - `[CustomDetailAffectedObjectDetail <IJobDetailsAffectedObjectDetails>]`: As propriedades de objeto afetadas, como servidor de origem, nuvem de origem, servidor de destino, nuvem de destino etc. com base nos detalhes do objeto de fluxo de trabalho.
    - `[(Any) <String>]`: Isso indica que qualquer propriedade pode ser adicionada a esse objeto.
  - `[EndTime <DateTime?>]`: A hora de término.
  - `[Error <IJobErrorDetails[]>]`: Os erros.
    - `[CreationTime <DateTime?>]`: O tempo de criação do erro de trabalho.
    - `[ErrorLevel <String>]`: Nível de erro.
    - `[ProviderErrorDetailErrorCode <Int32?>]`: O código de erro.
    - `[ProviderErrorDetailErrorId <String>]`: A ID de erro do provedor.
    - `[ProviderErrorDetailErrorMessage <String>]`: A mensagem De erro.
    - `[ProviderErrorDetailPossibleCaus <String>]`: As possíveis causas do erro.
    - `[ProviderErrorDetailRecommendedAction <String>]`: A ação recomendada para resolver o erro.
    - `[ServiceErrorDetailActivityId <String>]`: ID de atividade.
    - `[ServiceErrorDetailCode <String>]`: Código de erro.
    - `[ServiceErrorDetailMessage <String>]`: Mensagem de erro.
    - `[ServiceErrorDetailPossibleCaus <String>]`: Possíveis causas de erro.
    - `[ServiceErrorDetailRecommendedAction <String>]`: Ação recomendada para resolver o erro.
    - `[TaskId <String>]`: A ID da tarefa.
  - `[FriendlyName <String>]`: DisplayName.
  - `[ScenarioName <String>]`: ScenarioName.
  - `[StartTime <DateTime?>]`: A hora de início.
  - `[State <String>]`: o status do Trabalho. É um desses valores - NotStarted, InProgress, Succeeded, Failed, Cancelled, Suspended ou Other.
  - `[StateDescription <String>]`: A descrição do estado do trabalho. Por exemplo: - Para o estado bem-sucedido, a descrição pode ser Completed, PartiallySucceeded, CompletedWithInformation ou Skipped.
  - `[TargetInstanceType <String>]`: O tipo do objeto afetado que é da classe {Microsoft.Azure.SiteRecovery.V2015_11_10.AffectedObjectType}.
  - `[TargetObjectId <String>]`: A ID do objeto afetado.
  - `[TargetObjectName <String>]`: O nome do objeto afetado.
  - `[Task <IAsrTask[]>]`: As tarefas.
    - `[AllowedAction <String[]>]`: o estado/ações aplicáveis a essa tarefa.
    - `[CustomDetailInstanceType <String>]`: O tipo de detalhes da tarefa.
    - `[EndTime <DateTime?>]`: A hora de término.
    - `[Error <IJobErrorDetails[]>]`: Os detalhes do erro da tarefa.
    - `[FriendlyName <String>]`: O nome.
    - `[GroupTaskCustomDetailChildTask <IAsrTask[]>]`: As tarefas filho.
    - `[GroupTaskCustomDetailInstanceType <String>]`: O tipo de detalhes da tarefa.
    - `[Name <String>]`: O nome exclusivo da tarefa.
    - `[StartTime <DateTime?>]`: A hora de início.
    - `[State <String>]`: O Estado. É um desses valores - NotStarted, InProgress, Succeeded, Failed, Cancelled, Suspended ou Other.
    - `[StateDescription <String>]`: A descrição do estado da tarefa. Por exemplo: Para o estado bem-sucedido, a descrição pode ser Concluída, ParcialmenteSucedida, ConcluídaComInformation ou Ignorada.
    - `[TaskId <String>]`: A ID.
    - `[TaskType <String>]`: O tipo de tarefa. Os detalhes na propriedade CustomDetails dependem desse tipo.

## LINKS RELACIONADOS

