---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverautopatchingconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: 3ba7ab00076a3a0634a0d4394270fe4a83ec8ede
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398250"
---
# New-AzVMSqlServerAutoPatchingConfig

## Sinopse
Cria um objeto de configuração para o patch automático em uma máquina virtual.

## Sintaxe

```
New-AzVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>]
 [-MaintenanceWindowStartingHour <Int32>] [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>]
 [<CommonParameters>]
```

## Descrição
O cmdlet **New-AzVMSqlServerAutoPatchingConfig** cria um objeto de configuração para o patch automático em uma máquina virtual.

## Exemplos

### Exemplo 1: Criar um objeto de configuração para configurar o patch automático
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

Esse comando cria um objeto de configuração para patch.
O comando especifica o dia da semana e define a janela de manutenção.
Essa configuração habilita o patch que usa esses valores.
O comando armazena o resultado na variável $AutoBackupConfig dados.
Você pode especificar esse item de configuração para outros cmdlets, como o Set-AzVMSqlServerExtension cmdlet.

## Parâmetros

### -DayOfWeek
Especifica o dia da semana em que as atualizações devem ser instaladas.

Os valores aceitáveis para este parâmetro são:

- Domingo
- Segunda-feira
- Terça
- Quarta
- Quinta
- Sexta
- Sábado
- Diária

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
Indica que o patch automatizado para o computador virtual está habilitado.
Se você habilitar o patch automático, o cmdlet colocará o Windows Update no modo interativo.
Se você desabilitar o patch automático, as configurações do Windows Update não mudarão.

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
O patch automatizado evita a execução de uma ação que pode afetar a disponibilidade de uma máquina virtual fora dessa janela.
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
Esse horário define quando as atualizações começam a ser instaladas.

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
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Entradas

### Nenhum
Este cmdlet não aceita nenhuma entrada.

## Saídas

### AutoPatchingSettings
Este objeto de retorno de cmdlet contém configurações para o patch automático.

## Notas

## LINKS RELACIONADOS

[New-AzureVMSqlServerAutoBackupConfig](./New-AzVMSqlServerAutoBackupConfig.md)

[Set-AzVMSqlServerExtension](./Set-AzVMSqlServerExtension.md)


