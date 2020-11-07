---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 53580FF1-D905-40FD-A5F0-D5FBCD036E0B
online version: ''
schema: 2.0.0
ms.openlocfilehash: a51fd8210d2fe7fb224ed43650a354e383ed4e54
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945776"
---
# Start-AzureStorSimpleDeviceFailoverJob

## Sinopse
Inicia uma operação de failover de grupos de contêineres de volume.

## SYNTAX

### Vazio (padrão)
```
Start-AzureStorSimpleDeviceFailoverJob
 -VolumecontainerGroups <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]>
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyById
```
Start-AzureStorSimpleDeviceFailoverJob -DeviceId <String>
 -VolumecontainerGroups <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]>
 -TargetDeviceId <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyByName
```
Start-AzureStorSimpleDeviceFailoverJob -DeviceName <String>
 -VolumecontainerGroups <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]>
 -TargetDeviceName <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Start-AzureStorSimpleDeviceFailoverJob** inicia uma operação de failover de um ou mais grupos de contêineres de volume de um dispositivo para outro.

## EXEMPLOS

### Exemplo 1: iniciar um trabalho de failover para um dispositivo nomeado e um dispositivo de destino nomeado
```
PS C:\>(Get-AzureStorSimpleFailoverVolumeContainers -DeviceName "ChewD_App7") | Where-Object {$_.IsDCGroupEligibleForDR -eq $True} | Start-AzureStorSimpleDeviceFailoverJob -DeviceName "ChewD_App7" -TargetDeviceName "Fuller05" -Force
a3d902be-8ffb-42a4-bbf8-0a1b30db71b2_0ee59ae9-0293-46e2-ae56-bc308c8e5520
```

Esse comando obtém os contêineres de volume de failover para o dispositivo chamado ChewD_App7 usando o cmdlet **Get-AzureStorSimpleFailoverVolumeContainers** .
O comando passa os resultados para o cmdlet **Where-Object** , que descarta os contêineres que têm um valor diferente de $true para a propriedade **IsDCGroupEligibleForDR** .
Para obter mais informações, digite `Get-Help Where-Object` .
O cmdlet atual inicia trabalhos de failover para os contêineres de volume de failover restantes.
O comando especifica o nome do dispositivo e o nome do dispositivo de destino.
O comando retorna a ID da instância do trabalho que o cmdlet inicia.

### Exemplo 2: iniciar um trabalho de failover para um dispositivo e um dispositivo de destino especificado por ID
```
PS C:\>(Get-AzureStorSimpleFailoverVolumeContainers -DeviceId "3825f272-1efb-4c14-b63f-22605ce3b925") | Where-Object {$_.IsDCGroupEligibleForDR -eq $True} | Select-Object -First 1 | Start-AzureStorSimpleDeviceFailoverJob -DeviceId "3825f272-1efb-4c14-b63f-22605ce3b925" -TargetDeviceId "0ee59ae9-0293-46e2-ae56-bc308c8e5520" -Force
4c5ac0d0-4b66-465c-98f5-aec90505ad12_0ee59ae9-0293-46e2-ae56-bc308c8e5520
```

Esse comando obtém os contêineres de volume de failover para o dispositivo chamado ChewD_App7 usando **Get-AzureStorSimpleFailoverVolumeContainers**.
O comando passa os resultados para **Where-Object** , que descarta os Conquerors que têm um valor diferente de $true para a propriedade **IsDCGroupEligibleForDR** .
O cmdlet passa os resultados para o cmdlet **Select-Object** , que seleciona o primeiro objeto para passar para o cmdlet atual.
Para obter mais informações, digite `Get-Help Select-Object` .
O cmdlet atual inicia trabalhos de failover para o contêiner de volume de failover selecionado.
O comando especifica a ID do dispositivo e a ID do dispositivo de destino.
O comando retorna a ID da instância do trabalho que o cmdlet inicia.

## OS

### -DeviceID
Especifica a ID de instância do dispositivo StorSimple no qual os grupos de contêineres de volume existem.

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceName
Especifica o nome do dispositivo StorSimple no qual os grupos de contêineres de volume existem.

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Força o comando a ser executado sem pedir confirmação do usuário.

```yaml
Type: SwitchParameter
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

### -TargetDeviceId
Especifica a ID de instância do dispositivo StorSimple para o qual esse cmdlet falha em grupos de contêineres de volume.

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetDeviceName
Especifica o nome do dispositivo StorSimple para o qual esse cmdlet falha em grupos de contêineres de volume.

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VolumecontainerGroups
Especifica a lista de grupos de contêineres de volume para os quais este cmdlet executa failover em outro dispositivo.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Programação\<DataContainerGroup\>
Você pode canalizar uma lista de grupos de contêineres de volume para este cmdlet.

## EXIBE

### String

## INFORMA

## LINKS RELACIONADOS

[Get-AzureStorSimpleFailoverVolumeContainers](./Get-AzureStorSimpleFailoverVolumeContainers.md)


