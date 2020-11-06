---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D857FF6-A27D-4031-948D-8A69D24B4AD4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRootCertificate.md
ms.openlocfilehash: ad000878256eea429582881be90e2b15156015d4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600088"
---
# Remove-AzVpnClientRootCertificate

## Sinopse
Remove um certificado raiz de cliente VPN existente.

## SYNTAX

```
Remove-AzVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Remove-AzVpnClientRootCertificate** remove o certificado raiz especificado de um gateway de rede virtual.
Os certificados raiz são certificados X. 509 que identificam a autoridade de certificação raiz: todos os outros certificados usados no gateway confiam no certificado raiz.
Se você remover um certificado raiz que usa o certificado para fins de autenticação, ele não poderá mais se conectar ao gateway.
Ao usar **Remove-AzVpnClientRootCertificate** , você deve fornecer o nome do certificado e uma representação de texto dos dados do certificado.
Para obter mais informações sobre a representação de texto de um certificado, consulte a descrição do parâmetro *PublicCertData* .

## EXEMPLOS

### Exemplo 1: remover um certificado raiz de cliente de um gateway de rede virtual
```
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Remove-AzVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway"-VpnClientRootCertificateName "ContosoRootCertificate"
```

Este exemplo remove um certificado raiz de cliente chamado ContosoRootCertificate do gateway de rede virtual ContosoVirtualGateway.
O primeiro comando usa o cmdlet **Get-Content** para obter uma representação de texto exportado anteriormente do certificado; Essa representação de texto é armazenada em uma variável chamada $Text.
Em seguida, o segundo comando usa um loop for para extrair todo o texto no $Text, exceto a primeira linha e a última linha.
Esse texto extraído é armazenado em uma variável chamada $CertificateText.
O terceiro comando usa as informações armazenadas na variável $CertificateText juntamente com o cmdlet **Remove-AzVpnClientRootCertificate** para remover o certificado do gateway.

## OS

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

### -PublicCertData
Especifica a representação de texto do certificado raiz a ser removido.
Para obter a representação de texto, exporte seu certificado no formato. cer (usando a codificação Base64) e, em seguida, abra o arquivo resultante em um editor de texto.
Você deve ver uma saída semelhante à seguinte (Observe que a saída real conterá muito mais linhas de texto do que a amostra abreviada mostrada aqui):-----iniciar o certificado-----MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w-----fim do certificado-----o PublicCertData é composto de todas as linhas entre a primeira linha (-----iniciar certificado-----) e a última linha (----------de certificado final) no arquivo.
Você pode recuperar o PublicCertData usando comandos do Windows PowerShell semelhantes a este: $Text = Get-Content-Path "C:\Azure\Certificates\ExportedCertficate.cer" $CertificateText = for ($i = 1; $i-lt $Text. Length-1; $i + +) {$Text \[ $i \] }

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome do grupo de recursos ao qual o gateway de rede virtual está atribuído.
Grupos de recursos categorizam itens para ajudar a simplificar o gerenciamento de inventário e a administração geral do Azure.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetworkGatewayName
Especifica o nome do gateway de rede virtual do qual o certificado será removido.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VpnClientRootCertificateName
Especifica o nome do certificado raiz do cliente que este cmdlet Remove.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. String

## EXIBE

### System. Boolean

## INFORMA

## LINKS RELACIONADOS

[Add-AzVpnClientRootCertificate](./Add-AzVpnClientRootCertificate.md)

[Get-AzVpnClientRootCertificate](./Get-AzVpnClientRootCertificate.md)

[New-AzVpnClientRootCertificate](./New-AzVpnClientRootCertificate.md)


