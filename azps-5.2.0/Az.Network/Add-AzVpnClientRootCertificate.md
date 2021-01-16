---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B9153CA9-06D1-4EF3-9863-D649C2EBAEAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRootCertificate.md
ms.openlocfilehash: efb8640f765468432a2927f865ce9f67c7b9164f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262570"
---
# Add-AzVpnClientRootCertificate

## Sinopse
Adiciona um certificado raiz de cliente VPN.

## SYNTAX

```
Add-AzVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Add-AzVpnClientRootCertificate** adiciona um certificado raiz a um gateway de rede virtual.
Os certificados raiz são certificados X. 509 que identificam a autoridade de certificação raiz.
Por design, todos os certificados usados no gateway confiam no certificado raiz.
Esse cmdlet atribui um certificado existente como um certificado raiz de gateway.
Se você não tiver um certificado X. 509 disponível, poderá gerar um por meio da infraestrutura de chave pública ou usar um gerador de certificado, como makecert.exe.
Para adicionar um certificado raiz, você deve especificar o nome do certificado e fornecer uma representação somente texto do certificado (consulte *o parâmetro PublicCertData* para obter mais informações).
O Azure permite que você atribua mais de um certificado raiz a um gateway.
Geralmente, vários certificados raiz são implantados por organizações que incluem usuários de mais de uma empresa.

## EXEMPLOS

### Exemplo 1: adicionar um certificado raiz de cliente a um gateway virtual
```
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Add-AzVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway" -VpnClientRootCertificateName "ContosoClientRootCertificate"
```

Este exemplo adiciona um certificado raiz de cliente a um gateway virtual chamado ContosoVirtualGateway.
O primeiro comando usa o cmdlet **Get-Content** para obter uma representação de texto exportado anteriormente do certificado raiz e armazena esses dados de texto na variável chamada $Text.
Em seguida, o segundo comando usa um loop for para extrair todo o texto, exceto a primeira linha e a última linha.
O texto extraído é armazenado em uma variável chamada $CertificateText.
Em seguida, o terceiro comando usa o texto armazenado no $CertificateText com o cmdlet **Add-AzVpnClientRootCertificate** para adicionar o certificado raiz ao gateway.

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
Especifica a representação de texto do certificado raiz a ser adicionado.
Para obter a representação de texto, exporte seu certificado no formato. cer (usando a codificação Base64) e, em seguida, abra o arquivo resultante em um editor de texto.
Ao fazer isso, você verá uma saída semelhante à seguinte (Observe que a saída real conterá muito mais linhas de texto do que a amostra abreviada mostrada aqui):-----iniciar certificado-----MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w-----término do certificado-----o PublicCertData é composto de todas as linhas entre a primeira linha (-----iniciar certificado-----) e a última linha (----------de certificado final) no arquivo.
Você pode recuperar esses dados usando comandos do Windows PowerShell semelhantes a isto: `$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"`
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
Especifica o nome do grupo de recursos ao qual o certificado raiz está atribuído.
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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. String

## EXIBE

### Microsoft. Azure. Commands. Network. Models. PSVpnClientRootCertificate

## INFORMA

## LINKS RELACIONADOS

[Get-AzVpnClientRootCertificate](./Get-AzVpnClientRootCertificate.md)

[New-AzVpnClientRootCertificate](./New-AzVpnClientRootCertificate.md)

[Remove-AzVpnClientRootCertificate](./Remove-AzVpnClientRootCertificate.md)


