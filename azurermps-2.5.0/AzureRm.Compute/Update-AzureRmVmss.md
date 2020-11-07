---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermvmss
schema: 2.0.0
ms.openlocfilehash: 544af56c5e1ff72a3b23c3dcf89af36f7d74eff2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785533"
---
# Update-AzureRmVmss

## Sinopse
Atualiza o estado de um VMSS.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### Defaultparameter (padrão)
```
Update-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-ImageReferenceSku <String>]
 [-ManagedDiskStorageAccountType <StorageAccountTypes>] [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>]
 [-BootDiagnosticsEnabled <Boolean>] [-Overprovision <Boolean>] [-MaxBatchInstancePercent <Int32>]
 [-TimeZone <String>] [-BootDiagnosticsStorageUri <String>] [-AutomaticOSUpgrade <Boolean>]
 [-SinglePlacementGroup <Boolean>] [-CustomData <String>] [-UpgradePolicyMode <UpgradeMode>]
 [-ImageReferenceId <String>] [-DisablePasswordAuthentication <Boolean>] [-Tag <Hashtable>]
 [-PlanName <String>] [-MaxUnhealthyUpgradedInstancePercent <Int32>] [-ImageReferencePublisher <String>]
 [-PlanProduct <String>] [-VhdContainer <String[]>] [-ImageUri <String>] [-SkuTier <String>]
 [-EnableAutomaticUpdate <Boolean>] [-LicenseType <String>] [-SkuName <String>] [-PlanPromotionCode <String>]
 [-MaxUnhealthyInstancePercent <Int32>] [-SkuCapacity <Int32>] [-OsDiskWriteAccelerator <Boolean>]
 [-ImageReferenceOffer <String>] [-PauseTimeBetweenBatches <String>] [-OsDiskCaching <CachingTypes>]
 [-ImageReferenceVersion <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ExplicitIdentityParameterSet
```
Update-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-ImageReferenceSku <String>] [-IdentityId <String[]>]
 [-ManagedDiskStorageAccountType <StorageAccountTypes>] [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>]
 [-BootDiagnosticsEnabled <Boolean>] [-Overprovision <Boolean>] [-MaxBatchInstancePercent <Int32>]
 [-TimeZone <String>] [-BootDiagnosticsStorageUri <String>] [-AutomaticOSUpgrade <Boolean>]
 [-SinglePlacementGroup <Boolean>] [-CustomData <String>] [-UpgradePolicyMode <UpgradeMode>]
 [-ImageReferenceId <String>] [-DisablePasswordAuthentication <Boolean>] [-Tag <Hashtable>]
 [-PlanName <String>] [-MaxUnhealthyUpgradedInstancePercent <Int32>] [-ImageReferencePublisher <String>]
 [-PlanProduct <String>] [-VhdContainer <String[]>] [-ImageUri <String>] [-SkuTier <String>]
 [-EnableAutomaticUpdate <Boolean>] [-LicenseType <String>] -IdentityType <ResourceIdentityType>
 [-SkuName <String>] [-PlanPromotionCode <String>] [-MaxUnhealthyInstancePercent <Int32>]
 [-SkuCapacity <Int32>] [-OsDiskWriteAccelerator <Boolean>] [-ImageReferenceOffer <String>]
 [-PauseTimeBetweenBatches <String>] [-OsDiskCaching <CachingTypes>] [-ImageReferenceVersion <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Update-AzureRmVmss** atualiza o estado de um VMSS (conjunto de dimensionamento de máquina virtual) para o estado de um objeto VMSS local.

## EXEMPLOS

### Exemplo 1: Atualize o estado de um VMSS para o estado de um objeto VMSS local.
```
PS C:\> Update-AzureRmVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

Esse comando atualiza o estado do VMSS chamado VMSS001 que pertence ao grupo de recursos chamado Group001 para o estado de um objeto VMSS local, $LocalVMSS.

## OS

### -AsJob
Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.

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

### -AutomaticOSUpgrade
Define se as atualizações do sistema operacional devem ser aplicadas automaticamente às instâncias do conjunto de escala de forma contínua quando uma versão mais recente da imagem se torna disponível.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BootDiagnosticsEnabled
Se o diagnóstico de inicialização deve ser habilitado no conjunto de escala da máquina virtual.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BootDiagnosticsStorageUri
URL da conta de armazenamento a ser usada para colocar a captura de tela e a saída do console.

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

### -CustomData
Especifica uma cadeia de caracteres de dados personalizados codificada como base-64.
Isso é decodificado para uma matriz binária salva como um arquivo na máquina virtual.
O comprimento máximo da matriz binária é de 65535 bytes.

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

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisablePasswordAuthentication
Indica que esse cmdlet desabilita a autenticação de senha para o SO Linux.

```yaml
Type: Boolean
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
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Identityid
Especifica a lista de identidades de usuário associadas ao conjunto de escalas da máquina virtual.
As referências de identidade do usuário serão identificadores de recurso ARM no formato: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '

```yaml
Type: String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IdentityType
Especifica o tipo de identidade usado para o conjunto de escala da máquina virtual.
O tipo ' SystemAssignedUserAssigned ' inclui uma identidade criada implicitamente e um conjunto de identidades atribuídas ao usuário.
O tipo ' nenhum ' removerá todas as identidades do conjunto de escala da máquina virtual.
Os valores aceitáveis para esse parâmetro são:

- SystemAssigned
- Userassigned
- SystemAssignedUserAssigned
- Nenhuma

```yaml
Type: ResourceIdentityType
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
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ImageReferenceOffer
Especifica o tipo de oferta da máquina virtual da máquina (VMImage).
Para obter uma oferta de imagem, use o cmdlet Get-AzureRmVMImageOffer.

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

### -ImageReferencePublisher
Especifica o nome de um fornecedor de uma VMImage.
Para obter um fornecedor, use o cmdlet Get-AzureRmVMImagePublisher.

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

### -ImageReferenceSku
Especifica o SKU da VMImage.
Para obter os SKUs, use o cmdlet Get-AzureRmVMImageSku.

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

### -ImageReferenceVersion
Especifica a versão da VMImage.
Para usar a versão mais recente, especifique um valor mais recente em vez de uma versão específica.

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

### -ImageUri
Especifica o URI do blob para a imagem do usuário.
O VMSS cria um disco do sistema operacional no mesmo contêiner da imagem do usuário.

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

### -LicenseType
Especifique o tipo de licença, que é para colocar seu próprio cenário de licença.

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

### -ManagedDiskStorageAccountType
Especifica o tipo de conta de armazenamento para o disco gerenciado.
Os valores aceitáveis para esse parâmetro são:

- StandardLRS
- PremiumLRS

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxBatchInstancePercent
A porcentagem máxima do total de instâncias da máquina virtual que serão atualizadas simultaneamente pela atualização sem interrupção em um lote.
Como se trata de um valor máximo, instâncias não íntegras em lotes anteriores ou futuros podem fazer com que a porcentagem de instâncias em um lote seja reduzida para garantir maior confiabilidade.
Se o valor não for especificado, será definido como 20.

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

### -MaxUnhealthyInstancePercent
A porcentagem máxima do total de instâncias da máquina virtual no conjunto de escala que podem ser simultaneamente não íntegras, como resultado da atualização ou por estar em um estado não íntegro pelas verificações de integridade da máquina virtual antes de anular a atualização sem interrupção.
Esta restrição será verificada antes de iniciar qualquer lote.
Se o valor não for especificado, será definido como 20.

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

### -MaxUnhealthyUpgradedInstancePercent
A porcentagem máxima de instâncias da máquina virtual atualizadas que podem ser encontradas em um estado não íntegro.
Essa verificação ocorrerá após a atualização de cada lote.
Se essa porcentagem já tiver sido excedida, a atualização sem interrupção será anulada.
Se o valor não for especificado, será definido como 20.

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

### -OsDiskCaching
Especifica o modo de cache do disco do sistema operacional. Os valores aceitáveis para esse parâmetro são:

- Nenhuma
- ReadOnly
- Leitura

O valor padrão é ReadWrite.
Se você alterar o valor de cache, o cmdlet reiniciará a máquina virtual.

Essa configuração afeta a consistência e o desempenho do disco.

```yaml
Type: CachingTypes
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
Especifica se o WriteAccelerator deve ser habilitado ou desabilitado no disco do sistema operacional.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Superprovisionamento
Indica se o cmdlet está supervisionando o VMSS.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PauseTimeBetweenBatches
O tempo de espera entre concluir a atualização de todas as máquinas virtuais em um lote e iniciar o próximo lote.
A duração do tempo deve ser especificada no formato ISO 8601.
O valor padrão é 0 segundos (PT0S).

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

### -PlanName
Especifica o nome do plano.

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

### -PlanProduct
Especifica o produto do plano.

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

### -PlanPromotionCode
Especifica o código promocional do plano.

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

### -PlanPublisher
Especifica o fornecedor do plano.

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

### -ProvisionVMAgent
Indica se o agente da máquina virtual deve ser provisionado nas máquinas virtuais do Windows no VMSS.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome do grupo de recursos ao qual o VMSS pertence.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SinglePlacementGroup
Especifica o grupo de posicionamento único.

```yaml
Type: Boolean
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
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkuName
Especifica o tamanho de todas as instâncias de VMSS.

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

### -SkuTier
Especifica o nível de VMSS.
Os valores aceitáveis para esse parâmetro são:

- Oficial
- Basic

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

### -Marca
Pares de valores chave na forma de uma tabela de hash. Por exemplo:

@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Fuso horário
Especifica o fuso horário para o sistema operacional Windows.

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

### -UpgradePolicyMode
Especificou o modo de uma atualização para máquinas virtuais no conjunto de escala.
Os valores aceitáveis para esse parâmetro são:

- Automático
- Manual
- Implantação

```yaml
Type: UpgradeMode
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
Especifica as URLs de contêiner usadas para armazenar discos do sistema operacional para o VMSS.

```yaml
Type: String[]
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
Para obter um objeto VMSS, use o cmdlet Get-AzureRmVmss.
Esse objeto da máquina virtual contém o estado atualizado para o VMSS.

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VMScaleSetName
Especifica o nome do VMSS que este cmdlet cria.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirme
Solicita confirmação antes de executar o cmdlet.

```yaml
Type: SwitchParameter
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### VirtualMachineScaleSet
O parâmetro ' VirtualMachineScaleSet ' aceita o valor do tipo ' VirtualMachineScaleSet ' do pipeline

## EXIBE

### Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmVmss](./Get-AzureRmVmss.md)

[New-AzureRmVmss](./New-AzureRmVmss.md)

[Remove-AzureRmVmss](./Remove-AzureRmVmss.md)

[Restart-AzureRmVmss](./Restart-AzureRmVmss.md)

[Set-AzureRmVmss](./Set-AzureRmVmss.md)

[Start-AzureRmVmss](./Start-AzureRmVmss.md)

[Parar-AzureRmVmss](./Stop-AzureRmVmss.md)


