---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: A1E143A8-70F2-4158-9A10-F2082AD62A73
online version: ''
schema: 2.0.0
ms.openlocfilehash: 371291f4bd33809bc2f5880e4380c448219ed37a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946012"
---
# Stop-AzureStorSimpleJob

## Sinopse
Interrompe um trabalho do StorSimple.

## SYNTAX

```
Stop-AzureStorSimpleJob -InstanceId <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Stop-AzureStorSimpleJob** interrompe um trabalho do StorSimple em andamento.
Você pode especificar um trabalho fornecendo uma ID de instância ou um nome de trabalho.

## EXEMPLOS

### Exemplo 1: interromper trabalhos para um dispositivo
```
PS C:\>Get-AzureStorSimpleJob -DeviceName "Device07" | Stop-AzureStorSimpleJob -Force
```

Esse comando obtém os trabalhos para o dispositivo chamado Device07, usando o cmdlet **Get-AzureStorSimpleJob** .
O comando passa os trabalhos para o cmdlet atual usando o operador pipeline.
O cmdlet atual interrompe qualquer trabalho que o comando passa para ele.
O comando especifica o parâmetro *Force* e, portanto, não solicita confirmação antes de parar um trabalho.

### Exemplo 2: parar um trabalho específico
```
PS C:\>Stop-AzureStorSimpleJob -InstanceId "574f47e0-44e9-495c-b8a5-0203c57ebf6d" -Force
```

Esse comando interrompe o trabalho que tem a ID de instância especificada.

## OS

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

### -InstanceId
Especifica a ID do trabalho do dispositivo para parar.

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

### DeviceJobDetails
Esse cmdlet obtém detalhes do **DeviceJob** que este cmdlet interrompe.

## INFORMA

## LINKS RELACIONADOS

[Get-AzureStorSimpleJob](./Get-AzureStorSimpleJob.md)


