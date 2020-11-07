---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: C50959BB-7481-4898-BF4B-C5ABF8758473
online version: ''
schema: 2.0.0
ms.openlocfilehash: e2c06455004afbd15235f59164034abc2147964b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946453"
---
# Remove-AzureStorSimpleDeviceVolumeContainer

## Sinopse
Remove um contêiner de volume de um dispositivo StorSimple.

## SYNTAX

```
Remove-AzureStorSimpleDeviceVolumeContainer -DeviceName <String> -VolumeContainer <DataContainer>
 [-WaitForComplete] [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Remove-AzureStorSimpleDeviceVolumeContainer** remove um objeto de contêiner de volume de um dispositivo StorSimple.
Esse cmdlet solicita confirmação, a menos que você especifique o parâmetro *Force* .

## EXEMPLOS

### Exemplo 1: remover um contêiner usando o pipeline
```
PS C:\>Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "Container08" | Remove-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -Force
VERBOSE: ClientRequestId: 0efbb4fc-ceb0-4311-bc49-0e08161d0a37_PS
VERBOSE: ClientRequestId: bf5b615f-47e3-4868-91b6-f2d12217a302_PS
VERBOSE: ClientRequestId: 5590c87e-0602-4197-b6c3-cf58b0e7a7b3_PS
VERBOSE: ClientRequestId: b33c71ac-c345-44ff-8213-d7fdf9f8480a_PS
VERBOSE: ClientRequestId: 903d42ef-58f4-4e89-ba7f-5f234262356d_PS
VERBOSE: About to create a job to remove your Volume container! 
VERBOSE: ClientRequestId: 2279575f-5115-4344-9c6f-9ef599bd203e_PS
e9ddec89-67ac-4e2e-a2ed-820de3547bb0
VERBOSE: The delete task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
e9ddec89-67ac-4e2e-a2ed-820de3547bb0 for tracking the task's status
VERBOSE: Volume container with name: Container08 is found.
```

Esse comando obtém o contêiner de volume chamado Container08 no dispositivo chamado Contoso63-AppVm usando o cmdlet **Get-AzureStorSimpleDeviceVolumeContainer** .
O comando passa o contêiner de volume para o cmdlet atual usando o operador pipeline.
Esse comando inicia a tarefa para remover o contêiner e, em seguida, retorna um objeto **TaskResponse** .
Para ver o status da tarefa, use o cmdlet **Get-AzureStorSimpleTask** .
Esse comando especifica o parâmetro *Force* , portanto, não solicita a confirmação.

## OS

### -DeviceName
Especifica o nome do dispositivo StorSimple em que existe o contêiner de volume a ser removido.

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

### -Force
Indica que esse cmdlet não solicita confirmação.

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

### -VolumeContainer
Especifica o contêiner de volume a ser removido, como um objeto **DataContainer** .
Para obter um objeto **DataContainer** , use o cmdlet **Get-AzureStorSimpleDeviceVolumeContainer** .

```yaml
Type: DataContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WaitForComplete
Indica que esse cmdlet aguarda a conclusão da operação antes de retornar o controle ao console do Windows PowerShell.

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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### DataContainer
Esse cmdlet aceita um objeto **DataContainer** a ser removido.

## EXIBE

### TaskStatusInfo
Esse cmdlet retorna um objeto **TaskStatusInfo** , se você especificar o parâmetro *WaitForComplete* .

## INFORMA

## LINKS RELACIONADOS

[Get-AzureStorSimpleDeviceVolumeContainer](./Get-AzureStorSimpleDeviceVolumeContainer.md)

[New-AzureStorSimpleDeviceVolumeContainer](./New-AzureStorSimpleDeviceVolumeContainer.md)


