---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 910239BE-9E48-4DC5-85EA-CC6D466FE62F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappsslbinding
schema: 2.0.0
ms.openlocfilehash: 0a396b93a0ce1435302b1ee2f81d8700ec10a60d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786366"
---
# New-AzureRmWebAppSSLBinding

## Sinopse
Cria uma associação de certificado SSL para um aplicativo Web do Azure.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### Eles
```
New-AzureRmWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-Name] <String> [[-SslState] <SslState>] [-CertificateFilePath] <String> [-CertificatePassword] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### S2
```
New-AzureRmWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### S3
```
New-AzureRmWebAppSSLBinding [-WebApp] <Site> [-Name] <String> [[-SslState] <SslState>]
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### S4
```
New-AzureRmWebAppSSLBinding [-WebApp] <Site> [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzureRmWebAppSSLBinding** cria uma associação de certificado SSL (Secure Socket Layer) para um aplicativo Web do Azure.
O cmdlet cria uma associação SSL de duas maneiras: 

- Você pode associar um aplicativo Web a um certificado existente.
- Você pode carregar um novo certificado e, em seguida, associar o aplicativo Web a esse novo certificado.

Independentemente da abordagem que você usa, o certificado e o aplicativo Web devem estar associados ao mesmo grupo de recursos do Azure.
Se você tiver um aplicativo Web no grupo de recursos A e quiser associar esse aplicativo Web a um certificado no grupo de recursos B, a única maneira de fazer isso é carregar uma cópia do certificado para o grupo de recursos A.

Se você carregar um novo certificado, lembre-se dos seguintes requisitos para um certificado SSL do Azure: 

- O certificado deve conter uma chave privada. 
- O certificado deve usar o formato PFX (troca de informações pessoais). 
- O nome do requerente do certificado deve corresponder ao domínio usado para acessar o aplicativo Web. 
- O certificado deve usar uma criptografia mínima de 2048 bits.

## EXEMPLOS

### Exemplo 1: associar um certificado a um aplicativo Web
```
PS C:\>New-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" -Name "www.contoso.com"
```

Esse comando associa um certificado existente do Azure (um certificado com o E3A38EBA60CAA1C162785A2E1C44A15AD450199C3 de impressão digital) ao aplicativo Web chamado ContosoWebApp.

## OS

### -CertificateFilePath
Especifica o caminho do arquivo para o certificado a ser carregado.

O parâmetro *CertificateFilePath* será necessário apenas se o certificado ainda não tiver sido carregado no Azure.

```yaml
Type: String
Parameter Sets: S1, S3
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificatePassword
Especifica a senha de descriptografia do certificado.

```yaml
Type: String
Parameter Sets: S1, S3
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
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

### -Nome
Especifica o nome do aplicativo Web.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome do grupo de recursos ao qual o certificado está atribuído.

Não é possível usar o parâmetro *ResourceGroupName* e o parâmetro *webapp* no mesmo comando.

```yaml
Type: String
Parameter Sets: S1, S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Slot
Especifica o nome do slot de implantação do aplicativo Web.
Você pode usar o cmdlet Get-AzureRMWebAppSlot para obter um slot.

Os slots de implantação fornecem uma maneira de testar e validar aplicativos Web sem esses aplicativos serem acessíveis pela Internet.
Normalmente, você implantará as alterações em um site temporário, validará essas alterações e, em seguida, implantará no site de produção (acessível à Internet).

```yaml
Type: String
Parameter Sets: S1, S2
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SslState
Especifica se o certificado está habilitado.
Defina o parâmetro *SSLState* como 1 para habilitar o certificado ou defina *SSLState* como 0 para desabilitar o certificado.

```yaml
Type: SslState
Parameter Sets: (All)
Aliases: 
Accepted values: Disabled, SniEnabled, IpBasedEnabled

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Impressão digital
Especifica o identificador exclusivo do certificado.

```yaml
Type: String
Parameter Sets: S2, S4
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WebApp
Especifica um aplicativo Web.
Para obter um aplicativo Web, use o cmdlet Get-AzureRmWebApp.

Não é possível usar o parâmetro *webapp* no mesmo comando que o parâmetro *ResourceGroupName* e/ou o *webappname*.

```yaml
Type: Site
Parameter Sets: S3, S4
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WebAppname
Especifica o nome do aplicativo Web para o qual a nova associação SSL está sendo criada.

Não é possível usar o parâmetro *webappname* e o parâmetro *webapp* no mesmo comando.

```yaml
Type: String
Parameter Sets: S1, S2
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

### Instalação
O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline

## EXIBE

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmWebAppSSLBinding](./Get-AzureRmWebAppSSLBinding.md)

[Remove-AzureRmWebAppSSLBinding](./Remove-AzureRmWebAppSSLBinding.md)

[Get-AzureRMWebAppSlot](./Get-AzureRMWebAppSlot.md)

[Get-AzureRmWebApp](./Get-AzureRmWebApp.md)


