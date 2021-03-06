---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C650E465-7CDE-47F8-B85A-8FA3E1756FAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
ms.openlocfilehash: 753c1de5b2f967ad321334231c77e379e11bc2ba
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93948390"
---
# Set-AzVMSqlServerExtension

## Sinopse
Define a extensão do SQL Server do Azure em uma máquina virtual.

## SYNTAX

```
Set-AzVMSqlServerExtension [[-Version] <String>] [-ResourceGroupName] <String> [-VMName] <String>
 [[-Name] <String>] [[-AutoPatchingSettings] <AutoPatchingSettings>]
 [[-AutoBackupSettings] <AutoBackupSettings>] [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>]
 [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzVMSqlServerExtension** define a extensão do servidor AzureSQL em uma máquina virtual.

## EXEMPLOS

### Exemplo 1: definir as configurações de correção automática em uma máquina virtual
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoPatchingSettings $AutoPatchingConfig | Update-AzVM
```

O primeiro comando cria um objeto de configuração usando o cmdlet **New-AzVMSqlServerAutoPatchingConfig** .
O comando armazena a configuração na variável $AutoPatchingConfig.
O segundo comando obtém a máquina virtual chamada VirtualMachine11 no serviço chamado Service02 usando o cmdlet Get-AzVM.
O comando passa o objeto para o cmdlet atual usando o operador pipeline.
O cmdlet atual define as configurações de correção automática em $AutoPatchingConfig para a máquina virtual.
O comando passa a máquina virtual para o cmdlet Update-AzVM.

### Exemplo 2: definir configurações de backup automático em uma máquina virtual
```
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoBackupSettings $AutoBackupConfig | Update-AzVM
```

O primeiro comando cria um objeto de configuração usando o cmdlet **New-AzVMSqlServerAutoBackupConfig** .
O comando armazena a configuração na variável $AutoBackupConfig.
O segundo comando obtém a máquina virtual chamada VirtualMachine11 no serviço chamado Service02 e, em seguida, a transmite para o cmdlet atual.
O cmdlet atual define as configurações de backup automático em $AutoBackupConfig para a máquina virtual.
O comando passa a máquina virtual para o cmdlet Update-AzVM.

### Exemplo 3: desabilitar uma extensão do SQL Server em uma máquina virtual
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Disable
```

Esse comando obtém uma máquina virtual chamada VirtualMachine08 no Service03 e, em seguida, a transmite para o cmdlet atual.
O comando desabilita a extensão da máquina virtual do SQL Server nessa máquina virtual.

### Exemplo 4: desinstalar uma extensão do SQL Server em uma máquina virtual específica
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Uninstall
```

Esse comando obtém uma máquina virtual chamada VirtualMachine08 no Service03 e, em seguida, a transmite para o cmdlet atual.
O comando desinstala uma extensão de máquina virtual do SQL Server nessa máquina virtual.

## OS

### -AutoBackupSettings
Especifica as configurações de backup automático do SQL Server.
Para criar um objeto **AutoBackupSettings** , use o cmdlet New-AzVMSqlServerAutoBackupConfig.

```yaml
Type: Microsoft.Azure.Commands.Compute.AutoBackupSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AutoPatchingSettings
Especifica as configurações de correção automática do SQL Server.
Para criar um objeto **AutoPatchingSettings** , use o cmdlet New-AzVMSqlServerAutoPatchingConfig.

```yaml
Type: Microsoft.Azure.Commands.Compute.AutoPatchingSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -KeyVaultCredentialSettings
```yaml
Type: Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Local
Especifica o local da máquina virtual.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nome
Especifica o nome do SQL Server a extensão.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome do grupo de recursos da máquina virtual.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Versão
Especifica a versão da extensão do SQL Server.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
Especifica o nome da máquina virtual na qual esse cmdlet define a extensão do SQL Server.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

### System. String

### Microsoft. Azure. Commands. COMPUTE. AutoPatchingSettings

### Microsoft. Azure. Commands. COMPUTE. AutoBackupSettings

### Microsoft. Azure. Commands. COMPUTE. KeyVaultCredentialSettings

## EXIBE

### Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse

## INFORMA

## LINKS RELACIONADOS

[Get-AzVM](./Get-AzVM.md)

[Get-AzVMSqlServerExtension](./Get-AzVMSqlServerExtension.md)

[New-AzVMSqlServerAutoPatchingConfig](./New-AzVMSqlServerAutoPatchingConfig.md)

[New-AzVMSqlServerAutoBackupConfig](./New-AzVMSqlServerAutoBackupConfig.md)

[Remove-AzVMSqlServerExtension](./Remove-AzVMSqlServerExtension.md)

[Update-AzVM](./Update-AzVM.md)


