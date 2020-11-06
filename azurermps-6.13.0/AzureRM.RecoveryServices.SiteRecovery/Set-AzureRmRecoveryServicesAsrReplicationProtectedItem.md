---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/set-azurermrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: d387774ebf5f269474df959de981568141f90fbe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428395"
---
# <span data-ttu-id="5ab61-101">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="5ab61-101">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="5ab61-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5ab61-102">SYNOPSIS</span></span>
<span data-ttu-id="5ab61-103">Define propriedades de recuperação, como a rede de destino e o tamanho da máquina virtual para o item protegido de replicação especificado.</span><span class="sxs-lookup"><span data-stu-id="5ab61-103">Sets recovery properties such as target network and virtual machine size for the specified replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ab61-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5ab61-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem>
 [-Name <String>] [-Size <String>] [-PrimaryNic <String>] [-RecoveryNetworkId <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryNicSubnetName <String>] [-RecoveryNicStaticIPAddress <String>]
 [-NicSelectionType <String>] [-RecoveryResourceGroupId <String>] [-LicenseType <String>]
 [-RecoveryAvailabilitySet <String>] [-RecoveryBootDiagStorageAccountId <String>]
 [-AzureToAzureUpdateReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]>]
 [-UseManagedDisk <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5ab61-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5ab61-105">DESCRIPTION</span></span>
<span data-ttu-id="5ab61-106">O cmdlet **set-AzureRmRecoveryServicesAsrReplicationProtectedItem** define as propriedades de recuperação para um item protegido de replicação.</span><span class="sxs-lookup"><span data-stu-id="5ab61-106">The **Set-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet sets the recovery properties for a Replication Protected Item.</span></span>

## <span data-ttu-id="5ab61-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5ab61-107">EXAMPLES</span></span>

### <span data-ttu-id="5ab61-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5ab61-108">Example 1</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $RPI -PrimaryNic $NicId -RecoveryNetworkId $AzureNetworkID -RecoveryNicSubnetName $subnetName
```

<span data-ttu-id="5ab61-109">Inicia a operação de atualização das configurações de item de proteção de replicação usando os parâmetros especificados e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="5ab61-109">Starts the operation of updating the replication protect item settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="5ab61-110">OS</span><span class="sxs-lookup"><span data-stu-id="5ab61-110">PARAMETERS</span></span>

### <span data-ttu-id="5ab61-111">-AzureToAzureUpdateReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="5ab61-111">-AzureToAzureUpdateReplicationConfiguration</span></span>
<span data-ttu-id="5ab61-112">Especifica a relication de atualização de atualização.</span><span class="sxs-lookup"><span data-stu-id="5ab61-112">Specifies the update relication configration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ab61-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ab61-113">-DefaultProfile</span></span>
<span data-ttu-id="5ab61-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5ab61-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ab61-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5ab61-115">-InputObject</span></span>
<span data-ttu-id="5ab61-116">O objeto de entrada para o cmdlet: o objeto de item protegido da replicação ASR correspondente ao item de replicação protegida a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="5ab61-116">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ab61-117">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="5ab61-117">-LicenseType</span></span>
<span data-ttu-id="5ab61-118">Especifique a seleção do tipo de licença a ser usada para máquinas virtuais do Windows Server.</span><span class="sxs-lookup"><span data-stu-id="5ab61-118">Specifiy the license type selection to be used for Windows Server virtual machines.</span></span> <span data-ttu-id="5ab61-119">Se você tem o direito de usar o centro de uso híbrido do Azure (HUB) para migrações e gostaria de especificar que a configuração do HUB seja usada durante a falha desse item protegido, defina o tipo de licença como WindowsServer.</span><span class="sxs-lookup"><span data-stu-id="5ab61-119">If you are entitled to use the Azure Hybrid Use Benefit (HUB) for migrations and would like to specify that the HUB setting be used while failing over this protected item set the license type to be WindowsServer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NoLicenseType, WindowsServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ab61-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="5ab61-120">-Name</span></span>
<span data-ttu-id="5ab61-121">Especifica o nome da máquina virtual de recuperação que será criada no failover.</span><span class="sxs-lookup"><span data-stu-id="5ab61-121">Specifies the name of the recovery virtual machine that will be created on failover.</span></span>

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

### <span data-ttu-id="5ab61-122">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="5ab61-122">-NicSelectionType</span></span>
<span data-ttu-id="5ab61-123">Especifica as propriedades da NIC (placa de interface de rede) definidas por usuário ou definidas por padrão.</span><span class="sxs-lookup"><span data-stu-id="5ab61-123">Specifies the network interface card (NIC) properties set by user or set by default.</span></span>
<span data-ttu-id="5ab61-124">Você pode especificar não selecionado para voltar aos valores padrão.</span><span class="sxs-lookup"><span data-stu-id="5ab61-124">You can specify NotSelected to go back to the default values.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NotSelected, SelectedByUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ab61-125">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="5ab61-125">-PrimaryNic</span></span>
<span data-ttu-id="5ab61-126">Especifica a NIC da máquina virtual para a qual esse cmdlet define a propriedade de rede de recuperação.</span><span class="sxs-lookup"><span data-stu-id="5ab61-126">Specifies the NIC of the virtual machine for which this cmdlet sets the recovery network property.</span></span>

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

### <span data-ttu-id="5ab61-127">-RecoveryAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="5ab61-127">-RecoveryAvailabilitySet</span></span>
<span data-ttu-id="5ab61-128">Conjunto de disponibilidade para o item protegido da replicação após o failover.</span><span class="sxs-lookup"><span data-stu-id="5ab61-128">Availability set for replication protected item after failover.</span></span>

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

### <span data-ttu-id="5ab61-129">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="5ab61-129">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="5ab61-130">Especifica a conta de armazenamento para o diagnóstico de inicialização para a VM de recuperação do Azure.</span><span class="sxs-lookup"><span data-stu-id="5ab61-130">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="5ab61-131">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="5ab61-131">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="5ab61-132">A ID do recurso do serviço de nuvem de recuperação para o qual esta máquina virtual está em failover.</span><span class="sxs-lookup"><span data-stu-id="5ab61-132">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="5ab61-133">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="5ab61-133">-RecoveryNetworkId</span></span>
<span data-ttu-id="5ab61-134">Especifica a ID da rede virtual do Azure para a qual o item protegido deve ter failover.</span><span class="sxs-lookup"><span data-stu-id="5ab61-134">Specifies the ID of the Azure virtual network to which the protected item should be failed over.</span></span>

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

### <span data-ttu-id="5ab61-135">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="5ab61-135">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="5ab61-136">Especifica o endereço IP estático que deve ser atribuído à NIC primária na recuperação.</span><span class="sxs-lookup"><span data-stu-id="5ab61-136">Specifies the static IP address that should be assigned to primary NIC on recovery.</span></span>

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

### <span data-ttu-id="5ab61-137">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="5ab61-137">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="5ab61-138">Especifica o nome da sub-rede na rede virtual do Azure de recuperação à qual essa NIC do item protegido deve estar conectada no failover.</span><span class="sxs-lookup"><span data-stu-id="5ab61-138">Specifies the name of the subnet on the recovery Azure virtual network to which this NIC of the protected item should be connected to on failover.</span></span>

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

### <span data-ttu-id="5ab61-139">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="5ab61-139">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="5ab61-140">A ID do grupo de recursos do Azure na região de recuperação na qual o item protegido será recuperado no failover.</span><span class="sxs-lookup"><span data-stu-id="5ab61-140">The ID of the Azure resource group in the recovery region in which the protected item will be recovered on failover.</span></span>

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

### <span data-ttu-id="5ab61-141">-Tamanho</span><span class="sxs-lookup"><span data-stu-id="5ab61-141">-Size</span></span>
<span data-ttu-id="5ab61-142">Especifica o tamanho da máquina virtual de recuperação.</span><span class="sxs-lookup"><span data-stu-id="5ab61-142">Specifies the recovery virtual machine size.</span></span>
<span data-ttu-id="5ab61-143">O valor deve ser do conjunto de tamanhos com suporte nas máquinas virtuais do Azure.</span><span class="sxs-lookup"><span data-stu-id="5ab61-143">The value should be from the set of sizes supported by Azure virtual machines.</span></span>

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

### <span data-ttu-id="5ab61-144">-UseManagedDisk</span><span class="sxs-lookup"><span data-stu-id="5ab61-144">-UseManagedDisk</span></span>
<span data-ttu-id="5ab61-145">Especifica se a máquina virtual do Azure criada no failover deve usar discos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="5ab61-145">Specifies if the Azure virtual machine that is created on failover should use managed disks.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: True, False

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ab61-146">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5ab61-146">-Confirm</span></span>
<span data-ttu-id="5ab61-147">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ab61-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ab61-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ab61-148">-WhatIf</span></span>
<span data-ttu-id="5ab61-149">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5ab61-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5ab61-150">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5ab61-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ab61-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ab61-151">CommonParameters</span></span>
<span data-ttu-id="5ab61-152">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ab61-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ab61-153">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ab61-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ab61-154">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5ab61-154">INPUTS</span></span>

### <span data-ttu-id="5ab61-155">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="5ab61-155">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="5ab61-156">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5ab61-156">OUTPUTS</span></span>

### <span data-ttu-id="5ab61-157">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="5ab61-157">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="5ab61-158">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5ab61-158">NOTES</span></span>

## <span data-ttu-id="5ab61-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5ab61-159">RELATED LINKS</span></span>

[<span data-ttu-id="5ab61-160">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="5ab61-160">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="5ab61-161">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="5ab61-161">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="5ab61-162">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="5ab61-162">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)