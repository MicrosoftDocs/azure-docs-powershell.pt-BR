---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 39AADD19-2EDD-4C1F-BC9E-22186DD9A085
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmoperatingsystem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
ms.openlocfilehash: 75eb0ef60443cdbf2dfe3fa53202d3c8141d4888
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890300"
---
# Set-AzVMOperatingSystem

## SYNOPSIS
Define as propriedades do sistema operacional para uma máquina virtual.

## SINTAXE

### Windows (Padrão)
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-EnableHotpatching]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### WindowsWinRmHttps
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-EnableHotpatching] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### WindowsDisableVMAgent
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-EnableHotpatching]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### WindowsDisableVMAgentWinRmHttps
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-EnableHotpatching] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Linux
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Linux] [-ComputerName] <String> [-Credential] <PSCredential>
 [[-CustomData] <String>] [-PatchMode <String>] [-DisablePasswordAuthentication]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIPTION
O cmdlet **Set-AzVMOperatingSystem** define propriedades do sistema operacional para uma máquina virtual.
Você pode especificar credenciais de logon, nome do computador e tipo de sistema operacional.

## EXEMPLOS

### Exemplo 1: Definir propriedades do sistema operacional para uma nova máquina virtual
```
$SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
$AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
$VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
$ComputerName = "ContosoVM122"
$WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
$TimeZone = "Pacific Standard Time"
$CustomData = "echo 'Hello World'"
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone -PatchMode "AutomaticByPlatform"
```

O primeiro comando converte uma senha em uma cadeia de caracteres segura e a armazena na variável $SecurePassword segurança.
Para obter mais informações, digite `Get-Help ConvertTo-SecureString` .
O segundo comando cria uma credencial para o usuário FullerP e a senha armazenada no $SecurePassword e armazena a credencial na variável $Credential.
Para obter mais informações, digite `Get-Help New-Object` .
O terceiro comando obtém o conjunto de disponibilidade chamado AvailabilitySet03 no grupo de recursos chamado ResourceGroup11 e armazena esse objeto na variável $AvailabilitySet.
O quarto comando cria um objeto de máquina virtual e o armazena na variável $VirtualMachine.
O comando atribui um nome e tamanho à máquina virtual.
A máquina virtual pertence ao conjunto de disponibilidade armazenado $AvailabilitySet.
Os quatro comandos a seguir atribuem valores a variáveis a ser usadas no comando a seguir.
Como você pode especificar essas cadeias de caracteres diretamente no comando **Set-AzVMOperatingSystem,** essa abordagem é usada apenas para leitura.
No entanto, você pode usar uma abordagem como esta em scripts.
O comando final define as propriedades do sistema operacional para a máquina virtual armazenada $VirtualMachine.
O comando usa as credenciais armazenadas em $Credential.
O comando usa variáveis atribuídas em comandos anteriores para alguns parâmetros.

### Exemplo 2: Definir propriedades do sistema operacional para uma nova máquina virtual com patch de hot patch habilitado
```
$SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
$AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
$VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
$ComputerName = "ContosoVM122"
$WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
$TimeZone = "Pacific Standard Time"
$CustomData = "echo 'Hello World'"
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone -PatchMode "AutomaticByPlatform" -EnableHotPatching
```

O primeiro comando converte uma senha em uma cadeia de caracteres segura e a armazena na variável $SecurePassword segurança.
Para obter mais informações, digite `Get-Help ConvertTo-SecureString` .
O segundo comando cria uma credencial para o usuário FullerP e a senha armazenada no $SecurePassword e armazena a credencial na variável $Credential.
Para obter mais informações, digite `Get-Help New-Object` .
O terceiro comando obtém o conjunto de disponibilidade chamado AvailabilitySet03 no grupo de recursos chamado ResourceGroup11 e armazena esse objeto na variável $AvailabilitySet.
O quarto comando cria um objeto de máquina virtual e o armazena na variável $VirtualMachine.
O comando atribui um nome e tamanho à máquina virtual.
A máquina virtual pertence ao conjunto de disponibilidade armazenado $AvailabilitySet.
Os quatro comandos a seguir atribuem valores a variáveis a ser usadas no comando a seguir.
Como você pode especificar essas cadeias de caracteres diretamente no comando **Set-AzVMOperatingSystem,** essa abordagem é usada apenas para leitura.
No entanto, você pode usar uma abordagem como esta em scripts.
O comando final define as propriedades do sistema operacional para a máquina virtual armazenada $VirtualMachine.
O comando usa as credenciais armazenadas em $Credential.
O comando usa variáveis atribuídas em comandos anteriores para alguns parâmetros.
O comando habilita o Hotpatching na máquina virtual.

### Exemplo 3: Definir propriedades do sistema operacional para uma nova máquina virtual Linux
```
$SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
$AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
$VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
$ComputerName = "ContosoVM122"
$CustomData = "echo 'Hello World'"
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -PatchMode "AutomaticByPlatform"
```

