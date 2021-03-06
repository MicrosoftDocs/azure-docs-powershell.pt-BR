---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: D614B509-82DD-42FB-B975-D72CD3355E3E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Set-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Set-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: f17ce0a23c2b91cd00f2a12bb2451c4e235169ce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440580"
---
# Set-AzureRmRecoveryServicesBackupProtectionPolicy

## Sinopse
Modifica uma política de proteção de backup.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Set-AzureRmRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase>
 [[-RetentionPolicy] <RetentionPolicyBase>] [[-SchedulePolicy] <SchedulePolicyBase>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzureRmBackupProtectionPolicy** modifica uma política de proteção de backup do Azure existente.
Você pode modificar o agendamento de backup e os componentes da política de retenção.

Todas as alterações feitas afetam o backup e a retenção dos itens associados à política.

Defina o contexto do cofre usando o cmdlet Set-AzureRmRecoveryServicesVaultContext antes de usar o cmdlet atual.

## EXEMPLOS

### Exemplo 1: modificar uma política de proteção de backup
```
PS C:\>$SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> $RetPol = Get-AzureRmRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $Pol = Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Set-AzureRmRecoveryServicesBackupProtectionPolicy -Policy $Pol -SchedulePolicy $SchPol -RetentionPolicy $RetPol
```

O primeiro comando obtém um objeto SchedulePolicy base e, em seguida, armazena-o na variável $SchPol.

O segundo comando Remove todos os horários de execução agendados da política de agendamento em $SchPol.

O terceiro comando usa o cmdlet Get-Date para obter a data e hora atuais e, em seguida, armazena-o na variável $DT.

O quarto comando adiciona a data e a hora no $DT ao tempo de execução do cronograma para a política de agendamento.

O quinto comando obtém um objeto de política de retenção base e, em seguida, armazena-o na variável $RetPol.

O sexto comando define a duração da retenção para 365 dias.

O sétimo comando obtém a política de proteção de backup chamada NewPolicy e a armazena na variável $Pol.

O comando final modifica a política de proteção de backup no $Pol usando a política de agendamento em $SchPol e a política de retenção em $RetPol.

## OS

### -Política
Especifica a política de proteção de backup que esse cmdlet modifica.
Para obter um objeto **BackupProtectionPolicy** , use o cmdlet Get-AzureRmRecoveryServicesBackupProtectionPolicy.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RetentionPolicy
Especifica a política de retenção básica.
Para obter um objeto **RetentionPolicy** , use o cmdlet Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SchedulePolicy
Especifica o objeto da política de cronograma básico.
Para obter um objeto **SchedulePolicy** , use o objeto Get-AzureRmRecoveryServicesBackupSchedulePolicyObject.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### PolicyBase
O parâmetro "política" aceita o valor do tipo "PolicyBase" da pipeline

## EXIBE

### System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. JobBase]

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmRecoveryServicesBackupProtectionPolicy](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[Get-AzureRmRecoveryServicesBackupRetentionPolicyObject](./Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md)

[New-AzureRmRecoveryServicesBackupProtectionPolicy](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[Remove-AzureRmRecoveryServicesBackupProtectionPolicy](./Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md)


