---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermpacketcapturefilterconfig
schema: 2.0.0
ms.openlocfilehash: 1d6054307ad1e499fbb36342f6c81e7e32227f37
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785670"
---
# New-AzureRmPacketCaptureFilterConfig

## Sinopse
Cria um novo objeto de filtro de captura de pacotes.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
New-AzureRmPacketCaptureFilterConfig [-Protocol <String>] [-RemoteIPAddress <String>]
 [-LocalIPAddress <String>] [-LocalPort <String>] [-RemotePort <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet New-AzureRmPacketCaptureFilterConfig cria um novo objeto de filtro de captura de pacote. Esse objeto é usado para restringir o tipo de pacotes que são capturados durante uma sessão de captura de pacote usando os critérios especificados. O cmdlet New-AzureRmNetworkWatcherPacketCapture pode aceitar vários objetos de filtro para habilitar as sessões de captura combináveis.

## EXEMPLOS

### ---Exemplo 1: criar uma captura de pacotes com vários filtros---
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzureRmStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzureRmPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzureRmPacketCaptureFilterConfig -Protocol UDP 
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2
```

Neste exemplo, criamos uma captura de pacote chamada "PacketCaptureTest" com vários filtros e um limite de tempo. Após a conclusão da sessão, ela será salva na conta de armazenamento especificada. 

Observação: a extensão do Inspetor de rede do Azure deve ser instalada na máquina virtual de destino para criar capturas de pacote.

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

### -LocalIPAddress
Especifica o endereço IP local para filtrar.
Exemplos de entradas: "127.0.0.1" para entrada de endereço único.
"127.0.0.1-127.0.0.255" para o intervalo.
"127.0.0.1; 127.0.0.5;" para várias entradas.

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

### -LocalPort
Especifica o endereço IP local para filtrar.
Exemplos de entradas: "127.0.0.1" para entrada de endereço único.
"127.0.0.1-127.0.0.255" para o intervalo.
"127.0.0.1; 127.0.0.5;" para várias entradas.

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

### -Protocolo
Especifica o Procotol para filtrar. Valores aceitáveis "TCP", "UDP", "qualquer"

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RemoteIPAddress
Especifica o endereço IP remoto para filtrar.
Exemplos de entradas: "127.0.0.1" para entrada de endereço único.
"127.0.0.1-127.0.0.255" para o intervalo.
"127.0.0.1; 127.0.0.5;" para várias entradas.

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

### -RemotePort
Especifica a porta remota para filtrar.
Entradas de exemplo de porta remota: "80" para entrada de porta única.
"80-85" para o intervalo.
"80; 443;" para várias entradas.

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

### Microsoft. Azure. Commands. Network. Models. PSPacketCaptureFilter

## INFORMA
Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede, Inspetor, pacote, captura, tráfego, filtro 

## LINKS RELACIONADOS

[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md)

[Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md)

[Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[Parar-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md)

[Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md)

[Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)

[Test-AzureRmNetworkWatcherIPFlow](./Test-AzureRmNetworkWatcherIPFlow.md)

[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md)

[Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md)

[Start-AzureRmNetworkWatcherResourceTroubleshooting](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
