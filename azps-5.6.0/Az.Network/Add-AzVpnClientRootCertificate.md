---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B9153CA9-06D1-4EF3-9863-D649C2EBAEAA
online version: https://docs.microsoft.com/powershell/module/az.network/add-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRootCertificate.md
ms.openlocfilehash: 38a6abb631a77d41e38026edd3bef5abe9c70c01
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888843"
---
# Add-AzVpnClientRootCertificate

## SYNOPSIS
Adiciona um certificado raiz de cliente VPN.

## SINTAXE

```
Add-AzVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRIPTION
O cmdlet **Add-AzVpnClientRootCertificate** adiciona um certificado raiz a um gateway de rede virtual.
Certificados raiz são certificados X.509 que identificam sua Autoridade de Certificação Raiz.
Por design, todos os certificados usados no gateway confiam no certificado raiz.
Este cmdlet atribui um certificado existente como um certificado raiz de gateway.
Se você não tiver um certificado X.509 disponível, poderá gerar um por meio de sua infraestrutura de chave pública ou usar um gerador de certificados como makecert.exe.
Para adicionar um certificado raiz, você deve especificar o nome do certificado e fornecer uma representação somente de texto do certificado (consulte o parâmetro *PublicCertData* para obter mais informações).
O Azure permite atribuir mais de um certificado raiz a um gateway.
Vários certificados raiz geralmente são implantados por organizações que incluem usuários de mais de uma empresa.

## EXEMPLOS

### Exemplo 1: Adicionar um certificado raiz do cliente a um gateway virtual
```
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Add-AzVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway" -VpnClientRootCertificateName "ContosoClientRootCertificate"
```

Este exemplo adiciona um certificado raiz do cliente a um gateway virtual chamado ContosoVirtualGateway.
O primeiro comando usa o cmdlet **Get-Content** para obter uma representação de texto exportada anteriormente do certificado raiz e armazena os dados de texto da variável chamada $Text.
Em seguida, o segundo comando usa um loop para extrair todo o texto, exceto para a primeira linha e a última linha.
O texto extraído é armazenado em uma variável chamada $CertificateText.
O terceiro comando usa o texto armazenado no $CertificateText com o cmdlet **Add-AzVpnClientRootCertificate** para adicionar o certificado raiz ao gateway.

## PARÂMETROS

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

### -PublicCertData
Especifica a representação de texto do certificado raiz a ser adicionado.
Para obter a representação de texto, exporte seu certificado no formato .cer (usando a codificação Base64) e abra o arquivo resultante em um editor de texto.
Ao fazer isso, você verá uma saída semelhante à seguinte (observe que a saída real conterá muito mais linhas de texto do que o exemplo abreviado mostrado aqui): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJ ----- CERTIFICADO FINAL ----- O PublicCertData é feito de todas as linhas entre a primeira linha (----- BEGIN CERTIFICATE -----) e ----- ----- última linha (----- END CERTIFICATE -----) no arquivo.
Você pode recuperar esses dados usando Windows PowerShell comandos semelhantes a este: `$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"`
`$CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}`

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
Especifica o nome do grupo de recursos ao que o certificado raiz é atribuído.
Os grupos de recursos categorizam itens para ajudar a simplificar o gerenciamento de inventário e a administração geral do Azure.

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
Especifica o nome do gateway de rede virtual onde o certificado é adicionado.

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
Especifica o nome do certificado raiz do cliente que este cmdlet adiciona.

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

## INPUTS

### System.String

## SAÍDAS

### Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate

## NOTES

## LINKS RELACIONADOS

[Get-AzVpnClientRootCertificate](./Get-AzVpnClientRootCertificate.md)

[New-AzVpnClientRootCertificate](./New-AzVpnClientRootCertificate.md)

[Remove-AzVpnClientRootCertificate](./Remove-AzVpnClientRootCertificate.md)


