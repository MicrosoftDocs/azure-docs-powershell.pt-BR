---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 11919623-9EDF-42A3-93FE-54E93D76D3D0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7492dbdea0f924e364ac1acf5ce30476e34782d6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945932"
---
# New-AzureCertificateSetting

## Sinopse
Cria um objeto de configuração de certificado para um certificado em um serviço.

## SYNTAX

```
New-AzureCertificateSetting [[-StoreName] <String>] [-Thumbprint] <String>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzureCertificateSetting** cria um objeto de configuração de certificado para um certificado que está em um serviço do Azure.

Você pode usar um objeto de configuração de certificado para criar um objeto de configuração usando o cmdlet **Add-AzureProvisioningConfig** .
Use um objeto de configuração para criar a máquina virtual usando o cmdlet **New-AzureVM** .
Você pode usar um objeto de configuração de certificado para criar uma máquina virtual usando o cmdlet **New-AzureQuickVM** .

## EXEMPLOS

### Exemplo 1: criar um objeto de configuração de certificado
```
PS C:\> New-AzureCertificateSetting -Thumbprint "D7BECD4D63EBAF86023BB41FA5FBF5C2C924902A" -StoreName "My"
```

Esse comando cria um objeto de configuração de certificado para um certificado existente.

### Exemplo 2: criar uma máquina virtual que usa um objeto de configuração de configuração
```
PS C:\> Add-AzureCertificate -ServiceName "ContosoService" -CertToDeploy "C:\temp\ContosoCert.cer"
PS C:\> $CertificateSetting = New-AzureCertificateSetting -Thumbprint "D7BECD4D63EBAF86023BB41FA5FBF5C2C924902A" -StoreName "My" 
PS C:\> $Image = Get-AzureVMImage -ImageName "ContosoStandard"
PS C:\> New-AzureVMConfig -Name "VirtualMachine17" -InstanceSize Small -ImageName $Image | Add-AzureProvisioningConfig -Windows -Certificates $CertificateSetting -Password "password" | New-AzureVM -ServiceName "ContosoService"
```

O primeiro comando adiciona o certificado ContosoCert. cer ao serviço chamado ContosoService usando o cmdlet **Add-AzureCertificate** .

O segundo comando cria um objeto de configuração de certificado e, em seguida, armazena-o na variável $CertificateSetting.

O terceiro comando obtém uma imagem do repositório de imagens usando o cmdlet **Get-AzureVMImage** .
Esse comando armazena a imagem na variável $Image.

O comando final cria um objeto de configuração de máquina virtual com base na imagem no $Image usando o cmdlet **New-AzureVMConfig** .
O comando passa esse objeto para o cmdlet **Add-AzureProvisioningConfig** usando o operador pipeline.
Esse cmdlet adiciona informações de provisionamento à configuração.
O comando passa o objeto para o cmdlet **New-AzureVM** , que cria a máquina virtual.

## OS

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

### -StoreName
Especifica o repositório de certificados no qual colocar o certificado.
Os valores válidos são: 

- Agenda
- AuthRoot
- CertificateAuthority
- Não permitidas
- Meu
- Raiz
- TrustedPeople
- TrustedPublisher

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

## INFORMA

## LINKS RELACIONADOS

[Add-AzureCertificate](./Add-AzureCertificate.md)

[Add-AzureProvisioningConfig](./Add-AzureProvisioningConfig.md)

[Get-AzureCertificate](./Get-AzureCertificate.md)

[Get-AzureVMImage](./Get-AzureVMImage.md)

[New-AzureQuickVM](./New-AzureQuickVM.md)

[New-AzureVM](./New-AzureVM.md)

[Remove-AzureCertificate](./Remove-AzureCertificate.md)


