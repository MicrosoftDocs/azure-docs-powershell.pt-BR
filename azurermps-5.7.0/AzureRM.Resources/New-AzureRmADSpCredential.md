---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 063BAA79-484D-48CF-9170-3808813752BD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADSpCredential.md
ms.openlocfilehash: bf2a42df42a343d9745cb55f4d72463513b44dc3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431628"
---
# New-AzureRmADSpCredential

## Sinopse
Adiciona uma credencial a uma entidade de serviço existente.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### SpObjectIdWithPasswordParameterSet (padrão)
```
New-AzureRmADSpCredential -ObjectId <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SpObjectIdWithCertValueParameterSet
```
New-AzureRmADSpCredential -ObjectId <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SPNWithCertValueParameterSet
```
New-AzureRmADSpCredential -ServicePrincipalName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SPNWithPasswordParameterSet
```
New-AzureRmADSpCredential -ServicePrincipalName <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet New-AzureRmADSpCredential pode ser usado para adicionar uma nova credencial ou para rolar credenciais para uma entidade de serviço.
A entidade de serviço é identificada fornecendo a identificação do objeto ou o nome da entidade de serviço.

## EXEMPLOS

### Exemplo 1
```
PS E:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS E:\> New-AzureRmADSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 -Password $SecureStringPassword
```

Uma nova credencial de senha é adicionada a uma entidade de serviço existente.
Neste exemplo, o valor de senha fornecido é adicionado à entidade de serviço usando o objectId.

### Exemplo 2
```
$cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate 

$cer.Import("C:\myapp.cer") 

$binCert = $cer.GetRawCertData() 

$credValue = [System.Convert]::ToBase64String($binCert)

PS E:\> New-AzureRmADSpCredential -ServicePrincipalName "http://test123" -CertValue $credValue -StartDate $cer.GetEffectiveDateString() -EndDate $cer.GetExpirationDateString()
```

Uma nova credencial de chave é adicionada a uma entidade de serviço existente.
Neste exemplo, o certificado X509 público codificado em base64 fornecido ("MyApp. cer") é adicionado à entidade de serviço usando seu SPN.

### Exemplo 3

```
PS E:\> New-AzureRmADSpCredential -ServicePrincipalName "http://test123" -CertValue $credValue
```

## OS

### -Certvalue
O valor do tipo de credencial "assimétricod".
Ele representa o certificado codificado básico do 64.

```yaml
Type: String
Parameter Sets: SpObjectIdWithCertValueParameterSet, SPNWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure

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

### -EndDate
A data de término efetiva do uso da credencial.
O valor padrão de data de término é um ano a partir de hoje. Para uma credencial de tipo "assimétrico", deve ser definida como at ou antes da data em que o certificado X509 é válido.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ObjectId
A ID de objeto da entidade de serviço para a qual as credenciais são adicionadas.

```yaml
Type: String
Parameter Sets: SpObjectIdWithPasswordParameterSet, SpObjectIdWithCertValueParameterSet
Aliases: ServicePrincipalObjectId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Senha
A senha a ser associada ao aplicativo.

```yaml
Type: SecureString
Parameter Sets: SpObjectIdWithPasswordParameterSet, SPNWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Serviceprincipalnamename
O nome (SPN) da entidade de serviço para a qual adicionar as credenciais.

```yaml
Type: String
Parameter Sets: SPNWithCertValueParameterSet, SPNWithPasswordParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StartDate
A data de início efetiva do uso da credencial.
O valor da data de início padrão é hoje. Para uma credencial de tipo "assimétrico", isso deve ser definido como ligado ou posterior à data a partir da qual o certificado X509 é válido.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirme
Solicita confirmação antes de executar o cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma
Esse cmdlet não aceita nenhuma entrada.

## EXIBE

### Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmADSpCredential](./Get-AzureRmADSpCredential.md)

[Remove-AzureRmADSpCredential](./Remove-AzureRmADSpCredential.md)

[Get-AzureRmADServicePrincipal](./Get-AzureRmADServicePrincipal.md)



