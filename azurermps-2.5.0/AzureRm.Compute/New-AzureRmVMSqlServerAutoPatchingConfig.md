---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmsqlserverautopatchingconfig
schema: 2.0.0
ms.openlocfilehash: 1204a8b14cdbb45f46edd2a1ca2e4c12c27845a3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786170"
---
# New-AzureRmVMSqlServerAutoPatchingConfig

## Sinopse
Cria um objeto de configuração para a aplicação de patch automática em uma máquina virtual.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
New-AzureRmVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>]
 [-MaintenanceWindowStartingHour <Int32>] [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzureRmVMSqlServerAutoPatchingConfig** cria um objeto de configuração para a aplicação de patch automática em uma máquina virtual.

## EXEMPLOS

### Exemplo 1: criar um objeto de configuração para configurar a aplicação de patch automática
```
PS C:\> $AutoPatchingConfig = New-AzureRmVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

Esse comando cria o objeto de configuração para a aplicação de patch.
O comando especifica o dia da semana e define a janela de manutenção.
Essa configuração permite o patching que usa esses valores.
O comando armazena o resultado na variável $AutoBackupConfig.
Você pode especificar esse item de configuração para outros cmdlets, como o cmdlet Set-AzureRmVMSqlServerExtension.

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
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Everyday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Habilitar
Indica que a aplicação de patch automatizada para a máquina virtual está habilitada.
Se você habilitar a aplicação de patch automatizada, o cmdlet colocará o Windows Update no modo interativo.
Se você desabilitar a aplicação de patch automatizada, as configurações do Windows Update não são alteradas.

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

### -MaintenanceWindowDuration
Especifica a duração, em minutos, da janela de manutenção.
A aplicação de patch automatizada evita executar uma ação que pode afetar uma disponibilidade da máquina virtual fora da janela.
Especifique um múltiplo de 30 minutos.

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
Esse tempo define quando as atualizações começam a ser instaladas.

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
Accepted values: Important

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
Esse cmdlet não aceita nenhuma entrada.

## EXIBE

### AutoPatchingSettings
Este cmdlet retorna um objeto que contém as configurações de correção automática.

## INFORMA

## LINKS RELACIONADOS



[Set-AzureRmVMSqlServerExtension](./Set-AzureRMVMSqlServerExtension.md)


