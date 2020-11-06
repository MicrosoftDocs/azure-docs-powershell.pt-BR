---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 5627b94f87d69fab6b760bf05f1e22566992048b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609595"
---
# <span data-ttu-id="5198e-101">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="5198e-101">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="5198e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5198e-102">SYNOPSIS</span></span>
<span data-ttu-id="5198e-103">Define propriedades de recuperação, como a rede de destino e o tamanho da máquina virtual para o item protegido de replicação especificado.</span><span class="sxs-lookup"><span data-stu-id="5198e-103">Sets recovery properties such as target network and virtual machine size for the specified replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5198e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5198e-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem>
 [-Name <String>] [-Size <String>] [-PrimaryNic <String>] [-RecoveryNetworkId <String>]
 [-RecoveryNicSubnetName <String>] [-RecoveryNicStaticIPAddress <String>] [-NicSelectionType <String>]
 [-RecoveryResourceGroupId <String>] [-LicenseType <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5198e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5198e-105">DESCRIPTION</span></span>
<span data-ttu-id="5198e-106">O cmdlet **set-AzureRmRecoveryServicesAsrReplicationProtectedItem** define as propriedades de recuperação para um item protegido de replicação.</span><span class="sxs-lookup"><span data-stu-id="5198e-106">The **Set-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet sets the recovery properties for a Replication Protected Item.</span></span>

## <span data-ttu-id="5198e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5198e-107">EXAMPLES</span></span>

### <span data-ttu-id="5198e-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5198e-108">Example 1</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $RPI -PrimaryNic $NicId -RecoveryNetworkId $AzureNetworkID -RecoveryNicSubnetName $subnetName
```

<span data-ttu-id="5198e-109">Inicia a operação de atualização das configurações de item de proteção de replicação usando os parâmetros especificados e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="5198e-109">Starts the operation of updating the replication protect item settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="5198e-110">OS</span><span class="sxs-lookup"><span data-stu-id="5198e-110">PARAMETERS</span></span>

### <span data-ttu-id="5198e-111">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5198e-111">-InputObject</span></span>
<span data-ttu-id="5198e-112">O objeto de entrada para o cmdlet: o objeto de item protegido da replicação ASR correspondente ao item de replicação protegida a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="5198e-112">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item to update.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5198e-113">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="5198e-113">-LicenseType</span></span>
<span data-ttu-id="5198e-114">Especifique a seleção do tipo de licença a ser usada para máquinas virtuais do Windows Server.</span><span class="sxs-lookup"><span data-stu-id="5198e-114">Specifiy the license type selection to be used for Windows Server virtual machines.</span></span> <span data-ttu-id="5198e-115">Se você tem o direito de usar o centro de uso híbrido do Azure (HUB) para migrações e gostaria de especificar que a configuração do HUB seja usada durante a falha desse item protegido, defina o tipo de licença como WindowsServer.</span><span class="sxs-lookup"><span data-stu-id="5198e-115">If you are entitled to use the Azure Hybrid Use Benefit (HUB) for migrations and would like to specify that the HUB setting be used while failing over this protected item set the license type to be WindowsServer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: NoLicenseType, WindowsServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5198e-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="5198e-116">-Name</span></span>
<span data-ttu-id="5198e-117">Especifica o nome da máquina virtual de recuperação que será criada no failover.</span><span class="sxs-lookup"><span data-stu-id="5198e-117">Specifies the name of the recovery virtual machine that will be created on failover.</span></span>

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

### <span data-ttu-id="5198e-118">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="5198e-118">-NicSelectionType</span></span>
<span data-ttu-id="5198e-119">Especifica as propriedades da NIC (placa de interface de rede) definidas por usuário ou definidas por padrão.</span><span class="sxs-lookup"><span data-stu-id="5198e-119">Specifies the network interface card (NIC) properties set by user or set by default.</span></span>
<span data-ttu-id="5198e-120">Você pode especificar não selecionado para voltar aos valores padrão.</span><span class="sxs-lookup"><span data-stu-id="5198e-120">You can specify NotSelected to go back to the default values.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: NotSelected, SelectedByUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5198e-121">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="5198e-121">-PrimaryNic</span></span>
<span data-ttu-id="5198e-122">Especifica a NIC da máquina virtual para a qual esse cmdlet define a propriedade de rede de recuperação.</span><span class="sxs-lookup"><span data-stu-id="5198e-122">Specifies the NIC of the virtual machine for which this cmdlet sets the recovery network property.</span></span>

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

### <span data-ttu-id="5198e-123">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="5198e-123">-RecoveryNetworkId</span></span>
<span data-ttu-id="5198e-124">Especifica a ID da rede virtual do Azure para a qual o item protegido deve ter failover.</span><span class="sxs-lookup"><span data-stu-id="5198e-124">Specifies the ID of the Azure virtual network to which the protected item should be failed over.</span></span>

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

### <span data-ttu-id="5198e-125">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="5198e-125">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="5198e-126">Especifica o endereço IP estático que deve ser atribuído à NIC primária na recuperação.</span><span class="sxs-lookup"><span data-stu-id="5198e-126">Specifies the static IP address that should be assigned to primary NIC on recovery.</span></span>

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

### <span data-ttu-id="5198e-127">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="5198e-127">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="5198e-128">Especifica o nome da sub-rede na rede virtual do Azure de recuperação à qual essa NIC do item protegido deve estar conectada no failover.</span><span class="sxs-lookup"><span data-stu-id="5198e-128">Specifies the name of the subnet on the recovery Azure virtual network to which this NIC of the protected item should be connected to on failover.</span></span>

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

### <span data-ttu-id="5198e-129">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="5198e-129">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="5198e-130">A ID do grupo de recursos do Azure na região de recuperação na qual o item protegido será recuperado no failover.</span><span class="sxs-lookup"><span data-stu-id="5198e-130">The ID of the Azure resource group in the recovery region in which the protected item will be recovered on failover.</span></span>

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

### <span data-ttu-id="5198e-131">-Tamanho</span><span class="sxs-lookup"><span data-stu-id="5198e-131">-Size</span></span>
<span data-ttu-id="5198e-132">Especifica o tamanho da máquina virtual de recuperação.</span><span class="sxs-lookup"><span data-stu-id="5198e-132">Specifies the recovery virtual machine size.</span></span>
<span data-ttu-id="5198e-133">O valor deve ser do conjunto de tamanhos com suporte nas máquinas virtuais do Azure.</span><span class="sxs-lookup"><span data-stu-id="5198e-133">The value should be from the set of sizes supported by Azure virtual machines.</span></span>

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

### <span data-ttu-id="5198e-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5198e-134">-Confirm</span></span>
<span data-ttu-id="5198e-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5198e-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5198e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5198e-136">-WhatIf</span></span>
<span data-ttu-id="5198e-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5198e-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5198e-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5198e-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5198e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5198e-139">CommonParameters</span></span>
<span data-ttu-id="5198e-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5198e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5198e-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5198e-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5198e-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5198e-142">INPUTS</span></span>

### <span data-ttu-id="5198e-143">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="5198e-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="5198e-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5198e-144">OUTPUTS</span></span>

### <span data-ttu-id="5198e-145">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="5198e-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="5198e-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5198e-146">NOTES</span></span>

## <span data-ttu-id="5198e-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5198e-147">RELATED LINKS</span></span>

[<span data-ttu-id="5198e-148">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="5198e-148">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="5198e-149">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="5198e-149">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="5198e-150">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="5198e-150">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
