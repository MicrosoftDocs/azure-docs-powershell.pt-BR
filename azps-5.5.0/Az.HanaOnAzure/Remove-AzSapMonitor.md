---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/remove-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitor.md
ms.openlocfilehash: bcba06d87bce2f9ccc8016afc9f08dff75e29b1c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113173"
---
# Remove-AzSapMonitor

## Sinopse
Exclui um monitor SAP com a assinatura especificada, o grupo de recursos e o nome do monitor.

## Sintaxe

### Excluir (Padrão)
```
Remove-AzSapMonitor -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### DeleteViaIdentity
```
Remove-AzSapMonitor -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## Descrição
Exclui um monitor SAP com a assinatura especificada, o grupo de recursos e o nome do monitor.

## Exemplos

### Exemplo 1: Remover um monitor SAP por nome
```powershell
PS C:\> Remove-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-sapmonitor-t02

```

Esse comando remove um monitor SAP por nome.

### Exemplo 2: Remover um monitor SAP por objeto
```powershell
PS C:\> $sap = Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-sapmonitor-t01
PS C:\> Remove-AzSapMonitor -InputObject $sap

```

Esse comando remove um monitor SAP por objeto.

## Parâmetros

### -AsJob
Executar o comando como um trabalho

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

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Nome
Nome do recurso de monitor SAP.

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: SapMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWait
Executar o comando assíncrona

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

### -PassThru
Retorna verdadeiro quando o comando é bem-sucedido

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

### -ResourceGroupName
Nome do grupo de recursos.

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.
A ID da assinatura faz parte do URI para cada chamada de serviço.

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
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
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## Entradas

### Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity

## Saídas

### System.Boolean

## Notas

Aliases

PROPRIEDADES DE PARÂMETRO COMPLEXOS

Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas. Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.


INPUTOBJECT: <IHanaOnAzureIdentity> Parâmetro de Identidade
  - `[Id <String>]`: Caminho de identidade de recursos
  - `[Location <String>]`: o local do cofre excluído.
  - `[OperationKind <AccessPolicyUpdateKind?>]`: Nome da operação
  - `[ProviderInstanceName <String>]`: Nome da instância do provedor.
  - `[ResourceGroupName <String>]`: Nome do grupo de recursos.
  - `[ResourceName <String>]`: o nome do recurso de identidade.
  - `[SapMonitorName <String>]`: Nome do recurso de monitor SAP.
  - `[Scope <String>]`: o escopo do provedor de recursos do recurso. Recurso pai sendo estendido por Identidades Gerenciadas.
  - `[SubscriptionId <String>]`: ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure. A ID da assinatura faz parte do URI para cada chamada de serviço.
  - `[VaultName <String>]`: Nome do cofre

## LINKS RELACIONADOS

