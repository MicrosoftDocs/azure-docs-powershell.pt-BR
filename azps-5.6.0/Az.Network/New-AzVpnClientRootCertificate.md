---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C54AC64C-DA21-443E-8CFE-6CCAC6152C2B
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRootCertificate.md
ms.openlocfilehash: 866a3b9ac28de57a71fce5fb84b2fa1144d0ff8e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886897"
---
# New-AzVpnClientRootCertificate

## SYNOPSIS
Cria um novo certificado raiz de cliente VPN.

## SINTAXE

```
New-AzVpnClientRootCertificate -Name <String> -PublicCertData <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIPTION
O cmdlet **New-AzVpnClientRootCertificate** cria um novo certificado raiz VPN para uso em um gateway de rede virtual.
Certificados raiz são certificados X.509 que identificam sua Autoridade de Certificação Raiz: todos os outros certificados usados no gateway confiam no certificado raiz.
Este cmdlet cria um certificado autônomo que não é atribuído a um gateway virtual.
Em vez disso, o certificado criado pelo **New-AzVpnClientRootCertificate** é usado em conjunto com o cmdlet New-AzVirtualNetworkGateway ao criar um novo gateway.
Por exemplo, suponha que você crie um novo certificado e armazene-o em uma variável chamada $Certificate.
Em seguida, você pode usar esse objeto de certificado ao criar um novo gateway virtual.
Por exemplo, `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRootCertificates $Certificate`
Para obter mais informações, consulte a documentação do New-AzVirtualNetworkGateway cmdlet.

## EXEMPLOS

### Exemplo 1: Criar um certificado raiz do cliente
```
PS C:\> $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> $Certificate = New-AzVpnClientRootCertificate -PublicCertData $CertificateText -Name "ContosoClientRootCertificate"
```

Este exemplo cria um certificado raiz do cliente e armazena o objeto de certificado em uma variável chamada $Certificate.
Essa variável pode ser usada pelo cmdlet **New-AzVirtualNetworkGateway** para adicionar um certificado raiz a um novo gateway de rede virtual.
O primeiro comando usa o cmdlet **Get-Content** para obter uma representação de texto exportada anteriormente do certificado raiz; que os dados de texto são armazenados em uma variável chamada $Text.
O segundo comando usa um loop para extrair todo o texto, exceto a primeira linha e a última linha, armazenar o texto extraído em uma variável chamada $CertificateText.
O terceiro comando usa o cmdlet **New-AzVpnClientRootCertificate** para criar o certificado, armazenar o objeto criado em uma variável chamada $Certificate.

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

### -Name
Especifica um nome para o novo certificado raiz do cliente.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicCertData
Especifica uma representação de texto do certificado raiz a ser adicionado.
Para obter a representação de texto, exporte seu certificado no formato .cer (usando a codificação Base64) e abra o arquivo resultante em um editor de texto.
Você deve ver uma saída semelhante a esta (observe que a saída real conterá muito mais linhas de texto do que o exemplo abreviado mostrado aqui): ----- CERTIFICADO BEGIN ----- MIIC13FAAXC3671Auij9HgUNEW8343NMJklo 09982CVVFAw8w ----- END CERTIFICATE ----- O PublicCertData é feito de todas as linhas entre a primeira linha (----- BEGIN CERTIFICATE -----) e a última linha (----- END CERTIFICATE -----) no arquivo.
Você pode recuperar o PublicCertData usando comandos Windows PowerShell semelhantes a este: $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text \[ $i \] }

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

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

## SAÍDAS

### Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate

## NOTES

## LINKS RELACIONADOS

[Add-AzVpnClientRootCertificate](./Add-AzVpnClientRootCertificate.md)

[Get-AzVpnClientRootCertificate](./Get-AzVpnClientRootCertificate.md)

[Remove-AzVpnClientRootCertificate](./Remove-AzVpnClientRootCertificate.md)


