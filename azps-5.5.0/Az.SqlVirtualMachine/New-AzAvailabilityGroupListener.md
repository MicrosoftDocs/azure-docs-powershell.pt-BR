---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/new-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzAvailabilityGroupListener.md
ms.openlocfilehash: af36c7cae36cb3d6bdb9bf2760b9a8299463e877
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116120"
---
# New-AzAvailabilityGroupListener

## Sinopse
Cria um novo Ouvinte de Grupo de Disponibilidade.

## Sintaxe

### Nome (Padrão)
```
New-AzAvailabilityGroupListener -AvailabilityGroupName <String> [-Port <Int32>]
 -LoadBalancerResourceId <String> [-IpAddress <String>] [-SubnetId <String>] -ProbePort <Int32>
 [-PublicIpAddressResourceId <String>] [-AsJob] -SqlVirtualMachineId <String[]> [-ResourceGroupName] <String>
 [-SqlVMGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SqlVmGroupObject
```
New-AzAvailabilityGroupListener -AvailabilityGroupName <String> [-Port <Int32>]
 -LoadBalancerResourceId <String> [-IpAddress <String>] [-SubnetId <String>] -ProbePort <Int32>
 [-PublicIpAddressResourceId <String>] [-AsJob] -SqlVirtualMachineId <String[]>
 [-SqlVMGroupObject] <AzureSqlVMGroupModel> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrição
O New-AzAvailabilityGroupListener cmdlet cria um novo Ouvinte do Grupo de Disponibilidade.

## Exemplos

### Exemplo 1
```powershell
PS C:\> New-AzAvailabilityGroupListener -AvailabilityGroupName AvailabilityGroup01 -LoadBalancerResourceId $LoadBalanceResourceId -SubnetId $SubnetId -ProbePort 59999 -SqlVirtualMachineId $VmResourceId1,$VmResourceId2 -Name AgListener01  -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -IpAddress 10.0.0.3
```

Nome ResourceGroupName GroupName AvailabilityGroupName
----         ----------------- ---------    ---------------------
AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01

Cria um novo Grupo de Disponibilidade Do Ouvinte AgListener01 para o Grupo de Disponibilidade AvailabilityGroup01 no SQL Virtual Machine Group SqlVmGroup01.

## Parâmetros

### -AsJob
Executar cmdlet em segundo plano.

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

### -AvailabilityGroupName
Nome do Grupo de Disponibilidade.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.

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

### -IpAddress
Endereço Ip Particular

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LoadBalancerResourceId
ID do Balanceador de Carga

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Nome do Ouvinte do Grupo de Disponibilidade.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Porta
Número da porta do AG Listener. O Valor Padrão é 1433.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Eleport
Porta Descarrém

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicIpAddressResourceId
ID do Recurso de Endereço Ip Público

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
O nome do grupo de recursos.

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SqlVirtualMachineId
Lista de IDs de Recursos do Sql VM

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SqlVMGroupName
Nome do grupo de máquina virtual SQL.

```yaml
Type: System.String
Parameter Sets: Name
Aliases: GroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SqlVMGroupObject
Objeto do grupo de máquinas virtuais SQL.

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel
Parameter Sets: SqlVmGroupObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Sub-RedeId
ID do Recurso da Sub-rede

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
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

### Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel

## Saídas

### Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel

## Notas

## LINKS RELACIONADOS
