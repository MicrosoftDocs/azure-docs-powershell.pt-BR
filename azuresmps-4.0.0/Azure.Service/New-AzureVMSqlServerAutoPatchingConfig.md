---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7317DAC1-B535-4650-86BF-73E96F61EECD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 23bb8e09fac8ec4fe0e8ff5b3c23ab995f03694c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946191"
---
# New-AzureVMSqlServerAutoPatchingConfig

## Sinopse
Cria um objeto de configuração para a aplicação de patch automática da máquina virtual.

## SYNTAX

```
New-AzureVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>] [-MaintenanceWindowStartingHour <Int32>]
 [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzureVMSqlServerAutoPatchingConfig** cria um objeto de configuração para o patch automático da máquina virtual.

## EXEMPLOS

### Exemplo 1: criar um objeto de configuração para configurar a aplicação de patch automática
```
PS C:\> $APS = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
          Enable                        : True
          DayOfWeek                     : Thursday
          MaintenanceWindowStartingHour : 11
          MaintenanceWindowDuration     : 120
          PatchCategory                 : Important
```

Esse comando cria um objeto de configuração que pode ser usado para configurar a aplicação de patch automática usando Set-AzureVMSqlServerExtension.

## OS

### -DayOfWeek
Especifica o dia da semana em que as atualizações devem ser instaladas.

Os valores aceitáveis para esse parâmetro são:

- Domingo
- Sexta
- -
- Feira
- Terça
- Às
- Sábado
- Diário

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

### -Habilitar
Indica que a aplicação de patch automatizada para a máquina virtual está habilitada.
Se você habilitar a aplicação de patch automatizada, o cmdlet colocará o Windows Update no modo interativo.
Se você desabilitar a aplicação de patch automatizada, as configurações do Windows Update não serão alteradas.

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

### -Informationaction
Especifica como esse cmdlet responde a um evento de informações.

Os valores aceitáveis para esse parâmetro são:

- Contínuo
- Ignorar
- Inquire
- SilentlyContinue
- Finaliza
- Suspensão

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Especifica uma variável de informações.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaintenanceWindowDuration
Especifica a duração da janela de manutenção.
A aplicação de patch automatizada evitará executar uma ação que pode afetar a disponibilidade de uma máquina virtual fora da janela.
Somente incrementos de 30 minutos são permitidos.

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

### -MaintenanceWindowStartingHour
Especifica a hora do dia em que a janela de manutenção é iniciada.
Esse tempo define quando as atualizações iniciam a instalação e são arredondadas para a hora.

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

### -PatchCategory
Especifica se atualizações importantes devem ser incluídas.

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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

### AutoPatchingSettings
Este cmdlet retorna um objeto que contém as configurações de correção automática.

## INFORMA

## LINKS RELACIONADOS

[Set-AzureVMSqlServerExtension](./Set-AzureVMSqlServerExtension.md)

[Remove-AzureVMSqlServerExtension](./Remove-AzureVMSqlServerExtension.md)

[Set-AzureVMSqlServerExtension](./Set-AzureVMSqlServerExtension.md)


