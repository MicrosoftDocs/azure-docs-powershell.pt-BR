---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/set-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Set-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Set-AzMigrateServerReplication.md
ms.openlocfilehash: 4c2afa4922d6e33493379739753856731020f321
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112978"
---
# Set-AzMigrateServerReplication

## Sinopse
Atualiza as propriedades de destino do servidor de replicação.

## Sintaxe

### ByIDVCbt (Padrão)
```
Set-AzMigrateServerReplication -TargetObjectID <String> [-NicToUpdate <IVMwareCbtNicInput[]>]
 [-SubscriptionId <String>] [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetNetworkId <String>] [-TargetResourceGroupID <String>]
 [-TargetVMName <String>] [-TargetVMSize <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### ByInputObjectVCbt
```
Set-AzMigrateServerReplication -InputObject <IMigrationItem> [-NicToUpdate <IVMwareCbtNicInput[]>]
 [-SubscriptionId <String>] [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetNetworkId <String>] [-TargetResourceGroupID <String>]
 [-TargetVMName <String>] [-TargetVMSize <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## Descrição
O Set-AzMigrateServerReplication cmdlet atualiza as propriedades de destino do servidor de replicação.

## Exemplos

### Exemplo 1: Atualizar por id
```powershell
PS C:\> Set-AzMigrateServerReplication -TargetObjectID '/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_500f44f8-2aa3-587b-8958-ead358639629' -TargetVMName 'rb-w2k12r2-1'

ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Update
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : Update
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

Por id.

## Parâmetros

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.

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

### -InputObject
Especifica o servidor de replicação para o qual as propriedades precisam ser atualizadas.
O objeto do servidor pode ser recuperado usando o cmdlet Get-AzMigrateServerReplication servidor.
Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IMigrationItem
Parameter Sets: ByInputObjectVMwareCbt
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NicToUpdate
Atualiza o NIC para que o VM do Azure seja criado.
Para construir, consulte a seção ANOTAÇÕES para propriedades NICTOUPDATE e crie uma tabela hash.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtNicInput[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
A ID da assinatura.

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

### -TargetAvailabilitySet
Especifica o Conjunto de Disponibilidade a ser usado para criação de VM.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetAvailabilityZone
Especifica a Zona de Disponibilidade a ser usada para a criação de VM.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetBootDiagnosticsStorageAccount
Especifica a conta de armazenamento a ser usada para diagnóstico de inicialização.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetNetworkId
Atualiza a ID da Rede Virtual dentro da assinatura do Azure de destino para a qual o servidor precisa ser migrado.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetObjectID
Especifica o servidor de resposta para o qual as propriedades precisam ser atualizadas.
A ID deve ser recuperada usando o cmdlet Get-AzMigrateServerReplication dados.

```yaml
Type: System.String
Parameter Sets: ByIDVMwareCbt
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetResourceGroupID
Atualiza a ID do Grupo de Recursos dentro da assinatura do Azure de destino para a qual o servidor precisa ser migrado.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetVMName
Especifica o servidor de resposta para o qual as propriedades precisam ser atualizadas.
A ID deve ser recuperada usando o cmdlet Get-AzMigrateServerReplication dados.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetVMSize
Atualiza a SKU do VM do Azure a ser criado.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## Entradas

## Saídas

### Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob

## Notas

Aliases

PROPRIEDADES DE PARÂMETRO COMPLEXOS

Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas. Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.


INPUTOBJECT: <IMigrationItem> especifica o servidor de replicação para o qual as propriedades precisam ser atualizadas. O objeto do servidor pode ser recuperado usando o cmdlet Get-AzMigrateServerReplication servidor.
  - `[Location <String>]`: Localização do Recurso
  - `[CurrentJobId <String>]`: A ID arm do trabalho que está sendo executado.
  - `[CurrentJobName <String>]`: o nome do trabalho.
  - `[CurrentJobStartTime <DateTime?>]`: a hora de início do trabalho.
  - `[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: As configurações personalizadas do provedor de migração.

NICTOUPDATE <IVCbtNicInput[]>: atualiza a NIC para que o VM do Azure seja criado.
  - `IsPrimaryNic <String>`: um valor que indica se essa é a NIC principal.
  - `NicId <String>`: A ID de NIC.
  - `[IsSelectedForMigration <String>]`: um valor que indica se essa NIC está selecionada para migração.
  - `[TargetStaticIPAddress <String>]`: o endereço IP estático.
  - `[TargetSubnetName <String>]`: Nome da sub-rede de destino.

## LINKS RELACIONADOS

