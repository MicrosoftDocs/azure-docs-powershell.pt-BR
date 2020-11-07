---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 99D9EFA6-3506-4B0E-ACB5-C6EDBCB5A130
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9d73ede26d4bd85a39f4baf2090e581300eafb1b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945515"
---
# New-AzureStorSimpleNetworkConfig

## Sinopse
Prepara um objeto de configuração de rede.

## SYNTAX

```
New-AzureStorSimpleNetworkConfig -InterfaceAlias <String> [-EnableIscsi <Boolean>] [-EnableCloud <Boolean>]
 [-Controller0IPv4Address <String>] [-Controller1IPv4Address <String>] [-IPv6Gateway <String>]
 [-IPv4Gateway <String>] [-IPv4Address <String>] [-IPv6Prefix <String>] [-IPv4Netmask <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzureStorSimpleNetworkConfig** prepara um objeto de configuração de rede para passar para o cmdlet **set-AzureStorSimpleDevice** .
Defina o parâmetro *Controller0IPAddress* e o parâmetro *Controller1IPAddress* apenas na interface Data0.
O Data0 dá suporte a apenas três configurações: *Controller0IPAddress* , *Controller1IPAdress* e *EnableIscsi*.

## EXEMPLOS

### Exemplo 1: configurar uma interface Data0
```
PS C:\>New-AzureStorSimpleNetworkConfig -InterfaceAlias Data0 -EnableIscsi $True -Controller0IPv4Address "10.67.64.48" -Controller1IPv4Address "10.67.64.49"
VERBOSE: ClientRequestId: 0621d220-a460-48ec-84ec-02a3a82f88b2_PS


IsIscsiEnabled         : True
IsCloudEnabled         : 
Controller0IPv4Address : 10.67.64.48
Controller1IPv4Address : 10.67.64.49
IPv6Gateway            : 
IPv4Gateway            : 
IPv4Address            : 
IPv6Prefix             : 
IPv4Netmask            : 
InterfaceAlias         : Data0

VERBOSE: Successfully created a StorSimple Network Configuration for interface Data0
```

Esse comando cria a configuração de rede para a interface Data0.
Esse comando especifica os parâmetros *Controller0IPv4Address* , *Controller1IPv4Address* e *EnableIscsi* .
Este cmdlet pode configurar o Data0 para apenas esses três parâmetros.

### Exemplo 2: configurar uma interface diferente de Data0 um
```
PS C:\>New-AzureStorSimpleNetworkConfig -InterfaceAlias Data1 -EnableIscsi $True -EnableCloud $True -IPv6Gateway "db8:421e:9a8::a4:1c50" -IPv4Gateway "10.67.64.1" -IPv4Address "10.67.64.48" -IPv6Prefix "2001:db8:a::123/64" -IPv4Netmask "255.255.0.0"
VERBOSE: ClientRequestId: 3a15ff0e-b769-4329-9147-676b1e0acd7d_PS


