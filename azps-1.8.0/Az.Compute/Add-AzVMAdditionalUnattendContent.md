---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 50B64FFE-8277-4DAA-805A-271123B35355
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmadditionalunattendcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMAdditionalUnattendContent.md
ms.openlocfilehash: d5c84aab35b2c8dbbc6a3d1479a194ae9df827de
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771250"
---
# Add-AzVMAdditionalUnattendContent

## Sinopse
Adiciona informações ao arquivo de resposta da instalação autônoma do Windows.

## SYNTAX

```
Add-AzVMAdditionalUnattendContent [-VM] <PSVirtualMachine> [[-Content] <String>]
 [[-SettingName] <SettingNames>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Add-AzVMAdditionalUnattendContent** adiciona informações ao arquivo de resposta da instalação autônoma do Windows.
Especifique as informações formatadas. XML adicionais de base 64 codificadas que esse cmdlet adiciona ao arquivo unattend.xml.

## EXEMPLOS

### Exemplo 1: adicionar conteúdo a unattend.xml
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $AucContent = "<UserAccounts><AdministratorPassword><Value>" + "Password" + "</Value><PlainText>true</PlainText></AdministratorPassword></UserAccounts>";
PS C:\> $VirtualMachine = Add-AzVMAdditionalUnattendContent -VM $VirtualMachine -Content $AucContent -SettingName "AutoLogon"
```

O primeiro comando obtém o conjunto de disponibilidade chamado AvailablitySet03 no grupo de recursos chamado ResourceGroup11 e, em seguida, armazena esse objeto na variável $AvailabilitySet.
O segundo comando cria um objeto de máquina virtual e, em seguida, armazena-o na variável $VirtualMachine.
O comando atribui um nome e um tamanho para a máquina virtual.
A máquina virtual pertence ao conjunto de disponibilidade armazenado em $AvailabilitySet.
O terceiro comando cria um objeto Credential usando o cmdlet Get-Credential e armazena o resultado na variável $Credential.
O comando solicita um nome de usuário e uma senha.
Para obter mais informações, digite `Get-Help Get-Credential` .
O quarto comando usa o cmdlet **set-AzVMOperatingSystem** para configurar a máquina virtual armazenada em $VirtualMachine.
O quinto comando atribui conteúdo à variável $AucContent.
O conteúdo inclui uma senha.
O comando final adiciona o conteúdo armazenado em $AucContent ao arquivo unattend.xml.

## OS

### -Conteúdo
Especifica conteúdo formatado XML em base 64.
Esse cmdlet adiciona o conteúdo ao arquivo unattend.xml.
O conteúdo XML deve ter menos de 4 KB e deve incluir o elemento raiz para a configuração ou o recurso que esse cmdlet insere.

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

### -SettingName
Especifica o nome da configuração à qual o conteúdo se aplica.
Os valores aceitáveis para esse parâmetro são:
- FirstLogonCommands
- Logon automático

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
Especifica o objeto da máquina virtual que esse cmdlet modifica.
Para obter um objeto de máquina virtual, use o cmdlet [Get-AzVM](./Get-AzVM.md) .
Crie um objeto de máquina virtual usando o cmdlet [New-AzVMConfig](./New-AzVMConfig.md) .

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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine

### System. String

### System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. Models. Settingnames, Microsoft. Azure. Management. Compute, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]

## EXIBE

### Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine

## INFORMA

## LINKS RELACIONADOS

[Get-AzAvailabilitySet](./Get-AzAvailabilitySet.md)

[Set-AzVMOperatingSystem](./Set-AzVMOperatingSystem.md)

[New-AzVMConfig](./New-AzVMConfig.md)
