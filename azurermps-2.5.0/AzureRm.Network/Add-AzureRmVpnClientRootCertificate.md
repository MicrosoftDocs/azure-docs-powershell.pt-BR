---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B9153CA9-06D1-4EF3-9863-D649C2EBAEAA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermvpnclientrootcertificate
schema: 2.0.0
ms.openlocfilehash: 2f5d73cd06d975d6458776dee4242b392b5c160b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786491"
---
# Add-AzureRmVpnClientRootCertificate

## Sinopse
Adiciona um certificado raiz de cliente VPN.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Add-AzureRmVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Add-AzureRmVpnClientRootCertificate** adiciona um certificado raiz a um gateway de rede virtual.
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
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Add-AzureRmVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway" -VpnClientRootCertificateName "ContosoClientRootCertificate"
```

Este exemplo adiciona um certificado raiz de cliente a um gateway virtual chamado ContosoVirtualGateway.

O primeiro comando usa o cmdlet **Get-Content** para obter uma representação de texto exportado anteriormente do certificado raiz e armazena esses dados de texto na variável chamada $Text.

Em seguida, o segundo comando usa um loop for para extrair todo o texto, exceto a primeira linha e a última linha.
O texto extraído é armazenado em uma variável chamada $CertificateText.

Em seguida, o terceiro comando usa o texto armazenado no $CertificateText com o cmdlet **Add-AzureRmVpnClientRootCertificate** para adicionar o certificado raiz ao gateway.

## OS

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

### -PublicCertData
Especifica a representação de texto do certificado raiz a ser adicionado.
Para obter a representação de texto, exporte seu certificado no formato. cer (usando a codificação Base64) e, em seguida, abra o arquivo resultante em um editor de texto.
Ao fazer isso, você verá uma saída semelhante à seguinte (Observe que a saída real conterá muito mais linhas de texto do que a amostra abreviada mostrada aqui):

-----Iniciar certificado-----MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w----------término do certificado

O PublicCertData é composto de todas as linhas entre a primeira linha (-----iniciar-----de certificado) e a última linha (----------de certificado final) no arquivo.
Você pode recuperar esses dados usando comandos do Windows PowerShell semelhantes a isto: `$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"`
`$CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}`

```yaml
Type: String
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
Type: String
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
Type: String
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
Type: String
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

## EXIBE

### Microsoft. Azure. Commands. Network. Models. PSVpnClientRootCertificate

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmVpnClientRootCertificate](./Get-AzureRmVpnClientRootCertificate.md)

[New-AzureRmVpnClientRootCertificate](./New-AzureRmVpnClientRootCertificate.md)

[Remove-AzureRmVpnClientRootCertificate](./Remove-AzureRmVpnClientRootCertificate.md)


