---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 8A638FB1-F530-4E28-BAAE-5382671092C4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupItem.md
ms.openlocfilehash: 543aa3e28d7f3dee20065a0d20f2429b3fd6d4f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428000"
---
# Get-AzureRmBackupItem

## Sinopse
Obtém os itens em um contêiner no backup.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Get-AzureRmBackupItem [-ProtectionStatus <String>] [-Status <String>] [-Type <String>]
 [-Container] <AzureRMBackupContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmBackupItem** Obtém os itens em um contêiner no Azure backup e o status de proteção dos itens.
Habilite os itens para proteção usando o cmdlet Enable-AzureRmBackupProtection.

Um contêiner que está registrado em um cofre de backup pode ter um ou mais itens que podem ser protegidos.
Para máquinas virtuais do Azure, pode haver apenas um item no contêiner da máquina virtual.

## EXEMPLOS

### Exemplo 1: obter os itens em um contêiner
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> Get-AzureRmBackupItem -Container $Container
Name                    ProtectionStatus       DataSourceStatus       RecoveryPointsCount    ProtectionPolicyName
----                    ----------------       ----------------       -------------------    --------------------
co03-vm                 NotProtected                                  0
```

O primeiro comando obtém o cofre chamado Vault03 usando o cmdlet Get-AzureRmBackupVault.
O comando armazena esse objeto na variável $Vault.

O segundo comando obtém um contêiner que tem o nome especificado no cofre no $Vault usando o cmdlet **Get-AzureRmBackupContainer** .
O comando armazena esse objeto na variável $Container.

O comando final Obtém o item de backup no contêiner em $Container.

### Exemplo 2: exibir todas as propriedades de um item
```
PS C:\>Get-AzureRmBackupItem -Container $Container | Select-Object -Property *
Name                 : co03-vm
DataSourceStatus     : 
ProtectionStatus     : NotProtected
Type                 : AzureVM
ProtectionPolicyName : 
ProtectionPolicyId   : 
RecoveryPointsCount  : 0
ItemName             : iaasvmcontainer;co03-vm;co03-vm
ContainerType        : AzureVM
ContainerUniqueName  : iaasvmcontainer;co03-vm;co03-vm
ResourceGroupName    : resourcegroup02
ResourceName         : vault03
Location             : southeastasia
```

Esse comando obtém o item de backup no contêiner em $Container e, em seguida, o passa para o cmdlet Select-Object.
Esse cmdlet retorna todas as propriedades do item de backup.
Para obter mais informações, digite `Get-Help Select-Object` .

## OS

### -Contêiner
Especifica um objeto de contêiner para o qual este cmdlet obtém itens de backup.
Para obter um **AzureRmBackupContainer** , use o cmdlet Get-AzureRmBackupContainer.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ProtectionStatus
Especifica o status geral da proteção de um item no contêiner.
Os valores aceitáveis para esse parâmetro são:

- Protegida 
- Proteção  
- Não protegido

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Protected, Protecting, NotProtected

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Status
Especifica o status de backup de um item.
Os valores aceitáveis para esse parâmetro são: IRPending, Protected, ProtectionError e ProtectionStopped.
Se o parâmetro *ProtectionStatus* tiver o valor protegido, você poderá usar o valor do parâmetro *status* para filtrar itens.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: IRPending, ProtectionStopped, ProtectionError, Protected

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Digite
Especifica o tipo de item que este cmdlet obtém.
Atualmente, o único valor com suporte é AzureVM.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM

Required: False
Position: Named
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

### AzureRmBackupContainer

## EXIBE

### AzureRmBackupItem

## INFORMA

## LINKS RELACIONADOS

[Backup-AzureRmBackupItem](./Backup-AzureRmBackupItem.md)

[Disable-AzureRmBackupProtection](./Disable-AzureRmBackupProtection.md)

[Enable-AzureRmBackupProtection](./Enable-AzureRmBackupProtection.md)

[Get-AzureRmBackupContainer](./Get-AzureRmBackupContainer.md)

[Get-AzureRmBackupVault](./Get-AzureRmBackupVault.md)

[Restore-AzureRmBackupItem](./Restore-AzureRmBackupItem.md)


