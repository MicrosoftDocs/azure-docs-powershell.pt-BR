---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 3FADEC2E-4A2B-46EB-8A94-CF48D717C7FC
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/set-azdtlautostartpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAutoStartPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAutoStartPolicy.md
ms.openlocfilehash: 0692b828c03846f0c6f61a5f66b692a29616d848
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115343"
---
# Set-AzDtlAutoStartPolicy

## Sinopse
Define a política de início automático de um laboratório no DevTest Labs.

## Sintaxe

### Habilitar (Padrão)
```
Set-AzDtlAutoStartPolicy [[-Time] <DateTime>] [[-Days] <DayOfWeek[]>] [-Enable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Desativar
```
Set-AzDtlAutoStartPolicy [[-Time] <DateTime>] [[-Days] <DayOfWeek[]>] [-Disable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Descrição
O cmdlet **Set-AzDtlAutoStartPolicy** define a política de início automático de um laboratório, que permite que máquinas virtuais de laboratório sejam agendadas para início automático.
O cmdlet usa o grupo de recursos especificado e o nome do laboratório para definir a política.

## Exemplos

### Exemplo 1

Define a política de início automático de um laboratório no DevTest Labs. (gerado automaticamente)

```powershell <!-- Aladdin Generated Example --> 
Set-AzDtlAutoStartPolicy -Days Sunday -Enable -LabName <String> -ResourceGroupName MyResourceGroup -Time <DateTime>
```

## Parâmetros

### -Dias
Especifica, como uma matriz, os dias da semana para quando as máquinas virtuais do laboratório devem ser iniciadas.

```yaml
Type: System.DayOfWeek[]
Parameter Sets: (All)
Aliases:
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Desabilitar
Indica que esse cmdlet desabilita a política para as máquinas virtuais no laboratório.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Disable
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Habilitar
Indica que esse cmdlet habilita a política para as máquinas virtuais no laboratório.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Enable
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LabName
Especifica o nome do laboratório para o qual este cmdlet define a política de início automático.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome do grupo de recursos ao que o laboratório pertence.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Hora
Especifica o horário em que as máquinas virtuais do laboratório devem ser iniciadas.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirmar
Solicita confirmação antes de executar o cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra o que acontece se o cmdlet for executado.
O cmdlet não é executado.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Entradas

### System.String

## Saídas

### Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule

## Notas

## LINKS RELACIONADOS

[Get-AzDtlAutoStartPolicy](./Get-AzDtlAutoStartPolicy.md)


