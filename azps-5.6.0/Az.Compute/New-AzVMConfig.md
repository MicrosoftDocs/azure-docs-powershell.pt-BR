---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
ms.openlocfilehash: 71aa555528ff1cdb5748c1a4ac62481ddd17c17c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890450"
---
# New-AzVMConfig

## SYNOPSIS
Cria um objeto de máquina virtual configurável.

## SINTAXE

### DefaultParameterSet (Padrão)
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-Zone <String[]>] [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>]
 [-MaxPrice <Double>] [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD] 
 [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ExplicitIdentityParameterSet
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>]
 [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>] [-MaxPrice <Double>]
 [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIPTION
O cmdlet **New-AzVMConfig** cria um objeto de máquina virtual local configurável para o Azure.
Outros cmdlets podem ser usados para configurar um objeto de máquina virtual, como Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface e Set-AzVMOSDisk.

## EXEMPLOS

### Exemplo 1: Criar um objeto de máquina virtual
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

O primeiro comando obtém o conjunto de disponibilidade chamado AvailabilitySet03 no grupo de recursos chamado ResourceGroup11 e armazena esse objeto na variável $AvailabilitySet.
O segundo comando cria um objeto de máquina virtual e o armazena na variável $VirtualMachine.
O comando atribui um nome e tamanho à máquina virtual.
A máquina virtual pertence ao conjunto de disponibilidade armazenado $AvailabilitySet.

## PARÂMETROS

### -AvailabilitySetId
Especifica a ID de um conjunto de disponibilidade.
Para obter um objeto de conjunto de disponibilidade, use o cmdlet Get-AzAvailabilitySet de disponibilidade.
O objeto de conjunto de disponibilidade contém uma propriedade ID. <br>
As máquinas virtuais especificadas no mesmo conjunto de disponibilidade são alocadas para nós diferentes para maximizar a disponibilidade. <br>
Para obter mais informações sobre conjuntos de disponibilidade, consulte [Manage the availability of virtual machines](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-manage-availability?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json). <br>
Para obter mais informações sobre a manutenção planejada do Azure, consulte [Manutenção planejada para máquinas virtuais no Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-planned-maintenance?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json) <br>
Atualmente, uma VM só pode ser adicionada ao conjunto de disponibilidade no momento da criação. O conjunto de disponibilidade ao qual a VM está sendo adicionada deve estar no mesmo grupo de recursos que o recurso de conjunto de disponibilidade. Uma VM existente não pode ser adicionada a um conjunto de disponibilidade. <br>
Essa propriedade não pode existir juntamente com uma referência properties não nulo.virtualMachineScaleSet.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.

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

### -EnableUltraSSD
Permite que um recurso tenha um ou mais discos de dados gerenciados com UltraSSD_LRS tipo de conta de armazenamento na VM.
Discos gerenciados com tipo de conta de armazenamento UltraSSD_LRS podem ser adicionados a uma máquina virtual somente se essa propriedade estiver habilitada.


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EvictionPolicy
A política de despejo da máquina virtual do Azure Spot.  Os valores com suporte são 'Deallocate' e 'Delete'.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -HostId
A ID do Host

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IdentityId
Especifica a lista de identidades de usuário associadas ao conjunto de escala de máquina virtual.
As referências de identidade do usuário serão ARM ids de recurso no formato: '/subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identity/{identityName}'

```yaml
Type: System.String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IdentityType
A identidade da máquina virtual, se configurada.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LicenseType
Especifica um tipo de licença, que indica que a imagem ou o disco da máquina virtual foi licenciada no local.
Os valores possíveis para o Windows Server são:
- Windows_Client
- Windows_Server valores possíveis para o sistema operacional Linux Server são: 
- RHEL_BYOS (para RHEL) 
- SLES_BYOS (para SUSE) 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxPrice
Especifica o preço máximo que você está disposto a pagar por uma VM/VMSS de baixa prioridade. Esse preço está em dólares dos EUA. Esse preço será comparado com o preço atual de baixa prioridade para o tamanho da VM. Além disso, os preços são comparados no momento da criação/atualização da VM/VMSS de baixa prioridade e a operação só terá êxito se o maxPrice for maior do que o preço de baixa prioridade atual. O maxPrice também será usado para despejar uma VM/VMSS de baixa prioridade se o preço atual de baixa prioridade for além do maxPrice após a criação de VM/VMSS. Os valores possíveis são: qualquer valor decimal maior que zero. Exemplo: 0,01538.  -1 indica que a VM/VMSS de baixa prioridade não deve ser despejada por motivos de preço. Além disso, o preço máximo padrão será -1 se não for fornecido por você.

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EncryptionAtHost
A propriedade EncryptionAtHost pode ser usada pelo usuário na solicitação para habilitar ou desabilitar a Criptografia de Host para o conjunto de escala de máquina virtual ou máquina virtual. Isso habilitará a criptografia para todos os discos, incluindo o disco Resource/Temp no próprio host. Padrão: a Criptografia no host será desabilitada, a menos que essa propriedade seja definida como true para o recurso.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Priority
A prioridade para a máquina virtual.  Somente os valores com suporte são 'Regular', 'Spot' e 'Low'.
'Regular' é para máquina virtual regular.
'Spot' é para máquina virtual local.
'Baixo' também é para máquina virtual local, mas é substituído por 'Spot'. Use 'Spot' em vez de 'Low'.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ProximityPlacementGroupId
A id de recurso do Grupo de Posicionamento de Proximidade a ser usado com essa máquina virtual.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tags
As marcas anexadas ao recurso.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
Especifica um nome para a máquina virtual.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMSize
Especifica o tamanho da máquina virtual.

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

### -VmssId
A ID do conjunto de escala de máquina virtual

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Zone
Especifica a lista de zonas de disponibilidade da máquina virtual. Os valores permitidos dependem dos recursos da região. Os valores permitidos normalmente serão 1,2,3.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String

### System.String[]

### System.Collections.Hashtable

### System.Management.Automation.SwitchParameter

## SAÍDAS

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

## NOTES

## LINKS RELACIONADOS

[Update-AzVM](./Update-AzVM.md)

[Set-AzVMOperatingSystem](./Set-AzVMOperatingSystem.md)

[Set-AzVMSourceImage](./Set-AzVMSourceImage.md)

[Get-AzAvailabilitySet](./Get-AzAvailabilitySet.md)


