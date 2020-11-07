---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: BFD4E4AD-8F1B-4E4E-BF52-435A6EEAA060
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6beed021bfc12db3a3fdb1a66ee8ae6fe2e1e9b9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945955"
---
# Set-AzurePublicIP

## Sinopse
Adiciona um IP público a uma máquina virtual do Azure.

## SYNTAX

```
Set-AzurePublicIP [-PublicIPName] <String> [[-IdleTimeoutInMinutes] <Int32>] [[-DomainNameLabel] <String>]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzurePublicIP** adiciona um IP público a uma máquina virtual do Azure.
Se você executar esse cmdlet para uma máquina virtual existente, atualize a máquina virtual para implementá-las.
Você pode especificar um rótulo de nome de domínio para criar uma entrada de DNS correspondente para o IP público.

## EXEMPLOS

### Exemplo 1: adicionar um IP público a uma máquina virtual existente
```
PS C:\> Get-AzureVM -ServiceName "FTPInAzure" -Name "FTPInstance" | Set-AzurePublicIP -PublicIPName "ftpip" | Update-AzureVM
```

Esse comando obtém a máquina virtual chamada FTPInstance no serviço chamado FTPInAzure usando o cmdlet **Get-AzureVM** .
O comando transmite a máquina virtual para o cmdlet atual usando o operador pipeline.
O cmdlet atual adiciona a ftpip do nome do IP público.
O comando passa a máquina virtual para o cmdlet **Update-AzureVM** , que implementa suas alterações.

### Exemplo 2: adicionar um IP público a uma nova máquina virtual
```
PS C:\> New-AzureVMConfig -Name "FTPInstance" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -AdminUsername "AdminMain" -Password "password" | Set-AzurePublicIP -PublicIPName "ftpip" | New-AzureVM -ServiceName "FTPinAzure" -Location "North Central US"
```

Esse comando cria um objeto de configuração de máquina virtual usando o cmdlet **New-AzureVMConfig** .
O comando passa esse objeto para o cmdlet **Add-AzureProvisioningConfig** , que fornece configuração adicional.
O cmdlet atual adiciona a ftpip do nome do IP público.
O comando passa a configuração para o cmdlet **New-AzureVM** , que cria a máquina virtual.

### Exemplo 3: adicionar um IP público e um rótulo a uma máquina virtual existente
```
PS C:\> Get-AzureVM -ServiceName "FTPInAzure" -Name "FTPInstance" | Set-AzurePublicIP -PublicIPName "ftpip" -DomainNameLabel "ipname" | Update-AzureVM
```

Esse comando obtém a máquina virtual chamada FTPInstance no serviço chamado FTPInAzure usando o cmdlet **Get-AzureVM** .
O comando transmite a máquina virtual para o cmdlet atual usando o operador pipeline.
O cmdlet atual adiciona o ftpip de nomes de IP público e o rótulo ipname.
O comando atualiza a máquina virtual, que implementa suas alterações.

### Exemplo 4: adicionar um IP público e um rótulo a uma nova máquina virtual
```
PS C:\> New-AzureVMConfig -Name "FTPInstance" -InstanceSize Small -ImageName $images[50].ImageName | Add-AzureProvisioningConfig -Windows -AdminUsername "AdminMain" -Password "password" | Set-AzurePublicIP -PublicIPName "ftpip" -DomainNameLabel "ipname" | New-AzureVM -ServiceName "FTPinAzure" -Location "North Central US"
```

Esse comando cria um objeto de configuração de máquina virtual e, em seguida, passa esse objeto para **Add-AzureProvisioningConfig** , que fornece configuração adicional.
O cmdlet atual adiciona o ftpip de nomes de IP público e o rótulo ipname.
O comando cria a máquina virtual.

## OS

### -DomainNameLabel
Especifica o nome a ser usado para uma entrada DNS correspondente para o endereço IP público.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IdleTimeoutInMinutes
Especifica o período de tempo limite de TCP ocioso em minutos.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Informationaction
Especifica como esse cmdlet responde a um evento de informações.

Os valores aceitáveis para esse parâmetro são:

- Contínuo
- Ignorar
- Inquire
- SilentlyContinue
- Finaliza
- Suspensão

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Especifica uma variável de informações.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

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

### -PublicIPName
Especifica o nome do IP público.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
Especifica a máquina virtual para a qual esse cmdlet adiciona o IP público.

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

### Microsoft. WindowsAzure. Commands. onmanagement. Model. IPersistentVM

## INFORMA

## LINKS RELACIONADOS

[Get-AzurePublicIP](./Get-AzurePublicIP.md)

[Get-AzureVM](./Get-AzureVM.md)

[New-AzureVM](./New-AzureVM.md)

[New-AzureVMConfig](./New-AzureVMConfig.md)

[Remove-AzurePublicIP](./Remove-AzurePublicIP.md)

[Update-AzureVM](./Update-AzureVM.md)


