---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2575F5C4-A276-49CE-AB0C-726F359DA6F9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7f71138e47c851097fe36ca294784fc571b6369f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945751"
---
# Start-AzureSiteRecoveryPlannedFailoverJob

## Sinopse
Inicia uma operação de failover planejado de recuperação de site.

## SYNTAX

### ByRPId (padrão)
```
Start-AzureSiteRecoveryPlannedFailoverJob -RPId <String> -Direction <String> [-WaitForCompletion]
 [-Optimize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByPEId
```
Start-AzureSiteRecoveryPlannedFailoverJob -ProtectionEntityId <String> -ProtectionContainerId <String>
 -Direction <String> [-WaitForCompletion] [-Optimize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByRPObject
```
Start-AzureSiteRecoveryPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-WaitForCompletion] [-Optimize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByPEObject
```
Start-AzureSiteRecoveryPlannedFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-WaitForCompletion] [-Optimize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Start-AzureSiteRecoveryPlannedFailoverJob** inicia um failover planejado para uma entidade de proteção do Azure site Recovery ou um plano de recuperação.
Você pode verificar se o trabalho foi bem-sucedido usando o cmdlet **Get-AzureSiteRecoveryJob** .

## EXEMPLOS

### Exemplo 1: iniciar um trabalho de failover planejado
```
PS C:\> $Container = Get-AzureSiteRecoveryProtectionContainer 
PS C:\> $Protected = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $Container 
PS C:\> Start-AzureSiteRecoveryPlannedFailoverJob -Direction PrimaryToRecovery -ProtectionEntity $Protected -Optimize ForDowntime
ID               : c38eecdc-731c-405b-a61c-08db99aae2fe
ClientRequestId  : 32ace403-0916-4967-83a1-529176bd6e88-2014-49-06 15:49:24Z-P
State            : NotStarted
StateDescription : NotStarted
StartTime        : 
EndTime          : 
AllowedActions   : {}
Name             : 
Tasks            : {}
Errors           : {}
```

O primeiro comando obtém todos os contêineres protegidos no cofre do Azure site Recovery atual usando o cmdlet **Get-AzureSiteRecoveryProtectionContainer** e, em seguida, armazena os resultados na variável $container.
Neste exemplo, há um único contêiner.

O segundo comando obtém as máquinas virtuais protegidas que pertencem ao contêiner armazenado no $Container usando o cmdlet **Get-AzureSiteRecoveryProtectionEntity** .
O comando armazena os resultados na variável $Protected.

O comando final inicia o trabalho de failover na direção PrimaryToRecovery para as máquinas virtuais protegidas armazenadas em $Protected.

## OS

### -Direction
Especifica a direção do failover.
Os valores aceitáveis para esse parâmetro são:

- PrimaryToRecovery
- RecoveryToPrimary

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Otimizar
Especifica o que otimizar para.
Esse parâmetro se aplica para failover de um site do Azure para um site local que requer uma sincronização de dados significativa.
Os valores aceitáveis para esse parâmetro são:

- ForDowntime
- ForSynchronization

Quando **ForDowntime** é especificado, isso indica que os dados são sincronizados antes do failover para minimizar o tempo de inatividade.
A sincronização é realizada sem desligar a máquina virtual.
Após a conclusão da sincronização, o trabalho será suspenso.
Retome o trabalho para executar uma operação de sincronização adicional que desative a máquina virtual.

Quando **ForSynchronization** é especificado, isso indica que os dados são sincronizados durante o failover, para que a sincronização de dados seja minimizada.
Como essa configuração está habilitada, a máquina virtual é desligada imediatamente.
A sincronização começará após o desligamento para concluir a operação de failover.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Perfil
Especifica o perfil do Azure do qual este cmdlet lê.
Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProtectionContainerId
Especifica a ID do contêiner protegido para a qual iniciar o trabalho.

```yaml
Type: String
Parameter Sets: ByPEId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProtectionEntity
Especifica o objeto da entidade de proteção do site.

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ProtectionEntityId
Especifica um objeto **ASRProtectionEntity** para o qual iniciar o trabalho.
Para obter um objeto **ASRProtectionEntity** , use o cmdlet **Get-AzureSiteRecoveryProtectionEntity** .

```yaml
Type: String
Parameter Sets: ByPEId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryPlan
Especifica um objeto de plano de recuperação.

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RPId
Especifica a ID de um plano de recuperação para iniciar o trabalho.

```yaml
Type: String
Parameter Sets: ByRPId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WaitForCompletion
Indica que o cmdlet aguarda a conclusão da operação antes de retornar o controle ao console do Windows PowerShell.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

## INFORMA

## LINKS RELACIONADOS

[Get-AzureSiteRecoveryProtectionContainer](./Get-AzureSiteRecoveryProtectionContainer.md)

[Get-AzureSiteRecoveryProtectionEntity](./Get-AzureSiteRecoveryProtectionEntity.md)


