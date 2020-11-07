---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: C650E465-7CDE-47F8-B85A-8FA3E1756FAF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmsqlserverextension
schema: 2.0.0
ms.openlocfilehash: 2a1dbf5eea7f772a7819ed341a681adc24134225
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785967"
---
# Set-AzureRmVMSqlServerExtension

## Sinopse
Define a extensão do SQL Server do Azure em uma máquina virtual.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Set-AzureRmVMSqlServerExtension [[-Version] <String>] [-ResourceGroupName] <String> [-VMName] <String>
 [[-Name] <String>] [[-AutoPatchingSettings] <AutoPatchingSettings>]
 [[-AutoBackupSettings] <AutoBackupSettings>] [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>]
 [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzureRmVMSqlServerExtension** define a extensão do servidor AzureSQL em uma máquina virtual.

## EXEMPLOS

### Exemplo 1: definir as configurações de correção automática em uma máquina virtual
```
PS C:\> $AutoPatchingConfig = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
PS C:\> Get-AzureRmVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzureRmVMSqlServerExtension -AutoPatchingSettings $AutoPatchingConfig | Update-AzureRmVM
```

O primeiro comando cria um objeto de configuração usando o cmdlet **New-AzureVMSqlServerAutoPatchingConfig** .
O comando armazena a configuração na variável $AutoPatchingConfig.

O segundo comando obtém a máquina virtual chamada VirtualMachine11 no serviço chamado Service02 usando o cmdlet Get-AzureRmVM.
O comando passa o objeto para o cmdlet atual usando o operador pipeline.

O cmdlet atual define as configurações de correção automática em $AutoPatchingConfig para a máquina virtual.
O comando passa a máquina virtual para o cmdlet Update-AzureRmVM.

### Exemplo 2: definir configurações de backup automático em uma máquina virtual
```
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
PS C:\> Get-AzureRmVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzureRmVMSqlServerExtension -AutoBackupSettings $AutoBackupConfig | Update-AzureRmVM
```

O primeiro comando cria um objeto de configuração usando o cmdlet **New-AzureVMSqlServerAutoBackupConfig** .
O comando armazena a configuração na variável $AutoBackupConfig.

O segundo comando obtém a máquina virtual chamada VirtualMachine11 no serviço chamado Service02 e, em seguida, a transmite para o cmdlet atual.

O cmdlet atual define as configurações de backup automático em $AutoBackupConfig para a máquina virtual.
O comando passa a máquina virtual para o cmdlet Update-AzureRmVM.

### Exemplo 3: desabilitar uma extensão do SQL Server em uma máquina virtual
```
PS C:\> Get-AzureRmVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzureRmVMSqlServerExtension -Disable
```

Esse comando obtém uma máquina virtual chamada VirtualMachine08 no Service03 e, em seguida, a transmite para o cmdlet atual.
O comando desabilita a extensão da máquina virtual do SQL Server nessa máquina virtual.

### Exemplo 4: desinstalar uma extensão do SQL Server em uma máquina virtual específica
```
PS C:\> Get-AzureRmVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzureRmVMSqlServerExtension -Uninstall
```

Esse comando obtém uma máquina virtual chamada VirtualMachine08 no Service03 e, em seguida, a transmite para o cmdlet atual.
O comando desinstala uma extensão de máquina virtual do SQL Server nessa máquina virtual.

## OS

### -AutoBackupSettings
Especifica as configurações de backup automático do SQL Server.
Para criar um objeto **AutoBackupSettings** , use o cmdlet New-AzureVMSqlServerAutoBackupConfig.

```yaml
Type: AutoBackupSettings
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
Para criar um objeto **AutoPatchingSettings** , use o cmdlet New-AzureVMSqlServerAutoPatchingConfig.

```yaml
Type: AutoPatchingSettings
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyVaultCredentialSettings
```yaml
Type: KeyVaultCredentialSettings
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
Type: String
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
Type: String
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
Type: String
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
Type: String
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
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma
Esse cmdlet não aceita nenhuma entrada.

## EXIBE

### Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmVM](./Get-AzureRmVM.md)

[Get-AzureRmVMSqlServerExtension](./Get-AzureRMVMSqlServerExtension.md)





[Remove-AzureRmVMSqlServerExtension](./Remove-AzureRMVMSqlServerExtension.md)

[Update-AzureRmVM](./Update-AzureRmVM.md)


