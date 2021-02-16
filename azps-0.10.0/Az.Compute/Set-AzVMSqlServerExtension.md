---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: C650E465-7CDE-47F8-B85A-8FA3E1756FAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
ms.openlocfilehash: 1795216cbc18da2d503a1e0056d614337cd12785
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398233"
---
# Set-AzVMSqlServerExtension

## Sinopse
Define a extensão do SQL Server do Azure em uma máquina virtual.

## Sintaxe

```
Set-AzVMSqlServerExtension [[-Version] <String>] [-ResourceGroupName] <String> [-VMName] <String>
 [[-Name] <String>] [[-AutoPatchingSettings] <AutoPatchingSettings>]
 [[-AutoBackupSettings] <AutoBackupSettings>] [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>]
 [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrição
O cmdlet **Set-AzVMSqlServerExtension** define a extensão do AzureSQL Server em uma máquina virtual.

## Exemplos

### Exemplo 1: Definir configurações automáticas de patch em uma máquina virtual
```
PS C:\> $AutoPatchingConfig = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoPatchingSettings $AutoPatchingConfig | Update-AzVM
```

O primeiro comando cria um objeto de configuração usando o cmdlet **New-AzureVMSqlServerAutoPatchingConfig.**
O comando armazena a configuração na variável $AutoPatchingConfig dados.

O segundo comando obtém a máquina virtual chamada VirtualMachine11 no serviço chamado Service02 usando o cmdlet Get-AzVM usuário.
O comando passa esse objeto para o cmdlet atual usando o operador de pipeline.

O cmdlet atual define as configurações de patch automático $AutoPatchingConfig para a máquina virtual.
O comando passa a máquina virtual para o Update-AzVM cmdlet.

### Exemplo 2: Definir configurações de backup automático em uma máquina virtual
```
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoBackupSettings $AutoBackupConfig | Update-AzVM
```

O primeiro comando cria um objeto de configuração usando o cmdlet **New-AzureVMSqlServerAutoBackupConfig.**
O comando armazena a configuração na variável $AutoBackupConfig dados.

O segundo comando obtém a máquina virtual chamada VirtualMachine11 no serviço chamado Service02 e passa-a para o cmdlet atual.

O cmdlet atual define as configurações de backup automático $AutoBackupConfig para a máquina virtual.
O comando passa a máquina virtual para o Update-AzVM cmdlet.

### Exemplo 3: Desabilitar uma extensão do SQL Server em uma máquina virtual
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Disable
```

Esse comando obtém uma máquina virtual chamada VirtualMachine08 no Service03 e passa-a para o cmdlet atual.
O comando desabilita a extensão de máquina virtual do SQL Server nessa máquina virtual.

### Exemplo 4: Desinstalar uma extensão do SQL Server em uma máquina virtual específica
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Uninstall
```

Esse comando obtém uma máquina virtual chamada VirtualMachine08 no Service03 e passa-a para o cmdlet atual.
O comando desinstala uma extensão de máquina virtual do SQL Server nessa máquina virtual.

## Parâmetros

### -AutoBackupSettings
Especifica as configurações automáticas de backup do SQL Server.
Para criar um **objeto AutoBackupSettings,** use New-AzureVMSqlServerAutoBackupConfig cmdlet.

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
Especifica as configurações automáticas de patch do SQL Server.
Para criar um **objeto AutoPatchingSettings,** use New-AzureVMSqlServerAutoPatchingConfig cmdlet.

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
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.

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
Especifica a localização da máquina virtual.

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
Especifica o nome da extensão do SQL Server.

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
Especifica o nome da máquina virtual na qual este cmdlet define a extensão do SQL Server.

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
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Entradas

### Nenhum
Este cmdlet não aceita nenhuma entrada.

## Saídas

### Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse

## Notas

## LINKS RELACIONADOS

[Get-AzVM](./Get-AzVM.md)

[Get-AzVMSqlServerExtension](./Get-AzVMSqlServerExtension.md)

[New-AzureVMSqlServerAutoPatchingConfig](./New-AzVMSqlServerAutoPatchingConfig.md)

[New-AzureVMSqlServerAutoBackupConfig](./New-AzVMSqlServerAutoBackupConfig.md)

[Remove-AzVMSqlServerExtension](./Remove-AzVMSqlServerExtension.md)

[Update-AzVM](./Update-AzVM.md)


