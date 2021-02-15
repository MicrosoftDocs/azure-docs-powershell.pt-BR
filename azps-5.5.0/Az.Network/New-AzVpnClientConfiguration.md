---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientConfiguration.md
ms.openlocfilehash: 11b18f0a0f12a82e88694fd91ce89956951a4eb6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114125"
---
# New-AzVpnClientConfiguration

## Sinopse
Esse comando permite que os usuários criem o pacote de perfil vpn com base nas configurações de vpn pré-configuradas no gateway VPN, além de algumas configurações adicionais que os usuários talvez precisem configurar, por exemplo, alguns certificados raiz.

## Sintaxe

```
New-AzVpnClientConfiguration [-Name <String>] -ResourceGroupName <String> [-ProcessorArchitecture <String>]
 [-AuthenticationMethod <String>] [-RadiusRootCertificateFile <String>]
 [-ClientRootCertificateFileList <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Descrição
Isso permite que os usuários criem o pacote de perfil vpn com base nas configurações de vpn pré-configuradas no gateway VPN, além de algumas configurações adicionais que os usuários podem precisar configurar, por exemplo, alguns certificados raiz.

## Exemplos

### Exemplo 1
```
PS C:\> New-AzVpnClientConfiguration -ResourceGroupName "ContosoResourceGroup" -Name "ContosoVirtualNetworkGateway" -AuthenticationMethod "EAPTLS" -RadiusRootCertificateFile "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"
```

Este cmdlet é usado para criar um arquivo zip de perfil de cliente VPN para "ContosoVirtualNetworkGateway" no ResourceGroup "ContosoResourceGroup". O perfil é gerado para um servidor de raio pré-configurado configurado para usar o método de autenticação "EAPTLS" com o arquivo de certificado VpnProfileRadiusCert.

## Parâmetros

### -AuthenticationMethod
O Método de Autenticação pode ter valores EAPMSCHAPv2 ou EAPTLS. Quando EAPMSCHAPv2 é especificado, o cmdlet gera um instalador de configuração do cliente para autenticação de nome de usuário/senha que usa EAP-MSCHAPv2 protocolo de autenticação. Se EAPTLS for especificado, o cmdlet gerará um instalador de configuração de cliente para autenticação de certificado que usa o protocolo EAP-TLS. A opção "EapTls" pode ser usada para autenticação de certificado baseada em RAIO e autenticação de certificação executada pelo Gateway de Rede Virtual carregando a raiz confiável. O cmdlet detecta automaticamente o que está configurado.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: EAPTLS, EAPMSCHAPv2

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ClientRootCertificateFileList
Uma lista de caminhos de certificado raiz do cliente

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -Nome
O nome do recurso.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ProcessorArchitecture
Processorarchitecture

```yaml
Type: System.String
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
Caminho de certificado raiz do servidor de raios. Esse é um parâmetro obrigatório que deve ser especificado quando OEAP-TLS com autenticação RAIO é usado. Este é o nome completo do caminho do arquivo .cer que contém o certificado raiz RAIO que o cliente usa para validar o servidor RAIO durante a autenticação.

```yaml
Type: System.String
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
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirmar
Solicita confirmação antes de executar o cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra o que acontece se o cmdlet for executado. O cmdlet não é executado.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Entradas

### System.String

### System.String[]

## Saídas

### Microsoft.Azure.Commands.Network.Models.PSVpnProfile

## Notas

## LINKS RELACIONADOS

[Get-AzVpnClientConfiguration](./Get-AzVpnClientConfiguration.md)
