---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D857FF6-A27D-4031-948D-8A69D24B4AD4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRootCertificate.md
ms.openlocfilehash: 5cb4a57994ad8b15048bfc22dadefbbee031aaf7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111568"
---
# Remove-AzVpnClientRootCertificate

## Sinopse
Remove um certificado raiz de cliente VPN existente.

## Sintaxe

```
Remove-AzVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Descrição
O cmdlet **Remove-AzVpnClientRootCertificate** remove o certificado raiz especificado de um gateway de rede virtual.
Certificados raiz são certificados X.509 que identificam sua Autoridade de Certificação Raiz: todos os outros certificados usados no gateway confiam no certificado raiz.
Se você remover um certificado raiz de computadores que usam o certificado para fins de autenticação, não será mais possível se conectar ao gateway.
Ao usar **Remove-AzVpnClientRootCertificate,** você deve fornecer o nome do certificado e uma representação de texto dos dados do certificado.
Para obter mais informações sobre a representação de texto de um certificado, consulte a descrição do parâmetro *PublicCertData.*

## Exemplos

### Exemplo 1: Remover um certificado raiz do cliente de um gateway de rede virtual
```powershell
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Remove-AzVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway" -VpnClientRootCertificateName "ContosoRootCertificate"
```

Este exemplo remove um certificado raiz do cliente chamado ContosoRootCertificate do gateway de rede virtual ContosoVirtualGateway.
O primeiro comando usa o cmdlet **Get-Content** para obter uma representação de texto exportada anteriormente do certificado; essa representação de texto é armazenada em uma variável chamada $Text.
O segundo comando usa um loop para extrair todo o texto $Text exceto a primeira linha e a última linha.
Esse texto extraído é armazenado em uma variável chamada $CertificateText.
O terceiro comando usa as informações armazenadas na variável $CertificateText juntamente com o cmdlet **Remove-AzVpnClientRootCertificate** para remover o certificado do gateway.

## Parâmetros

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

### -PublicCertData
Especifica a representação de texto do certificado raiz a ser removido.
Para obter a representação de texto, exporte seu certificado no formato .cer (usando a codificação base64) e abra o arquivo resultante em um editor de texto.
Você deve ver uma saída semelhante à seguinte (observe que a saída real conterá muitas mais linhas de texto do que a amostra abreviada mostrada aqui): ----- INICIAR CERTIFICADO ----- MIIC13FAAXC3671Auij9HgUNEW8343NMJklo 09982CVVFAw8w ----- END CERTIFICATE ----- The PublicCertData is made of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) no arquivo.
Você pode recuperar os PublicCertData usando comandos do Windows PowerShell semelhantes a este: $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText = para ($i=1; $i -lt $Text.Length -1 ; $i+){$Text \[ $i \] }

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
Especifica o nome do grupo de recursos ao que o gateway de rede virtual está atribuído.
Os grupos de recursos categorizam itens para ajudar a simplificar o gerenciamento de estoque e a administração geral do Azure.

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
Especifica o nome do gateway de rede virtual do nome do certificado que foi removido.

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
Especifica o nome do certificado raiz do cliente que este cmdlet remove.

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
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Entradas

### System.String

## Saídas

### System.Boolean

## Notas

## LINKS RELACIONADOS

[Add-AzVpnClientRootCertificate](./Add-AzVpnClientRootCertificate.md)

[Get-AzVpnClientRootCertificate](./Get-AzVpnClientRootCertificate.md)

[New-AzVpnClientRootCertificate](./New-AzVpnClientRootCertificate.md)