O primeiro comando converte uma senha em uma cadeia de caracteres segura e a armazena na variável $SecurePassword segurança.
Para obter mais informações, digite `Get-Help ConvertTo-SecureString` .
O segundo comando cria uma credencial para o usuário FullerP e a senha armazenada no $SecurePassword e armazena a credencial na variável $Credential.
Para obter mais informações, digite `Get-Help New-Object` .
O terceiro comando obtém o conjunto de disponibilidade chamado AvailabilitySet03 no grupo de recursos chamado ResourceGroup11 e armazena esse objeto na variável $AvailabilitySet.
O quarto comando cria um objeto de máquina virtual e o armazena na variável $VirtualMachine.
O comando atribui um nome e tamanho à máquina virtual.
A máquina virtual pertence ao conjunto de disponibilidade armazenado $AvailabilitySet.
Os dois comandos a seguir atribuem valores a variáveis a ser usadas no comando a seguir.
O comando final define as propriedades do sistema operacional para a máquina virtual armazenada $VirtualMachine.
O comando usa as credenciais armazenadas em $Credential.
O comando usa variáveis atribuídas em comandos anteriores para alguns parâmetros.
O comando define o valor do modo de patch na máquina virtual como "AutomaticByPlatform".

## PARÂMETROS

### -ComputerName
Especifica o nome do computador.

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

### -Credential
Especifica o nome de usuário e a senha da máquina virtual como um **objeto PSCredential.**
Para obter uma credencial, use Get-Credential cmdlet.
Para obter mais informações, digite `Get-Help Get-Credential` .

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CustomData
Especifica uma cadeia de caracteres a ser passada para a máquina virtual. Para obter mais informações, [consulte Dados Personalizados em VMs do Azure](https://docs.microsoft.com/en-us/azure/virtual-machines/custom-data).
**Observação: não é recomendável armazenar informações confidenciais em dados personalizados.**


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

### -DefaultProfile
As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.

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

### -DisablePasswordAuthentication
Indica que esse cmdlet desabilita a autenticação de senha.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DisableVMAgent
Desabilitar o Agente de VM de Provisionamento.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableAutoUpdate
Indica que esse cmdlet habilita a atualização automática.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EnableHotpatching
Permite que os clientes patch suas VMs do Azure sem exigir uma reinicialização. Para enableHotpatching, o 'provisionVMAgent' deve ser definido como true e 'patchMode' deve ser definido como 'AutomaticByPlatform'.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Linux
Indica que o tipo de sistema operacional é Linux.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PatchMode
Especifica o modo de patch no convidado para a máquina virtual IaaS.<br><br>
Os valores possíveis são:<br>
**Manual** - Você controla a aplicação de patches em uma máquina virtual. Faça isso aplicando patches manualmente dentro da VM. Nesse modo, as atualizações automáticas são desabilitadas; a propriedade WindowsConfiguration.enableAutomaticUpdates deve ser false<br>
**AutomaticByOS** - A máquina virtual será atualizada automaticamente pelo sistema operacional. A propriedade WindowsConfiguration.enableAutomaticUpdates deve ser true. <br >
**AutomaticByPlatform** - a máquina virtual será atualizada automaticamente pelo sistema operacional. As propriedades provisionVMAgent e WindowsConfiguration.enableAutomaticUpdates devem ser verdadeiras

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ProvisionVMAgent
Indica que as configurações exigem que o agente da máquina virtual seja instalado na máquina virtual.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TimeZone
Especifica o fuso horário da máquina virtual. Por exemplo, Hora \" Padrão do Pacífico \" . <br>
Os valores possíveis podem [TimeZoneInfo.Id](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) de fusos horário retornados por [TimeZoneInfo.GetSystemTimeZones](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.getsystemtimezones).

```yaml
Type: System.String
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Especifica o objeto da máquina virtual local no qual definir as propriedades do sistema operacional.
Para obter um objeto de máquina virtual, use Get-AzVM cmdlet.
Crie um objeto de máquina virtual usando o New-AzVMConfig cmdlet.

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Windows
Indica que o tipo de sistema operacional é o Windows.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WinRMCertificateUrl
Especifica o URI de um certificado WinRM.
Isso precisa ser armazenado em um Cofre de Chaves.

```yaml
Type: System.Uri
Parameter Sets: WindowsWinRmHttps, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: True
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WinRMHttp
Indica que esse sistema operacional usa HTTP WinRM.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WinRMHttps
Indica que esse sistema operacional usa HTTPS WinRM.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsWinRmHttps, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: True
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

### System.Management.Automation.SwitchParameter

### System.String

### System.Management.Automation.PSCredential

### System.Uri

## SAÍDAS

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

## NOTES

## LINKS RELACIONADOS

[Get-AzVM](./Get-AzVM.md)

[New-AzVMConfig](./New-AzVMConfig.md)


