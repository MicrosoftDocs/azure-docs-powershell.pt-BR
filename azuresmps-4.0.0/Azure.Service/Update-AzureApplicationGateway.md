---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: C7F08804-E177-4BC5-8F0E-DEC1B467C4BB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 20cb37fbba8fd3789c0932f9ff1e9352334662e9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945844"
---
# Update-AzureApplicationGateway

## Sinopse
Atualiza um gateway de aplicativo.

## SYNTAX

```
Update-AzureApplicationGateway -Name <String> [-VnetName <String>]
 [-Subnets <System.Collections.Generic.List`1[System.String]>] [-InstanceCount <UInt32>]
 [-GatewaySize <String>] [-Description <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Update-AzureApplicationGateway** atualiza um gateway de aplicativo existente.

## EXEMPLOS

### Exemplo 1: modificar um gateway do aplicativo usando seu nome
```
PS C:\> Stop-AzureApplicationGateway -Name "ApplicationGateway06"
PS C:\> Update-AzureApplicationGateway -Name "ApplicationGateway06" -VnetName "VirutalNetwork18" -Subnets @("Subnet05", "Subnet06")
```

O primeiro comando interrompe o aplicativo gateway chamado ApplicationGateway06.
Um gateway de aplicativo deve ser interrompido para que você possa modificar a rede virtual ou sub-redes.

O segundo comando modifica a sub-rede virtual e sub-redes do gateway do aplicativo chamado ApplicationGateway06.

### Exemplo 2: modificar as propriedades adicionais de um gateway de aplicativo
```
PS C:\> Update-AzureApplicationGateway -Name "ApplicationGateway06" -InstanceCount 2 -GatewaySize "Large" -Description "Updated application gateway"
```

Esse comando modifica a contagem de instâncias, o tamanho do gateway e a descrição do gateway do aplicativo chamado ApplicationGateway06.
Esse comando não modifica a rede virtual ou sub-redes do Application Gateway.
Portanto, você não precisa parar o gateway do aplicativo antes de executar esse comando.

### Exemplo 3: modificar um gateway do aplicativo usando o pipeline
```
PS C:\> $ApplicationGateway = Get-AzureApplicationGateway -Name "ApplicationGateway06"
PS C:\> $ApplicationGateway.GatewaySize = "Medium"
PS C:\> $ApplicationGateway | Update-AzureApplicationGateway
```

O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway06 usando o cmdlet **Get-AzureApplicationGateway** .
O comando o armazena na variável $ApplicationGateway.

O segundo comando atribui à propriedade **GatewaySize** o valor Medium.

O comando final passa o $ApplicationGateway atualizado para o cmdlet atual.

## OS

### -Descrição
Especifica uma descrição que esse cmdlet atribui ao gateway do aplicativo.

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

### -GatewaySize
Especifica o tamanho que esse cmdlet atribui ao gateway do aplicativo.
Os valores válidos são:

- Versalete
- Port
- Muita

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

### -InstanceCount
Especifica o número de instâncias atribuídas por esse cmdlet ao gateway do aplicativo.

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nome
Especifica o nome do aplicativo do gateway que este cmdlet atualiza.

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

### -Perfil
Especifica o perfil do Azure do qual este cmdlet lê.
Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Sub-redes
Especifica uma matriz de sub-redes em que esse cmdlet implanta o Application Gateway.

Você não pode atualizar sub-redes enquanto o gateway do aplicativo está em execução.
Para interromper o gateway do aplicativo, use o cmdlet Stop-AzureApplicationGateway.

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

### -VnetName
Especifica a rede virtual na qual esse cmdlet implanta o gateway do aplicativo.

Você não pode atualizar uma rede virtual enquanto o gateway do aplicativo está em execução.
Para interromper o gateway do aplicativo, use **Stop-AzureApplicationGateway**.

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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. String

## EXIBE

### Microsoft. WindowsAzure. Management. ApplicationGateway. Models. ApplicationGatewayOperationResponse

## INFORMA

## LINKS RELACIONADOS

[Get-AzureApplicationGateway](./Get-AzureApplicationGateway.md)

[New-AzureApplicationGateway](./New-AzureApplicationGateway.md)

[Remove-AzureApplicationGateway](./Remove-AzureApplicationGateway.md)

[Start-AzureApplicationGateway](./Start-AzureApplicationGateway.md)

[Parar-AzureApplicationGateway](./Stop-AzureApplicationGateway.md)
