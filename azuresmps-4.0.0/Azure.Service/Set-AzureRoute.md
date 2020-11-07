---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A7DFF559-188D-4CF9-9315-CA327E0C5C0B
online version: ''
schema: 2.0.0
ms.openlocfilehash: d502ba2961e5238426228e4ac58a29b922be81f3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945823"
---
# Set-AzureRoute

## Sinopse
Cria uma rota em uma tabela de rota.

## SYNTAX

```
Set-AzureRoute -RouteName <String> -AddressPrefix <String> -NextHopType <String> [-NextHopIpAddress <String>]
 -RouteTable <IRouteTable> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzureRoute** cria uma rota em uma tabela de rota.
A nova rota entra praticamente em vigor praticamente nas máquinas virtuais associadas à tabela de rota.

## EXEMPLOS

### Exemplo 1: adicionar um dispositivo virtual próximo caminho de salto
```
PS C:\> New-AzureRouteTable -Name "ApplianceRouteTable" -Location "Central US" -Label "Appliance Route Table" | Set-AzureRoute -RouteName "ApplianceRoute03" -AddressPrefix "10.0.0.0/24" -NextHopType VirtualAppliance -NextHopIpAddress "10.0.1.5"

Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{approute}                    AppRT                         Central US                    Appliance Route Table
```

Esse comando cria uma tabela de rota chamada ApplianceRouteTable no local especificado.
O comando transmite essa tabela de rota para o cmdlet atual.
O cmdlet Current adiciona uma rota chamada ApplianceRoute03, que é um tipo de salto do VirtualAppliance próximo.
O comando especifica o próximo endereço IP do salto e o prefixo do endereço para a rota.

### Exemplo 2: adicionar uma rota da Internet no próximo salto
```
PS C:\> Get-AzureRouteTable -Name "ApplianceRouteTable" | Set-AzureRoute -RouteName "InternetRoute" -AddressPrefix "0.0.0.0/0" -NextHopType Internet

Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{approute, internetroute}     AppRT                         Central US                    Appliance Route Table
```

Esse comando obtém uma tabela de rota chamada ApplianceRouteTable.
O comando transmite essa tabela de rota para o cmdlet atual.
O cmdlet atual adiciona uma rota chamada InternetRoute, que é um tipo de salto seguinte na Internet.
O comando especifica o prefixo do endereço para a rota.

## OS

### -AddressPrefix
Especifica um prefixo de endereço para a nova rota.

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

### -NextHopIpAddress
Especifica o endereço IP do dispositivo que é o próximo nó do tráfego que usa essa rota.
Especifique esse valor apenas se especificar um valor de VirtualAppliance para o parâmetro *NextHopType* .

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

### -NextHopType
Especifica o próximo tipo de salto para tráfego que usa essa rota.
Os valores válidos são: 

- VPNGateway
- VNETLocal
- Rede
- VirtualAppliance
- Vazio

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

### -Perfil
Especifica o perfil do Azure do qual este cmdlet lê. Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.

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

### -RouteName
Especifica um nome para a nova rota que este cmdlet adiciona.

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

### -RouteTable
Especifica a tabela de rota para a qual esse cmdlet adiciona a nova rota.

```yaml
Type: IRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

## INFORMA

## LINKS RELACIONADOS

[Remove-AzureRoute](./Remove-AzureRoute.md)


