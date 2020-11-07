---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E712421A-FA69-46E7-A0DE-F2734D767F2D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8355e0a1d36a6c1dc5b2ca8172cde5bf94480bbe
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946532"
---
# Get-AzureVMImage

## Sinopse
Obtém as propriedades em um ou em uma lista de sistemas operacionais ou em uma imagem de máquina virtual no repositório de imagens.

## SYNTAX

```
Get-AzureVMImage [[-ImageName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureVMImage** Obtém Propriedades em um ou uma lista de sistemas operacionais ou uma imagem de máquina virtual no repositório de imagens.
O cmdlet retorna informações de todas as imagens no repositório ou de uma imagem específica se o nome da imagem for fornecido.

## EXEMPLOS

### Exemplo 1: obter um objeto de imagem específico do repositório de imagens atual.
```
PS C:\> Get-AzureVMImage -ImageName Image001
```

Esse comando obtém o objeto Image chamado Image001 do repositório de imagens atual.

### Exemplo 2: obter todas as imagens do repositório de imagens atual
```
PS C:\> Get-AzureVMImage
```

Esse comando recupera todas as imagens do repositório de imagens atual.

### Exemplo 3: definir o contexto de assinatura e obter todas as imagens
```
PS C:\> $SubsId = <MySubscriptionID>
C:\PS>$Cert = Get-AzureCertificate cert:\LocalMachine\MY\<CertificateThumbprint>
C:\PS>$MyOSImages = Get-AzureVMImage
```

Esse comando define o contexto da assinatura e recupera todas as imagens do repositório de imagens.

## OS

### -ImageName
Especifica o nome da imagem do sistema operacional ou da máquina virtual no repositório de imagens.
Se você não especificar esse parâmetro, todas as imagens serão retornadas.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

## INFORMA

## LINKS RELACIONADOS

[Add-AzureVMImage](./Add-AzureVMImage.md)

[Remove-AzureVMImage](./Remove-AzureVMImage.md)

[Save-AzureVMImage](./Save-AzureVMImage.md)

[Update-AzureVMImage](./Update-AzureVMImage.md)


