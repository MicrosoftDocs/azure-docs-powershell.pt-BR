---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: DA5689DF-AA4A-4161-89B0-8055BF384274
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7b71367ac18a753fad5425d0073b55cacb413e4b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945772"
---
# Start-AzureVirtualNetworkGatewayDiagnostics

## Sinopse
Inicia o diagnóstico para um gateway de rede virtual.

## SYNTAX

```
Start-AzureVirtualNetworkGatewayDiagnostics -GatewayId <String> [-CaptureDurationInSeconds <Int32>]
 [-ContainerName <String>] [-StorageContext <AzureStorageContext>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Start-AzureVirtualNetworkGatewayDiagnostics** inicia uma nova sessão de diagnóstico de gateway para um gateway de rede virtual.
Somente uma sessão de diagnóstico do gateway pode ser executada por vez.
Se você executar esse cmdlet enquanto uma sessão de diagnóstico do gateway estiver em execução, esse cmdlet retornará um erro.

## EXEMPLOS

## OS

### -CaptureDurationInSeconds
Especifica a duração da captura em segundos.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ContainerName
Especifica o nome de um contêiner do Azure.
Esse cmdlet armazena resultados no contêiner que esse parâmetro especifica.

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

### -Gatewayid
Especifica a ID de um gateway.

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

### -StorageContext
Especifica um contexto de armazenamento do Azure.
Esse cmdlet armazena resultados usando o contexto de armazenamento que esse parâmetro especifica.

```yaml
Type: AzureStorageContext
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

## EXIBE

## INFORMA

## LINKS RELACIONADOS

[Get-AzureVirtualNetworkGatewayDiagnostics](./Get-AzureVirtualNetworkGatewayDiagnostics.md)

[Parar-AzureVirtualNetworkGatewayDiagnostics](./Stop-AzureVirtualNetworkGatewayDiagnostics.md)


