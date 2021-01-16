---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/undo-azrecoveryservicesbackupitemdeletion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Undo-AzRecoveryServicesBackupItemDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Undo-AzRecoveryServicesBackupItemDeletion.md
ms.openlocfilehash: 62d8dc302dc5819272034cfdd1c3fd0c0c79f54c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271627"
---
# Undo-AzRecoveryServicesBackupItemDeletion

## Sinopse
Se um item de backup for excluído e estiver presente em um estado excluído de forma flexível, esse comando colocará o item novamente em um estado em que os dados são mantidos para sempre 

## SYNTAX

```
Undo-AzRecoveryServicesBackupItemDeletion [-Item] <ItemBase> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet Undo-AzRecoveryServicesBackupItemDeletion reverte um item excluído de forma flexível para um estado em que a proteção é interrompida, mas os dados são mantidos para sempre.

## EXEMPLOS

### Exemplo 1
```powershell
PS C:\> $Cont = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Disable-AzRecoveryServicesBackupProtection -Item $PI[0] -RemoveRecoveryPoints
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM | Where-Object {$_.DeleteState -eq "ToBeDeleted"}
PS C:\> Undo-AzRecoveryServicesBackupItemDeletion -Item $PI[0]
```

O primeiro comando obtém uma matriz de contêineres de backup e, em seguida, armazena-o na matriz $Cont.
O segundo comando obtém o item de backup correspondente ao primeiro item de contêiner e, em seguida, armazena-o na variável $PI.
O terceiro comando desabilita a proteção de backup para o item em $PI \[ 0 \] e coloca o item em um estado SoftDeleted.
O quarto comando obtém o item que está em um estado SoftDeleted.
O último comando leva a VM SoftDeleted a um estado em que a proteção é interrompida, mas os dados são mantidos para sempre.

### Exemplo 2

Rehydrates um item excluído de uma tela. (gerado automaticamente)

```powershell
<!-- Aladdin Generated Example --> 
Undo-AzRecoveryServicesBackupItemDeletion -Item $PI[0] -VaultId $vault.ID
```

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

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

### -Force
Force desabilita a proteção de backup (impede a caixa de diálogo de confirmação).
Este parâmetro é opcional.

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

### -Item
Especifica o item de backup para o qual esse cmdlet reverte a exclusão.
Para obter um AzureRmRecoveryServicesBackupItem, use o cmdlet Get-AzRecoveryServicesBackupItem.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Cofreid
ID do braço do cofre de serviços de recuperação.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Confirme
Solicita confirmação antes de executar o cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra o que aconteceria se o cmdlet fosse executado.
O cmdlet não é executado.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

### Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. dobase

### System. String

## EXIBE

### Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. JobBase

## INFORMA

## LINKS RELACIONADOS

[Get-AzRecoveryServicesBackupContainer]()

[Get-AzRecoveryServicesBackupItem]()

