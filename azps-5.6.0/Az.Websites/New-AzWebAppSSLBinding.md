---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 910239BE-9E48-4DC5-85EA-CC6D466FE62F
online version: https://docs.microsoft.com/powershell/module/az.websites/new-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSSLBinding.md
ms.openlocfilehash: 3429868b1d603606f64c75ec23505cf63f9ade03
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891545"
---
# New-AzWebAppSSLBinding

## SYNOPSIS
Cria uma associação de certificado SSL para um Aplicativo Web do Azure.

## SINTAXE

### S1
```
New-AzWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>] [-Name] <String>
 [[-SslState] <SslState>] [-CertificateFilePath] <String> [-CertificatePassword] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### S2
```
New-AzWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>] [-Name] <String>
 [[-SslState] <SslState>] [-Thumbprint] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### S3
```
New-AzWebAppSSLBinding [-WebApp] <PSSite> [-Name] <String> [[-SslState] <SslState>]
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### S4
```
New-AzWebAppSSLBinding [-WebApp] <PSSite> [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIPTION
O cmdlet **New-AzWebAppSSLBinding** cria uma associação de certificado SSL (Secure Socket Layer) para um Aplicativo Web do Azure.
O cmdlet cria uma associação SSL de duas maneiras: 
- Você pode vincular um Aplicativo Web a um certificado existente.
- Você pode carregar um novo certificado e, em seguida, vincular o Aplicativo Web a esse novo certificado.
Independentemente da abordagem usada, o certificado e o Aplicativo Web devem estar associados ao mesmo grupo de recursos do Azure.
Se você tiver um Aplicativo Web no Grupo de Recursos A e quiser vincular esse Aplicativo Web a um certificado no Grupo de Recursos B, a única maneira de fazer isso é carregar uma cópia do certificado para o Grupo de Recursos A. Se você carregar um novo certificado, lembre-se dos seguintes requisitos para um certificado SSL do Azure: 
- O certificado deve conter uma chave privada. 
- O certificado deve usar o formato PFX (Personal Information Exchange). 
- O nome de assunto do certificado deve corresponder ao domínio usado para acessar o Aplicativo Web. 
- O certificado deve usar um mínimo de criptografia de 2048 bits.

## EXEMPLOS

### Exemplo 1: vincular um certificado a um aplicativo Web
```powershell
PS C:\>New-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" -Name "www.contoso.com"
```

Este comando vincula um certificado existente do Azure (um certificado com a impressão digital E3A38EBA60CAA1C162785A2E1C44A15AD450199C3) ao aplicativo Web chamado ContosoWebApp.

### Exemplo 2

Cria uma associação de certificado SSL para um Aplicativo Web do Azure. (gerado automaticamente)

```powershell <!-- Aladdin Generated Example --> 
New-AzWebAppSSLBinding -Name 'www.contoso.com' -ResourceGroupName 'ContosoResourceGroup' -SslState Disabled -Thumbprint 'E3A38EBA60CAA1C162785A2E1C44A15AD450199C3' -WebAppName 'ContosoWebApp'
```

## PARÂMETROS

### -CertificateFilePath
Especifica o caminho do arquivo para o certificado a ser carregado.
O *parâmetro CertificateFilePath* só será necessário se o certificado ainda não tiver sido carregado no Azure.

```yaml
Type: System.String
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
Type: System.String
Parameter Sets: S1, S3
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: False
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

### -Name
Especifica o nome do Aplicativo Web.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome do grupo de recursos ao que o certificado é atribuído.
Não é possível usar o *parâmetro ResourceGroupName* e o *parâmetro WebApp* no mesmo comando.

```yaml
Type: System.String
Parameter Sets: S1, S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Slot
Especifica o nome do slot de implantação do Web App.
Você pode usar o cmdlet Get-AzWebAppSlot para obter um slot.
Os slots de implantação fornecem uma maneira de você fazer estágios e validar aplicativos Web sem que esses aplicativos sejam acessíveis pela Internet.
Normalmente, você implantará suas alterações em um site de preparação, validará essas alterações e implantará no site de produção (acessível à Internet).

```yaml
Type: System.String
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
Defina o *parâmetro SSLState* como 1 para habilitar o certificado ou defina *SSLState* como 0 para desabilitar o certificado.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.WebSites.Models.SslState]
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, SniEnabled, IpBasedEnabled

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Thumbprint
Especifica o identificador exclusivo do certificado.

```yaml
Type: System.String
Parameter Sets: S2, S4
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WebApp
Especifica um Aplicativo Web.
Para obter um Aplicativo Web, use o Get-AzWebApp cmdlet.
Não é possível usar o *parâmetro WebApp* no mesmo comando que o *parâmetro ResourceGroupName* e/ou *o WebAppName*.

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S3, S4
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WebAppName
Especifica o nome do Aplicativo Web para o qual a nova associação SSL está sendo criada.
Não é possível usar o *parâmetro WebAppName* e o *parâmetro WebApp* no mesmo comando.

```yaml
Type: System.String
Parameter Sets: S1, S2
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Commands.WebApps.Models.PSSite

## SAÍDAS

### Microsoft.Azure.Management.WebSites.Models.HostNameSslState

## NOTES

## LINKS RELACIONADOS

[Get-AzWebAppSSLBinding](./Get-AzWebAppSSLBinding.md)

[Remove-AzWebAppSSLBinding](./Remove-AzWebAppSSLBinding.md)

[Get-AzWebAppSlot](./Get-AzWebAppSlot.md)

[Get-AzWebApp](./Get-AzWebApp.md)


