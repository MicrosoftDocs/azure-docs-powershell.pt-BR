---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 50B64FFE-8277-4DAA-805A-271123B35355
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmadditionalunattendcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMAdditionalUnattendContent.md
ms.openlocfilehash: 05f100e730cb808bf40bbec60386901eb39020ce
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117884"
---
# Add-AzVMAdditionalUnattendContent

## Sinopse
Adiciona informações ao arquivo de resposta de configuração autônoma do Windows.

## Sintaxe

```
Add-AzVMAdditionalUnattendContent [-VM] <PSVirtualMachine> [[-Content] <String>]
 [[-SettingName] <SettingNames>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrição
O **cmdlet Add-AzVMAdditionalUnattendContent** adiciona informações ao arquivo de resposta de configuração autônoma do Windows.
Especifique informações adicionais codificadas .xml codificadas de base 64 que este cmdlet adiciona ao arquivo unattend.xml arquivo.

## Exemplos

### Exemplo 1: Adicionar conteúdo ao unattend.xml
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $AucContent = "<UserAccounts><AdministratorPassword><Value>" + "Password" + "</Value><PlainText>true</PlainText></AdministratorPassword></UserAccounts>";
PS C:\> $VirtualMachine = Add-AzVMAdditionalUnattendContent -VM $VirtualMachine -Content $AucContent -SettingName "AutoLogon"
```

O primeiro comando obtém o conjunto de disponibilidade chamado AvailabilitySet03 no grupo de recursos chamado ResourceGroup11 e armazena esse objeto na variável $AvailabilitySet.
O segundo comando cria um objeto virtual de máquina e o armazena na variável $VirtualMachine dados.
O comando atribui um nome e um tamanho à máquina virtual.
A máquina virtual pertence ao conjunto de disponibilidade armazenado em $AvailabilitySet.
O terceiro comando cria um objeto de credencial usando o cmdlet Get-Credential e armazena o resultado na variável $Credential dados.
O comando solicita um nome de usuário e senha.
Para obter mais informações, digite `Get-Help Get-Credential` .
O quarto comando usa **o cmdlet Set-AzVMOperatingSystem** para configurar a máquina virtual armazenada no $VirtualMachine.
O quinto comando atribui conteúdo à variável $AucContent dados.
O conteúdo inclui uma senha.
O comando final adiciona o conteúdo armazenado no $AucContent ao unattend.xml arquivo.

## Parâmetros

### -Conteúdo
Especifica o conteúdo xml codificado da base 64.
Este cmdlet adiciona o conteúdo ao arquivo unattend.xml arquivo.
O conteúdo XML deve ser menor que 4 KB e deve incluir o elemento raiz para a configuração ou recurso que esse cmdlet insere.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.

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

### -SettingName
Especifica o nome da configuração à qual o conteúdo se aplica.
Os valores aceitáveis para este parâmetro são:
- FirstLogonCommands
- Autologon

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.SettingNames]
Parameter Sets: (All)
Aliases:
Accepted values: AutoLogon, FirstLogonCommands

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Especifica o objeto de máquina virtual que este cmdlet modifica.
Para obter um objeto de máquina virtual, use [o cmdlet Get-AzVM.](./Get-AzVM.md)
Crie um objeto de máquina virtual usando [o cmdlet New-AzVMConfig.](./New-AzVMConfig.md)

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

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## Entradas

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

### System.String

### System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.SettingNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]

## Saídas

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

## Notas

## LINKS RELACIONADOS

[Get-AzAvailabilitySet](./Get-AzAvailabilitySet.md)

[Set-AzVMOperatingSystem](./Set-AzVMOperatingSystem.md)

[New-AzVMConfig](./New-AzVMConfig.md)