IsIscsiEnabled         : True
IsCloudEnabled         : True
Controller0IPv4Address : 
Controller1IPv4Address : 
IPv6Gateway            : db8:421e:9a8::a4:1c50
IPv4Gateway            : 10.67.64.1
IPv4Address            : 10.67.64.48
IPv6Prefix             : 2001:db8:a::123/64
IPv4Netmask            : 255.255.0.0
InterfaceAlias         : Data1
VERBOSE: Successfully created a StorSimple Network Configuration for interface Data1
```

Esse comando configura a interface Dados1.

### Exemplo 3: modificar uma configuração para um dispositivo
```
PS C:\>$NetworkConfigData0 = New-AzureStorSimpleNetworkConfig -InterfaceAlias Data0 -EnableIscsi $True -Controller0IPv4Address "10.67.64.48" -Controller1IPv4Address "10.67.64.49"
$OnlineDevice = @(Get-AzureStorSimpleDevice | Where { $_.Status -eq "Online"})[0]
$UpdatedDetails = Set-AzureStorSimpleDevice -DeviceId $OnlineDevice.DeviceId -StorSimpleNetworkConfig $NetworkConfigData0
VERBOSE: ClientRequestId: 0f163163-5ad0-4635-a7b5-870d47297f66_PS
VERBOSE: Successfully created a StorSimple Network Configuration for interface Data0
VERBOSE: ClientRequestId: 552e4a6c-7006-4015-a20b-9def6428a85e_PS
VERBOSE: ClientRequestId: f31cc84c-bc8a-404a-9da6-4670a7999e75_PS
VERBOSE: 1 StorSimple device found! 
VERBOSE: ClientRequestId: 545bc1a9-3c1b-4e50-89a6-9678aefe79e5_PS
VERBOSE: ClientRequestId: f114ad08-47f5-4fb8-8a01-1ea7f1ed1b98_PS
VERBOSE: About to configure the device : newDeviceName ! 
VERBOSE: ClientRequestId: 6afe7927-1c19-48d3-ac22-68148fd056b8_PS
VERBOSE: The task created for your Setup operation has completed successfully. 
VERBOSE: ClientRequestId: 467c142c-90da-4d75-82a4-c114afce953d_PS
VERBOSE: Successfully updated configuration for device newDeviceName with id 865e68f6-1e71-47b6-80d5-15d3a23bd2b0
```

O primeiro comando cria uma configuração de rede para a interface Data0.
Esse comando especifica os parâmetros *Controller0IPv4Address* , *Controller1IPv4Address* e *EnableIscsi* .
O comando armazena o resultado na variável $NetworkConfigData 0.

O segundo comando usa o cmdlet **Get-AzureStorSimpleDevice** e o cmdlet de núcleo do **objeto Where** para obter um dispositivo StorSimple online e, em seguida, armazena-o na variável $OnlineDevice.

O comando final modifica a configuração do dispositivo que tem a identificação de dispositivo especificada usando o cmdlet **set-AzureStorSimpleDevice** .
O comando usa o objeto de configuração que o cmdlet atual criou no primeiro comando.

## OS

### -Controller0IPv4Address
Especifica o endereço IPv4 para o controlador 0.
Especifique esse parâmetro somente para a interface Data0.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Controller1IPv4Address
Especifica o endereço IPv4 para o controlador 1.
Especifique esse parâmetro somente para a interface Data0.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableCloud
Indica se a interface será habilitada na nuvem.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableIscsi
Indica se o SCSI da Internet (ISCSI) deve ser habilitado para a interface.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InterfaceAlias
Especifica o alias da interface para o qual este cmdlet fornece configurações.
Os valores válidos são de Data0 para data5.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IPv4Address
Especifica o endereço IPv4 para a interface.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IPv4Gateway
Especifica o endereço IPv4 de um gateway.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IPv4Netmask
Especifica a máscara de rede IPv4 para a interface.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IPv6Gateway
Especifica o gateway IPv6 para a interface.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IPv6Prefix
Especifica o prefixo IPv6 para a interface.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Perfil
Especifica um perfil do Azure.

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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma

## EXIBE

### NetworkConfig
Esse cmdlet retorna um objeto NetworkConfig que contém as seguintes propriedades: 

- **IsIscsiEnabled** ( **booliano** ) 
- **IsCloudEnabled** ( **booliano** )
- **Controller0IPv4Address** ( **IPAddress** ) 
- **Controller1IPv4Address** ( **IPAddress** ) 
- **IPv6Gateway** ( **IPAddress** ) 
- **IPv4Gateway** ( **IPAddress** ) 
- **IPv4Address** ( **IPAddress** ) 
- **IPv6Prefix** ( **cadeia de caracteres** )
- **IPv4Netmask** ( **IPAddress** ) 
- **InterfaceAlias** ( **netinterfaceid** )

## INFORMA

## LINKS RELACIONADOS

[Set-AzureStorSimpleDevice](./Set-AzureStorSimpleDevice.md)

[Get-AzureStorSimpleDevice](./Get-AzureStorSimpleDevice.md)


