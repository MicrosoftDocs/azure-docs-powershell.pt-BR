---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azvmsqlserverautopatchingconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: 3433d6bf5d3886978b75024e34c873e38230212b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891869"
---
# New-AzVMSqlServerAutoPatchingConfig

## SYNOPSIS
Cria um objeto de configuração para o patch automático em uma máquina virtual.

## SINTAXE

```
New-AzVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>] [-MaintenanceWindowStartingHour <Int32>]
 [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>] [<CommonParameters>]
```

## DESCRIPTION
O cmdlet **New-AzVMSqlServerAutoPatchingConfig** cria um objeto de configuração para o patch automático em uma máquina virtual.

## EXEMPLOS

### Exemplo 1: Criar um objeto de configuração para configurar o patch automático
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

Este comando cria um objeto de configuração para correção.
O comando especifica o dia da semana e define a janela de manutenção.
Essa configuração habilita o patch que usa esses valores.
O comando armazena o resultado na variável $AutoBackupConfig.
Você pode especificar esse item de configuração para outros cmdlets, como o Set-AzVMSqlServerExtension cmdlet.

## PARÂMETROS

### -DayOfWeek
Especifica o dia da semana em que as atualizações devem ser instaladas.
Os valores aceitáveis para este parâmetro são:
- Domingo
- Segunda-feira
- Terça-feira
- Quarta-feira
- Quinta-feira
- Sexta-feira
- Sábado
- Todos os dias

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Everyday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Enable
Indica que a correção automatizada para a máquina virtual está habilitada.
Se você habilitar o patch automatizado, o cmdlet colocará o Windows Update no modo interativo.
Se você desabilitar o patch automático, as configurações do Windows Update não mudarão.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaintenanceWindowDuration
Especifica a duração, em minutos, da janela de manutenção.
A correção automatizada evita a execução de uma ação que pode afetar a disponibilidade de uma máquina virtual fora dessa janela.
Especifique um múltiplo de 30 minutos.

```yaml
Type: System.Int32
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
Este tempo define quando as atualizações começam a ser instaladas.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PatchCategory
Especifica se as atualizações importantes devem ser incluídas.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Important

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Nenhum

## SAÍDAS

### Microsoft.Azure.Commands.Compute.AutoPatchingSettings

## NOTES

## LINKS RELACIONADOS

[New-AzVMSqlServerAutoBackupConfig](./New-AzVMSqlServerAutoBackupConfig.md)

[Set-AzVMSqlServerExtension](./Set-AzVMSqlServerExtension.md)


