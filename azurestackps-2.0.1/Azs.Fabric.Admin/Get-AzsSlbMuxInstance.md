---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsslbmuxinstance
schema: 2.0.0
ms.openlocfilehash: 64e33236bbdd3f07969f6633356c98b593ee672f
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/24/2020
ms.locfileid: "93945307"
---
# Get-AzsSlbMuxInstance

## Sinopse
Retorna a instância solicitada do Multiplexador de balanceamento de carga do software.

## SYNTAX

### Lista (padrão)
```
Get-AzsSlbMuxInstance [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### Obter
```
Get-AzsSlbMuxInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzsSlbMuxInstance -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## DESCRITIVO
Retorna a instância solicitada do Multiplexador de balanceamento de carga do software.

## EXEMPLOS

### Exemplo 1:
```powershell
PS C:\> Get-AzsSlbMuxInstance

A list of all software load balancer multiplexer instance at a location.
```

Obtenha todas as instâncias do Multiplexador de balanceamento de carga de software em um local.

### Exemplo 2:
```powershell
PS C:\> Get-AzsSlbMuxInstance -Name "AzS-SLB01"

A specific software load balancer multiplexer instance at a location given a name.
```

Obtenha uma instância específica do Multiplexador de balanceamento de carga de software em um local em que o nome foi atribuído.

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.


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

### -Filtro
Parâmetro de filtro OData.

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -InputObject
Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### -Local
Local do recurso.

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### -Nome
Nome de uma instância de MUX SLB.

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
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
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### -SubscriptionId
Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.
A ID da assinatura forma a parte do URI para cada chamada de serviço.

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

### Microsoft. Azure. PowerShell. cmdlets. FabricAdmin. Models. IFabricAdminIdentity

## EXIBE

### Microsoft. Azure. PowerShell. cmdlets. FabricAdmin. Models. Api20160501. ISlbMuxInstance



## INFORMA

Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas. Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.

INPUTobject <IFabricAdminIdentity> : parâmetro de identidade
  - `[Drive <String>]`: Nome do drive de armazenamento.
  - `[EdgeGateway <String>]`: Nome do gateway de borda.
  - `[EdgeGatewayPool <String>]`: Nome do pool de gateways de borda.
  - `[FabricLocation <String>]`: Localização do fabric.
  - `[FileShare <String>]`: Nome do compartilhamento de arquivos do fabric.
  - `[IPPool <String>]`: Nome do pool de IP.
  - `[Id <String>]`: Caminho de identidade do recurso
  - `[InfraRole <String>]`: Nome da função de infraestrutura.
  - `[InfraRoleInstance <String>]`: Nome de uma instância de função de infraestrutura.
  - `[Location <String>]`: Local do recurso.
  - `[LogicalNetwork <String>]`: Nome da rede lógica.
  - `[LogicalSubnet <String>]`: Nome da sub-rede lógica.
  - `[MacAddressPool <String>]`: Nome do pool de endereços MAC.
  - `[Operation <String>]`: Identificador de operação.
  - `[ResourceGroupName <String>]`: Nome do grupo de recursos.
  - `[ScaleUnit <String>]`: Nome das unidades de escala.
  - `[ScaleUnitNode <String>]`: Nome do nó da unidade de escala.
  - `[SlbMuxInstance <String>]`: Nome de uma instância de MUX SLB.
  - `[StoragePool <String>]`: Nome do pool de armazenamento.
  - `[StorageSubSystem <String>]`: Nome do sistema de armazenamento.
  - `[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure. A ID da assinatura forma a parte do URI para cada chamada de serviço.
  - `[Volume <String>]`: Nome do volume de armazenamento.

## LINKS RELACIONADOS

