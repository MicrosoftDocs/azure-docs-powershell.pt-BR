---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientConfiguration.md
ms.openlocfilehash: 07618d546ebdadfb3313e17b881a7afbe09d1ff2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432066"
---
# New-AzureRmVpnClientConfiguration

## Sinopse
Esse comando permite que os usuários criem o pacote de perfil VPN com base em configurações de VPN pré-configuradas no gateway VPN, além de algumas configurações adicionais que os usuários podem precisar configurar, por exemplo, alguns certificados raiz.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
New-AzureRmVpnClientConfiguration [-Name <String>] -ResourceGroupName <String>
 [-ProcessorArchitecture <String>] -AuthenticationMethod <String> [-RadiusRootCertificateFile <String>]
 [-ClientRootCertificateFileList <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
Isso permite que os usuários criem o pacote de perfil VPN com base em configurações de VPN pré-configuradas no gateway VPN, além de algumas configurações adicionais que os usuários podem precisar configurar, por exemplo, alguns certificados raiz.

## EXEMPLOS

### Exemplo 1
```
PS C:\> New-AzureRmVpnClientConfiguration -ResourceGroupName "ContosoResourceGroup" -Name "ContosoVirtualNetworkGateway" -AuthenticationMethod "EAPTLS" -RadiusRootCertificateFile "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"
```

Esse cmdlet é usado para criar um arquivo zip do perfil do cliente VPN para "ContosoVirtualNetworkGateway" no grupo de Resource "ContosoResourceGroup". O perfil é gerado para um servidor RADIUS pré-configurado que é configurado para usar o método de autenticação "EAPTLS" com o arquivo de certificado VpnProfileRadiusCert.

## OS

### -AuthenticationMethod
O método de autenticação pode ter os valores EAPMSCHAPv2 ou EAPTLS. Quando EAPMSCHAPv2 é especificado, o cmdlet gera um instalador de configuração de cliente para autenticação de nome de usuário/senha que usa o protocolo de autenticação EAP-MSCHAPv2. Se EAPTLS for especificado, o cmdlet gerará um instalador de configuração de cliente para autenticação de certificado que usa o protocolo EAP-TLS. A opção "EapTls" pode ser usada para autenticação de certificação e autenticação de certificado baseada em RADIUS realizada pelo gateway de rede virtual carregando a raiz confiável. O cmdlet detecta automaticamente o que está configurado.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: EAPTLS, EAPMSCHAPv2

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ClientRootCertificateFileList
Uma lista de caminhos de certificado raiz do cliente
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
O nome do recurso.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ProcessorArchitecture
ProcessorArchitecture

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Amd64, X86

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RadiusRootCertificateFile
Caminho do certificado raiz do servidor RADIUS. Esse é um parâmetro obrigatório que deve ser especificado quando EAP-TLS com autenticação RADIUS for usado. Esse é o nome do caminho completo do arquivo. cer que contém o certificado raiz RADIUS que o cliente usa para validar o servidor RADIUS durante a autenticação.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
O nome do grupo de recursos.

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
Mostra o que aconteceria se o cmdlet fosse executado. O cmdlet não é executado.

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

### System. String
System. Collections. Generic. List ' 1 [System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]

## EXIBE

### Microsoft. Azure. Commands. Network. Models. PSVpnProfile

## INFORMA

## LINKS RELACIONADOS

