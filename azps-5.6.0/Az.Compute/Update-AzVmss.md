---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/powershell/module/az.compute/update-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
ms.openlocfilehash: fbdefd7e80e0054bbef8e12614316f7b23ff134a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901500"
---
# Update-AzVmss

## SYNOPSIS
Atualiza o estado de um VMSS.

## SINTAXE

### DefaultParameter (Padrão)
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-AutomaticOSUpgrade <Boolean>]
 [-AutomaticRepairGracePeriod <String>] [-BootDiagnosticsEnabled <Boolean>]
 [-BootDiagnosticsStorageUri <String>] [-CustomData <String>] [-DisableAutoRollback <Boolean>]
 [-DisablePasswordAuthentication <Boolean>] [-EnableAutomaticRepair <Boolean>]
 [-EnableAutomaticUpdate <Boolean>] [-ImageReferenceId <String>] [-ImageReferenceOffer <String>]
 [-ImageReferencePublisher <String>] [-ImageReferenceSku <String>] [-ImageReferenceVersion <String>]
 [-ImageUri <String>] [-LicenseType <String>] [-ManagedDiskStorageAccountType <String>]
 [-MaxBatchInstancePercent <Int32>] [-MaxPrice <Double>] [-MaxUnhealthyInstancePercent <Int32>]
 [-MaxUnhealthyUpgradedInstancePercent <Int32>] [-OsDiskCaching <CachingTypes>]
 [-OsDiskWriteAccelerator <Boolean>] [-Overprovision <Boolean>] [-PauseTimeBetweenBatches <String>]
 [-PlanName <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>] [-PlanPublisher <String>]
 [-ProvisionVMAgent <Boolean>] [-ProximityPlacementGroupId <String>] [-ScaleInPolicy <String[]>]
 [-SinglePlacementGroup <Boolean>] [-SkipExtensionsOnOverprovisionedVMs <Boolean>] [-SkuCapacity <Int32>]
 [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-TerminateScheduledEvents <Boolean>]
 [-TimeZone <String>] [-UltraSSDEnabled <Boolean>] [-UpgradePolicyMode <UpgradeMode>]
 [-VhdContainer <String[]>] [-AsJob] [-EncryptionAtHost <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ExplicitIdentityParameterSet
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-AutomaticOSUpgrade <Boolean>]
 [-AutomaticRepairGracePeriod <String>] [-BootDiagnosticsEnabled <Boolean>]
 [-BootDiagnosticsStorageUri <String>] [-CustomData <String>] [-DisableAutoRollback <Boolean>]
 [-DisablePasswordAuthentication <Boolean>] [-EnableAutomaticRepair <Boolean>]
 [-EnableAutomaticUpdate <Boolean>] [-IdentityId <String[]>] -IdentityType <ResourceIdentityType>
 [-ImageReferenceId <String>] [-ImageReferenceOffer <String>] [-ImageReferencePublisher <String>]
 [-ImageReferenceSku <String>] [-ImageReferenceVersion <String>] [-ImageUri <String>] [-LicenseType <String>]
 [-ManagedDiskStorageAccountType <String>] [-MaxBatchInstancePercent <Int32>] [-MaxPrice <Double>]
 [-MaxUnhealthyInstancePercent <Int32>] [-MaxUnhealthyUpgradedInstancePercent <Int32>]
 [-OsDiskCaching <CachingTypes>] [-OsDiskWriteAccelerator <Boolean>] [-Overprovision <Boolean>]
 [-PauseTimeBetweenBatches <String>] [-PlanName <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>] [-ProximityPlacementGroupId <String>]
 [-ScaleInPolicy <String[]>] [-SinglePlacementGroup <Boolean>] [-SkipExtensionsOnOverprovisionedVMs <Boolean>]
 [-SkuCapacity <Int32>] [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-TerminateScheduledEvents <Boolean>]
 [-TimeZone <String>] [-UltraSSDEnabled <Boolean>] [-UpgradePolicyMode <UpgradeMode>]
 [-VhdContainer <String[]>] [-AsJob] [-EncryptionAtHost <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
O cmdlet **Update-AzVmss** atualiza o estado de um Conjunto de Escala de Máquina Virtual (VMSS) para o estado de um objeto VMSS local.

## EXEMPLOS

### Exemplo 1: atualize o estado de um VMSS para o estado de um objeto VMSS local.
```
PS C:\> Update-AzVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

Este comando atualiza o estado do VMSS chamado VMSS001 que pertence ao grupo de recursos chamado Group001 ao estado de um objeto VMSS local, $LocalVMSS.

## PARÂMETROS

### -AsJob
Execute o cmdlet em segundo plano e retorne um Trabalho para controlar o progresso.

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

### -AutomaticOSUpgrade
Define se as atualizações do sistema operacional devem ser aplicadas automaticamente às instâncias de conjunto de escalas de forma rolante quando uma versão mais recente da imagem se torna disponível.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AutomaticRepairGracePeriod
O tempo para o qual os reparos automáticos são suspensos devido a uma alteração de estado na VM. O tempo de carência começa após a conclusão da alteração de estado. Isso ajuda a evitar reparos prematuras ou acidentais. A duração do tempo deve ser especificada no formato ISO 8601. O período mínimo de carência permitido é de 30 minutos (PT30M), que também é o valor padrão. O período máximo permitido de carência é de 90 minutos (PT90M).

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

### -BootDiagnosticsEnabled
Se os diagnósticos de inicialização devem ser habilitados no conjunto de escala da máquina virtual.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BootDiagnosticsStorageUri
URI da conta de armazenamento a ser usada para colocar a saída do console e a captura de tela.

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

### -CustomData
Especifica uma cadeia de caracteres codificada com base 64 de dados personalizados.
Isso é decodificado para uma matriz binária que é salva como um arquivo na máquina virtual.
O comprimento máximo da matriz binária é 65535 bytes. <br>
Para usar o cloud-init para sua VM, consulte [Using cloud-init to customize a Linux VM during creation](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).

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

### -DisableAutoRollback
Desabilitar a Reação Automática para a Política de Atualização automática do sistema operacional

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisablePasswordAuthentication
Indica que esse cmdlet desabilita a autenticação de senha para o sistema operacional Linux.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableAutomaticRepair
Habilitar ou desabilitar reparos automáticos no conjunto de escala de máquina virtual.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableAutomaticUpdate
Indica se as máquinas virtuais do Windows no VMSS estão habilitadas para atualizações automáticas.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EncryptionAtHost
Esse parâmetro pode ser usado pelo usuário na solicitação para habilitar ou desabilitar a Criptografia host para o conjunto de escala de máquina virtual. 

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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
Accept pipeline input: False
Accept wildcard characters: False
```

### -IdentityType
Especifica o tipo de identidade usado para o conjunto de escala de máquina virtual.
O tipo "SystemAssignedUserAssigned" inclui uma identidade criada implicitamente e um conjunto de identidades atribuídas pelo usuário.
O tipo "Nenhum" removerá qualquer identidade do conjunto de escala de máquina virtual.
Os valores aceitáveis para este parâmetro são:
- SystemAssigned
- UserAssigned
- SystemAssignedUserAssigned
- Nenhum

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ImageReferenceId
Especifica a ID de referência da imagem.

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

### -ImageReferenceOffer
Especifica o tipo de oferta de imagem de máquina virtual (VMImage).
Para obter uma oferta de imagem, use Get-AzVMImageOffer cmdlet.

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

### -ImageReferencePublisher
Especifica o nome de um editor de um VMImage.
Para obter um editor, use o Get-AzVMImagePublisher cmdlet.

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

### -ImageReferenceSku
Especifica o SKU do VMImage.
Para obter SKUs, use o cmdlet Get-AzVMImageSku.

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

### -ImageReferenceVersion
Especifica a versão do VMImage.
Para usar a versão mais recente, especifique um valor mais recente em vez de uma versão específica.

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

### -ImageUri
Especifica o URI blob para a imagem do usuário.
O VMSS cria um disco do sistema operacional no mesmo contêiner da imagem do usuário.

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

### -LicenseType
Especifique o tipo de licença, que é para trazer seu próprio cenário de licença.

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

### -ManagedDiskStorageAccountType
Especifica o tipo de conta de armazenamento para disco gerenciado.
Os valores aceitáveis para este parâmetro são:
- StandardLRS
- PremiumLRS

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

### -MaxBatchInstancePercent
A porcentagem máxima do total de instâncias de máquina virtual que serão atualizadas simultaneamente pela atualização de rolagem em um lote.
Como isso é um máximo, instâncias não salubres em lotes anteriores ou futuros podem fazer com que a porcentagem de instâncias em um lote diminua para garantir maior confiabilidade.
Se o valor não for especificado, ele será definido como 20.

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

### -MaxPrice
Especifica o preço máximo que você está disposto a pagar por uma VM/VMSS de baixa prioridade. Esse preço está em dólares dos EUA. Esse preço será comparado com o preço atual de baixa prioridade para o tamanho da VM. Além disso, os preços são comparados no momento da criação/atualização da VM/VMSS de baixa prioridade e a operação só terá êxito se o maxPrice for maior do que o preço de baixa prioridade atual. O maxPrice também será usado para despejar uma VM/VMSS de baixa prioridade se o preço atual de baixa prioridade for além do maxPrice após a criação de VM/VMSS. Os valores possíveis são: qualquer valor decimal maior que zero. Exemplo: 0,01538.  -1 indica que a VM/VMSS de baixa prioridade não deve ser despejada por motivos de preço. Além disso, o preço máximo padrão será -1 se não for fornecido por você.

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxUnhealthyInstancePercent
A porcentagem máxima do total de instâncias de máquina virtual no conjunto de escala que podem ser simultaneamente não árias, como resultado da atualização ou por serem encontradas em um estado salubressuário pelas verificações de saúde da máquina virtual antes que a atualização de rolagem seja anulada.
Essa restrição será verificada antes de iniciar qualquer lote.
Se o valor não for especificado, ele será definido como 20.

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

### -MaxUnhealthyUpgradedInstancePercent
A porcentagem máxima de instâncias de máquina virtual atualizadas que podem ser encontradas em um estado não alub.
Essa verificação acontecerá depois que cada lote for atualizado.
Se essa porcentagem for sempre excedida, a atualização em circulação será anulada.
Se o valor não for especificado, ele será definido como 20.

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

### -OsDiskCaching
Especifica o modo de cache do disco do sistema operacional. Os valores aceitáveis para este parâmetro são:
- Nenhum
- ReadOnly
- ReadWrite O valor padrão é ReadWrite.
Se você alterar o valor de cache, o cmdlet reiniciará a máquina virtual.
Essa configuração afeta a consistência e o desempenho do disco.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.CachingTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OsDiskWriteAccelerator
Especifica se WriteAccelerator deve ser habilitado ou desabilitado no disco do sistema operacional.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Overprovision
Indica se o cmdlet sobreprovisiona o VMSS.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PauseTimeBetweenBatches
O tempo de espera entre concluir a atualização para todas as máquinas virtuais em um lote e iniciar o próximo lote.
A duração do tempo deve ser especificada no formato ISO 8601.
O valor padrão é 0 segundos (PT0S).

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

### -PlanName
Especifica o nome do plano.

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

### -PlanProduct
Especifica o produto do plano.

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

### -PlanPromotionCode
Especifica o código de promoção do plano.

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

### -PlanPublisher
Especifica o editor de planos.

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

### -ProvisionVMAgent
Indica se o agente de máquina virtual deve ser provisionado nas máquinas virtuais do Windows no VMSS.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProximityPlacementGroupId
A id de recurso do Grupo de Posicionamento de Proximidade a ser usado com esse conjunto de escala.

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
Especifica o nome do grupo de recursos ao que o VMSS pertence.

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

### -ScaleInPolicy
As regras a serem seguidas ao dimensionar um conjunto de escala de máquina virtual.  Os valores possíveis são: 'Default', 'OldestVM' e 'NewestVM'.  'Padrão' quando um conjunto de escala de máquina virtual é dimensionado, o conjunto de escala será balanceado primeiro entre zonas se for um conjunto de escala zonal.  Em seguida, ele será balanceado entre domínios de falha o mais longe possível.  Dentro de cada Domínio de Falha, as máquinas virtuais escolhidas para remoção serão as mais novas que não estão protegidas de dimensionar.  "OldestVM" quando um conjunto de escalas de máquina virtual está sendo dimensionado, as máquinas virtuais mais antigas que não estão protegidas contra a escala serão escolhidas para remoção.  Para conjuntos de escala de máquina virtual zonal, o conjunto de escalas primeiro será balanceado entre zonas.  Dentro de cada zona, as máquinas virtuais mais antigas que não estão protegidas serão escolhidas para remoção.  "NewestVM" quando um conjunto de escalas de máquina virtual está sendo dimensionado, as máquinas virtuais mais novas que não estão protegidas contra dimensionar serão escolhidas para remoção.  Para conjuntos de escala de máquina virtual zonal, o conjunto de escalas primeiro será balanceado entre zonas.  Dentro de cada zona, as máquinas virtuais mais novas que não estão protegidas serão escolhidas para remoção.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SinglePlacementGroup
Especifica o grupo de posicionamento único.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkipExtensionsOnOverprovisionedVMs
Especifica que as extensões não são executados nas VMs sobreprovisionadas extras.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkuCapacity
Especifica o número de instâncias no VMSS.

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

### -SkuName
Especifica o tamanho de todas as instâncias do VMSS.

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

### -SkuTier
Especifica a camada de VMSS.
Os valores aceitáveis para este parâmetro são:
- Standard
- Básico

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

### -Tag
Pares de valores-chave na forma de uma tabela de hash. Por exemplo: @{key0="value0";key1=$null;key2="value2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TerminateScheduledEventNotBeforeTimeoutInMinutes
Tempo configurável (em minutos) uma Máquina Virtual que está sendo excluída terá que aprovar potencialmente o Evento Encerrado Agendado antes que o evento seja aprovado automaticamente (tempo final).

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TerminateScheduledEvents
Especifica se o evento Encerrar Agendado está habilitado ou desabilitado.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TimeZone
Especifica o fuso horário do sistema operacional Windows. Por exemplo, Hora \" Padrão do Pacífico \" . <br>
Os valores possíveis podem [TimeZoneInfo.Id](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) de fusos horário retornados por [TimeZoneInfo.GetSystemTimeZones](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.getsystemtimezones).

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

### -UltraSSDEnabled
O sinalizador que habilita ou desabilita um recurso de ter um ou mais discos de dados gerenciados com UltraSSD_LRS de conta de armazenamento no conjunto de escala de máquina virtual.
Discos gerenciados com tipo de conta de armazenamento UltraSSD_LRS podem ser adicionados a um VMSS somente se essa propriedade estiver habilitada.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UpgradePolicyMode
Especificou o modo de atualização para máquinas virtuais no conjunto de escala.
Os valores aceitáveis para este parâmetro são:
- Automático
- Manual
- Rolling

```yaml
Type: Microsoft.Azure.Management.Compute.Models.UpgradeMode
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual, Rolling

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VhdContainer
Especifica as URLs de contêiner que são usadas para armazenar discos do sistema operacional para o VMSS.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualMachineScaleSet
Especifica um objeto VMSS local.
Para obter um objeto VMSS, use Get-AzVmss cmdlet.
Este objeto de máquina virtual contém o estado atualizado para o VMSS.

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VMScaleSetName
Especifica o nome do VMSS que este cmdlet cria.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
Solicita a confirmação antes de executar o cmdlet.

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
Mostra o que aconteceria se o cmdlet fosse executado.
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
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet

### System.Boolean

## SAÍDAS

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet

## NOTES

## LINKS RELACIONADOS

[Get-AzVmss](./Get-AzVmss.md)

[New-AzVmss](./New-AzVmss.md)

[Remove-AzVmss](./Remove-AzVmss.md)

[Restart-AzVmss](./Restart-AzVmss.md)

[Set-AzVmss](./Set-AzVmss.md)

[Start-AzVmss](./Start-AzVmss.md)

[Stop-AzVmss](./Stop-AzVmss.md)


