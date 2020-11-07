---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: AA58B897-EFA0-4321-9246-ED8E11AB3538
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7a0e0d5cac7ac27bf7eeefe8e3eb995a82a32ea4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945982"
---
# New-AzureSSHKey

## Sinopse
Cria um objeto chave SSH para inserir um certificado existente em uma nova máquina virtual do Azure com base em Linux.

## SYNTAX

### par de chaves
```
New-AzureSSHKey [-KeyPair] [-Fingerprint] <String> [-Path] <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### PublicKey
```
New-AzureSSHKey [-PublicKey] [-Fingerprint] <String> [-Path] <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzureSSHKey** cria um objeto chave SSH para um certificado que já foi adicionado ao Azure.
Esse objeto chave SSH pode ser usado por **New-AzureProvisioningConfig** ao criar o objeto de configuração para uma nova máquina virtual usando **New-AzureVM** ou ao criar uma nova máquina virtual com **New-AzureQuickVM**.
Quando incluída como parte de um script de criação de máquina virtual, isso adiciona a chave pública SSH ou par de chaves especificado à nova máquina virtual.

## EXEMPLOS

### Exemplo 1: criar um objeto de configuração de certificado
```
PS C:\> $myLxCert = New-AzureSSHKey -Fingerprint "D7BECD4D63EBAF86023BB4F1A5FBF5C2C924902A" -Path "/home/username/.ssh/authorized_keys"
```

Esse comando cria um objeto de configuração de certificado para um certificado existente e, em seguida, armazena o objeto em uma variável para uso posterior.

### Exemplo 2: adicionar um certificado a um serviço
```
PS C:\> Add-AzureCertificate -ServiceName "MySvc" -CertToDeploy "C:\temp\MyLxCert.cer"
$myLxCert = New-AzureSSHKey ?Fingerprint "D7BECD4D63EBAF86023BB4F1A5FBF5C2C924902A" -Path "/home/username/.ssh/authorized_keys"
New-AzureVMConfig -Name "MyVM2" -InstanceSize Small -ImageName $LxImage `
          | Add-AzureProvisioningConfig -Linux -LinuxUser $lxUser -SSHPublicKeys $myLxCert -Password 'pass@word1' `
          | New-AzureVM -ServiceName "MySvc"
```

Esse comando adiciona um certificado a um serviço do Azure e, em seguida, cria uma nova máquina virtual Linux que usa o certificado.

## OS

### -Impressão digital
Especifica a impressão digital do certificado.

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

### -Par de chaves
Especifica que esse cmdlet cria um objeto para a inserção de um par de chaves SSH na nova configuração de máquina virtual.

```yaml
Type: SwitchParameter
Parameter Sets: keypair
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Caminho
Especifica o caminho para armazenar a chave pública SSH ou par de chaves.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicKey
Especifica que esse cmdlet cria um objeto para a inserção de uma chave pública SSH na nova configuração de máquina virtual.

```yaml
Type: SwitchParameter
Parameter Sets: publickey
Aliases: 

Required: True
Position: 0
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

[Add-AzureProvisioningConfig](./Add-AzureProvisioningConfig.md)

[New-AzureVMConfig](./New-AzureVMConfig.md)

[New-AzureVM](./New-AzureVM.md)

[New-AzureQuickVM](./New-AzureQuickVM.md)


