---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
ms.openlocfilehash: 4b262b219c479cc2c56311c54d41eb05e2eb866d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116504"
---
# <span data-ttu-id="fad35-101">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fad35-101">Update-AzVmss</span></span>

## <span data-ttu-id="fad35-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fad35-102">SYNOPSIS</span></span>
<span data-ttu-id="fad35-103">Atualiza o estado de um VMSS.</span><span class="sxs-lookup"><span data-stu-id="fad35-103">Updates the state of a VMSS.</span></span>

## <span data-ttu-id="fad35-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fad35-104">SYNTAX</span></span>

### <span data-ttu-id="fad35-105">DefaultParameter (Padrão)</span><span class="sxs-lookup"><span data-stu-id="fad35-105">DefaultParameter (Default)</span></span>
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

### <span data-ttu-id="fad35-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="fad35-106">ExplicitIdentityParameterSet</span></span>
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

## <span data-ttu-id="fad35-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="fad35-107">DESCRIPTION</span></span>
<span data-ttu-id="fad35-108">O cmdlet **Update-AzVmss** atualiza o estado de um VMSS (Virtual Machine Scale Set) para o estado de um objeto VMSS local.</span><span class="sxs-lookup"><span data-stu-id="fad35-108">The **Update-AzVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="fad35-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fad35-109">EXAMPLES</span></span>

### <span data-ttu-id="fad35-110">Exemplo 1: Atualizar o estado de um VMSS para o estado de um objeto VMSS local.</span><span class="sxs-lookup"><span data-stu-id="fad35-110">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

<span data-ttu-id="fad35-111">Este comando atualiza o estado do VMSS chamado VMSS01 que pertence ao grupo de recursos chamado Group001 ao estado de um objeto VMSS local, $LocalVMSS.</span><span class="sxs-lookup"><span data-stu-id="fad35-111">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object, $LocalVMSS.</span></span>

## <span data-ttu-id="fad35-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fad35-112">PARAMETERS</span></span>

### <span data-ttu-id="fad35-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fad35-113">-AsJob</span></span>
<span data-ttu-id="fad35-114">Execute o cmdlet em segundo plano e retorne um Trabalho para controlar o andamento.</span><span class="sxs-lookup"><span data-stu-id="fad35-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="fad35-115">-AutomaticOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="fad35-115">-AutomaticOSUpgrade</span></span>
<span data-ttu-id="fad35-116">Define se as atualizações do sistema operacional devem ser aplicadas automaticamente às instâncias de conjunto de escalas de forma rolando quando uma versão mais recente da imagem estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="fad35-116">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="fad35-117">-AutomaticRepairGracePeriod</span><span class="sxs-lookup"><span data-stu-id="fad35-117">-AutomaticRepairGracePeriod</span></span>
<span data-ttu-id="fad35-118">O tempo para o qual os reparos automáticos são suspensos devido a uma alteração de estado no VM.</span><span class="sxs-lookup"><span data-stu-id="fad35-118">The amount of time for which automatic repairs are suspended due to a state change on VM.</span></span> <span data-ttu-id="fad35-119">O período de carência começa após a conclusão da alteração do estado.</span><span class="sxs-lookup"><span data-stu-id="fad35-119">The grace time starts after the state change has completed.</span></span> <span data-ttu-id="fad35-120">Isso ajuda a evitar reparos acidental ou acidental.</span><span class="sxs-lookup"><span data-stu-id="fad35-120">This helps avoid premature or accidental repairs.</span></span> <span data-ttu-id="fad35-121">A duração do tempo deve ser especificada no formato ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="fad35-121">The time duration should be specified in ISO 8601 format.</span></span> <span data-ttu-id="fad35-122">O período mínimo permitido de carência é de 30 minutos (PT30M), que também é o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="fad35-122">The minimum allowed grace period is 30 minutes (PT30M), which is also the default value.</span></span> <span data-ttu-id="fad35-123">O período máximo permitido de carência é de 90 minutos (PT90M).</span><span class="sxs-lookup"><span data-stu-id="fad35-123">The maximum allowed grace period is 90 minutes (PT90M).</span></span>

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

### <span data-ttu-id="fad35-124">-BootDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="fad35-124">-BootDiagnosticsEnabled</span></span>
<span data-ttu-id="fad35-125">Se o diagnóstico de inicialização deve ser habilitado no conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="fad35-125">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="fad35-126">-BootDiagnosticsStorageUri</span><span class="sxs-lookup"><span data-stu-id="fad35-126">-BootDiagnosticsStorageUri</span></span>
<span data-ttu-id="fad35-127">URI da conta de armazenamento a ser usada para colocar a saída do console e a captura de tela.</span><span class="sxs-lookup"><span data-stu-id="fad35-127">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="fad35-128">-CustomData</span><span class="sxs-lookup"><span data-stu-id="fad35-128">-CustomData</span></span>
<span data-ttu-id="fad35-129">Especifica uma cadeia de caracteres codificada de base 64 de dados personalizados.</span><span class="sxs-lookup"><span data-stu-id="fad35-129">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="fad35-130">Isso é decodificado para uma matriz binária que é salva como um arquivo na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="fad35-130">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="fad35-131">O comprimento máximo da matriz binária é de 65535 bytes.</span><span class="sxs-lookup"><span data-stu-id="fad35-131">The maximum length of the binary array is 65535 bytes.</span></span> <br>
<span data-ttu-id="fad35-132">Para usar o cloud-init para seu VM, consulte [Usando o cloud-init para personalizar um VM do Linux durante a criação.](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)</span><span class="sxs-lookup"><span data-stu-id="fad35-132">For using cloud-init for your VM, see [Using cloud-init to customize a Linux VM during creation](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span></span>

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

### <span data-ttu-id="fad35-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fad35-133">-DefaultProfile</span></span>
<span data-ttu-id="fad35-134">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="fad35-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fad35-135">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="fad35-135">-DisableAutoRollback</span></span>
<span data-ttu-id="fad35-136">Desabilitar a Reação Automática para a Política de Atualização do Sistema Operacional Automático</span><span class="sxs-lookup"><span data-stu-id="fad35-136">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="fad35-137">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="fad35-137">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="fad35-138">Indica que esse cmdlet desabilita a autenticação de senha para o sistema operacional Linux.</span><span class="sxs-lookup"><span data-stu-id="fad35-138">Indicates that this cmdlet disables password authentication for Linux OS.</span></span>

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

### <span data-ttu-id="fad35-139">-EnableAutomaticRepair</span><span class="sxs-lookup"><span data-stu-id="fad35-139">-EnableAutomaticRepair</span></span>
<span data-ttu-id="fad35-140">Habilitar ou desabilitar reparos automáticos no conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="fad35-140">Enable or disable automatic repairs on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="fad35-141">-EnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="fad35-141">-EnableAutomaticUpdate</span></span>
<span data-ttu-id="fad35-142">Indica se as máquinas virtuais do Windows no VMSS estão habilitadas para atualizações automáticas.</span><span class="sxs-lookup"><span data-stu-id="fad35-142">Indicates whether the Windows virtual machines in the VMSS are enabled for automatic updates.</span></span>

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

### <span data-ttu-id="fad35-143">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="fad35-143">-EncryptionAtHost</span></span>
<span data-ttu-id="fad35-144">Esse parâmetro pode ser usado pelo usuário na solicitação para habilitar ou desabilitar a Criptografia de Host para o conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="fad35-144">This parameter can be used by user in the request to enable or disable the Host Encryption for the virtual machine scale set.</span></span> 

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

### <span data-ttu-id="fad35-145">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="fad35-145">-IdentityId</span></span>
<span data-ttu-id="fad35-146">Especifica a lista de identidades de usuário associadas ao conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="fad35-146">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="fad35-147">As referências de identidade do usuário serão IDs de recurso ARM no formulário: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span><span class="sxs-lookup"><span data-stu-id="fad35-147">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="fad35-148">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="fad35-148">-IdentityType</span></span>
<span data-ttu-id="fad35-149">Especifica o tipo de identidade usado para o conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="fad35-149">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="fad35-150">O tipo "SystemAssignedUserAssigned" inclui uma identidade criada implicitamente e um conjunto de identidades atribuídas pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="fad35-150">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="fad35-151">O tipo "Nenhum" removerá as identidades do conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="fad35-151">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="fad35-152">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="fad35-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fad35-153">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="fad35-153">SystemAssigned</span></span>
- <span data-ttu-id="fad35-154">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="fad35-154">UserAssigned</span></span>
- <span data-ttu-id="fad35-155">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="fad35-155">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="fad35-156">Nenhum</span><span class="sxs-lookup"><span data-stu-id="fad35-156">None</span></span>

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

### <span data-ttu-id="fad35-157">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="fad35-157">-ImageReferenceId</span></span>
<span data-ttu-id="fad35-158">Especifica a ID de referência de imagem.</span><span class="sxs-lookup"><span data-stu-id="fad35-158">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="fad35-159">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="fad35-159">-ImageReferenceOffer</span></span>
<span data-ttu-id="fad35-160">Especifica o tipo de oferta de imagem de máquina virtual (VMImage).</span><span class="sxs-lookup"><span data-stu-id="fad35-160">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="fad35-161">Para obter uma oferta de imagem, use o cmdlet Get-AzVMImageOffer imagem.</span><span class="sxs-lookup"><span data-stu-id="fad35-161">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="fad35-162">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="fad35-162">-ImageReferencePublisher</span></span>
<span data-ttu-id="fad35-163">Especifica o nome de um editor de uma VMImage.</span><span class="sxs-lookup"><span data-stu-id="fad35-163">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="fad35-164">Para obter um editor, use o Get-AzVMImagePublisher cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fad35-164">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="fad35-165">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="fad35-165">-ImageReferenceSku</span></span>
<span data-ttu-id="fad35-166">Especifica a SKU do VMImage.</span><span class="sxs-lookup"><span data-stu-id="fad35-166">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="fad35-167">Para obter SKUs, use o cmdlet Get-AzVMImageSku dados.</span><span class="sxs-lookup"><span data-stu-id="fad35-167">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="fad35-168">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="fad35-168">-ImageReferenceVersion</span></span>
<span data-ttu-id="fad35-169">Especifica a versão do VMImage.</span><span class="sxs-lookup"><span data-stu-id="fad35-169">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="fad35-170">Para usar a versão mais recente, especifique um valor mais recente em vez de uma versão específica.</span><span class="sxs-lookup"><span data-stu-id="fad35-170">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="fad35-171">-ImageUri</span><span class="sxs-lookup"><span data-stu-id="fad35-171">-ImageUri</span></span>
<span data-ttu-id="fad35-172">Especifica o URI de blob para a imagem do usuário.</span><span class="sxs-lookup"><span data-stu-id="fad35-172">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="fad35-173">O VMSS cria um disco do sistema operacional no mesmo contêiner da imagem do usuário.</span><span class="sxs-lookup"><span data-stu-id="fad35-173">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="fad35-174">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="fad35-174">-LicenseType</span></span>
<span data-ttu-id="fad35-175">Especifique o tipo de licença, que é para trazer seu próprio cenário de licença.</span><span class="sxs-lookup"><span data-stu-id="fad35-175">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="fad35-176">-ManagedDiskStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="fad35-176">-ManagedDiskStorageAccountType</span></span>
<span data-ttu-id="fad35-177">Especifica o tipo de conta de armazenamento do disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="fad35-177">Specifies the storage account type for managed disk.</span></span>
<span data-ttu-id="fad35-178">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="fad35-178">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fad35-179">StandardLRS</span><span class="sxs-lookup"><span data-stu-id="fad35-179">StandardLRS</span></span>
- <span data-ttu-id="fad35-180">PremiumLRS</span><span class="sxs-lookup"><span data-stu-id="fad35-180">PremiumLRS</span></span>

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

### <span data-ttu-id="fad35-181">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="fad35-181">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="fad35-182">A porcentagem máxima do total de instâncias de máquina virtual que serão atualizadas simultaneamente pela atualização em um lote.</span><span class="sxs-lookup"><span data-stu-id="fad35-182">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="fad35-183">Como esse é um máximo, instâncias não saudáveis em lotes anteriores ou futuros podem fazer com que a porcentagem de instâncias em um lote diminua para garantir maior confiabilidade.</span><span class="sxs-lookup"><span data-stu-id="fad35-183">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="fad35-184">Se o valor não for especificado, ele será definido como 20.</span><span class="sxs-lookup"><span data-stu-id="fad35-184">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="fad35-185">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="fad35-185">-MaxPrice</span></span>
<span data-ttu-id="fad35-186">Especifica o preço máximo que você está disposto a pagar por um VM/VMSS de baixa prioridade.</span><span class="sxs-lookup"><span data-stu-id="fad35-186">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="fad35-187">Este preço está em dólares americanos.</span><span class="sxs-lookup"><span data-stu-id="fad35-187">This price is in US Dollars.</span></span> <span data-ttu-id="fad35-188">Esse preço será comparado com o preço atual de baixa prioridade para o tamanho de VM.</span><span class="sxs-lookup"><span data-stu-id="fad35-188">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="fad35-189">Além disso, os preços são comparados no momento da criação/atualização de VM/VMSS de baixa prioridade e a operação só será bem-sucedida se o preço máximo for maior do que o preço de baixa prioridade atual.</span><span class="sxs-lookup"><span data-stu-id="fad35-189">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="fad35-190">O maxPrice também será usado para desapropriar um VM/VMSS de baixa prioridade se o preço atual de baixa prioridade ultrapassar o máximoPrice após a criação de VM/VMSS.</span><span class="sxs-lookup"><span data-stu-id="fad35-190">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="fad35-191">Os valores possíveis são: qualquer valor decimal maior que zero.</span><span class="sxs-lookup"><span data-stu-id="fad35-191">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="fad35-192">Exemplo: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="fad35-192">Example: 0.01538.</span></span>  <span data-ttu-id="fad35-193">-1 indica que o VM/VMSS de baixa prioridade não deve ser despejado por motivos de preço.</span><span class="sxs-lookup"><span data-stu-id="fad35-193">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="fad35-194">Além disso, o preço máximo padrão será -1 se ele não for fornecido por você.</span><span class="sxs-lookup"><span data-stu-id="fad35-194">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="fad35-195">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="fad35-195">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="fad35-196">A porcentagem máxima do total de instâncias de máquina virtual no conjunto de escalas que pode ser simultaneamente não saudável, seja como resultado da atualização, ou por ser encontrada em um estado insalubre pela saúde da máquina virtual verifica antes que a atualização em implantação seja cancelada.</span><span class="sxs-lookup"><span data-stu-id="fad35-196">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="fad35-197">Essa restrição será verificada antes de iniciar qualquer lote.</span><span class="sxs-lookup"><span data-stu-id="fad35-197">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="fad35-198">Se o valor não for especificado, ele será definido como 20.</span><span class="sxs-lookup"><span data-stu-id="fad35-198">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="fad35-199">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="fad35-199">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="fad35-200">A porcentagem máxima de instâncias de máquina virtual atualizadas que podem ser encontradas em um estado não saudável.</span><span class="sxs-lookup"><span data-stu-id="fad35-200">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="fad35-201">Essa verificação acontecerá depois que cada lote for atualizado.</span><span class="sxs-lookup"><span data-stu-id="fad35-201">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="fad35-202">Se essa porcentagem for excedida, a atualização em circulação será cancelada.</span><span class="sxs-lookup"><span data-stu-id="fad35-202">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="fad35-203">Se o valor não for especificado, ele será definido como 20.</span><span class="sxs-lookup"><span data-stu-id="fad35-203">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="fad35-204">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="fad35-204">-OsDiskCaching</span></span>
<span data-ttu-id="fad35-205">Especifica o modo de cache do disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="fad35-205">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="fad35-206">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="fad35-206">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fad35-207">Nenhum</span><span class="sxs-lookup"><span data-stu-id="fad35-207">None</span></span>
- <span data-ttu-id="fad35-208">Readonly</span><span class="sxs-lookup"><span data-stu-id="fad35-208">ReadOnly</span></span>
- <span data-ttu-id="fad35-209">ReadWrite O valor padrão é ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="fad35-209">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="fad35-210">Se você alterar o valor de cache, o cmdlet reiniciará a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="fad35-210">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="fad35-211">Essa configuração afeta a consistência e o desempenho do disco.</span><span class="sxs-lookup"><span data-stu-id="fad35-211">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="fad35-212">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="fad35-212">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="fad35-213">Especifica se o WriteAccelerator deve estar habilitado ou desabilitado no disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="fad35-213">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="fad35-214">-Overprovision</span><span class="sxs-lookup"><span data-stu-id="fad35-214">-Overprovision</span></span>
<span data-ttu-id="fad35-215">Indica se o cmdlet sobreprovisiona o VMSS.</span><span class="sxs-lookup"><span data-stu-id="fad35-215">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="fad35-216">-PauseTimeBetweenBat along</span><span class="sxs-lookup"><span data-stu-id="fad35-216">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="fad35-217">O tempo de espera entre concluir a atualização para todas as máquinas virtuais em um lote e iniciar o próximo lote.</span><span class="sxs-lookup"><span data-stu-id="fad35-217">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="fad35-218">A duração do tempo deve ser especificada no formato ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="fad35-218">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="fad35-219">O valor padrão é 0 segundos (PT0S).</span><span class="sxs-lookup"><span data-stu-id="fad35-219">The default value is 0 seconds (PT0S).</span></span>

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

### <span data-ttu-id="fad35-220">-PlanName</span><span class="sxs-lookup"><span data-stu-id="fad35-220">-PlanName</span></span>
<span data-ttu-id="fad35-221">Especifica o nome do plano.</span><span class="sxs-lookup"><span data-stu-id="fad35-221">Specifies the plan name.</span></span>

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

### <span data-ttu-id="fad35-222">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="fad35-222">-PlanProduct</span></span>
<span data-ttu-id="fad35-223">Especifica o produto do plano.</span><span class="sxs-lookup"><span data-stu-id="fad35-223">Specifies the plan product.</span></span>

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

### <span data-ttu-id="fad35-224">-PlanProcode</span><span class="sxs-lookup"><span data-stu-id="fad35-224">-PlanPromotionCode</span></span>
<span data-ttu-id="fad35-225">Especifica o código de promoção do plano.</span><span class="sxs-lookup"><span data-stu-id="fad35-225">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="fad35-226">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="fad35-226">-PlanPublisher</span></span>
<span data-ttu-id="fad35-227">Especifica o editor do plano.</span><span class="sxs-lookup"><span data-stu-id="fad35-227">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="fad35-228">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="fad35-228">-ProvisionVMAgent</span></span>
<span data-ttu-id="fad35-229">Indica se o agente de máquina virtual deve ser provisionado nas máquinas virtuais do Windows no VMSS.</span><span class="sxs-lookup"><span data-stu-id="fad35-229">Indicates whether virtual machine agent should be provisioned on the Windows virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="fad35-230">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="fad35-230">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="fad35-231">A ID do recurso do Grupo de Posicionamento de Proximidade a ser usado com esse conjunto de escalas.</span><span class="sxs-lookup"><span data-stu-id="fad35-231">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

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

### <span data-ttu-id="fad35-232">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fad35-232">-ResourceGroupName</span></span>
<span data-ttu-id="fad35-233">Especifica o nome do grupo de recursos ao que o VMSS pertence.</span><span class="sxs-lookup"><span data-stu-id="fad35-233">Specifies the name of the resource group the VMSS belongs to.</span></span>

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

### <span data-ttu-id="fad35-234">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="fad35-234">-ScaleInPolicy</span></span>
<span data-ttu-id="fad35-235">As regras a serem seguidas ao dimensionar um conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="fad35-235">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="fad35-236">Os valores possíveis são: 'Padrão', 'OldestVM' e 'NewestVM'.</span><span class="sxs-lookup"><span data-stu-id="fad35-236">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="fad35-237">"Padrão" quando um conjunto de escalas de máquina virtual é dimensionado, o conjunto de escalas primeiro será equilibrado entre zonas se for um conjunto de escalas zonais.</span><span class="sxs-lookup"><span data-stu-id="fad35-237">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="fad35-238">Em seguida, ele será equilibrado em todos os Domínios de Falha o mais longe possível.</span><span class="sxs-lookup"><span data-stu-id="fad35-238">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="fad35-239">Em cada Domínio de Falha, as máquinas virtuais escolhidas para remoção serão as mais novas que não estão protegidas da escala.</span><span class="sxs-lookup"><span data-stu-id="fad35-239">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="fad35-240">'OldestVM' quando um conjunto de escalas de máquina virtual está sendo dimensionado, as máquinas virtuais mais antigas que não estão protegidas contra escalas serão escolhidas para remoção.</span><span class="sxs-lookup"><span data-stu-id="fad35-240">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="fad35-241">Para conjuntos de escala de computador virtual zonal, o conjunto de escalas será primeiro equilibrado entre zonas.</span><span class="sxs-lookup"><span data-stu-id="fad35-241">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="fad35-242">Em cada zona, as máquinas virtuais mais antigas que não estão protegidas serão escolhidas para remoção.</span><span class="sxs-lookup"><span data-stu-id="fad35-242">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="fad35-243">'NewestVM' quando um conjunto de escalas de máquina virtual estiver sendo dimensionado, as máquinas virtuais mais novas que não estão protegidas contra escalas serão escolhidas para remoção.</span><span class="sxs-lookup"><span data-stu-id="fad35-243">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="fad35-244">Para conjuntos de escala de computador virtual zonal, o conjunto de escalas será primeiro equilibrado entre zonas.</span><span class="sxs-lookup"><span data-stu-id="fad35-244">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="fad35-245">Em cada zona, as máquinas virtuais mais novas que não estão protegidas serão escolhidas para remoção.</span><span class="sxs-lookup"><span data-stu-id="fad35-245">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

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

### <span data-ttu-id="fad35-246">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="fad35-246">-SinglePlacementGroup</span></span>
<span data-ttu-id="fad35-247">Especifica o único grupo de posicionamento.</span><span class="sxs-lookup"><span data-stu-id="fad35-247">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="fad35-248">-SkipExtensionsOnOverprovisionedVMs</span><span class="sxs-lookup"><span data-stu-id="fad35-248">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="fad35-249">Especifica que as extensões não são executados em VMs extra sobreprovisionadas.</span><span class="sxs-lookup"><span data-stu-id="fad35-249">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

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

### <span data-ttu-id="fad35-250">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="fad35-250">-SkuCapacity</span></span>
<span data-ttu-id="fad35-251">Especifica o número de instâncias no VMSS.</span><span class="sxs-lookup"><span data-stu-id="fad35-251">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="fad35-252">-SkuName</span><span class="sxs-lookup"><span data-stu-id="fad35-252">-SkuName</span></span>
<span data-ttu-id="fad35-253">Especifica o tamanho de todas as instâncias do VMSS.</span><span class="sxs-lookup"><span data-stu-id="fad35-253">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="fad35-254">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="fad35-254">-SkuTier</span></span>
<span data-ttu-id="fad35-255">Especifica o nível de VMSS.</span><span class="sxs-lookup"><span data-stu-id="fad35-255">Specifies the tier of VMSS.</span></span>
<span data-ttu-id="fad35-256">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="fad35-256">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fad35-257">Padrão</span><span class="sxs-lookup"><span data-stu-id="fad35-257">Standard</span></span>
- <span data-ttu-id="fad35-258">Basic</span><span class="sxs-lookup"><span data-stu-id="fad35-258">Basic</span></span>

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

### <span data-ttu-id="fad35-259">-Tag</span><span class="sxs-lookup"><span data-stu-id="fad35-259">-Tag</span></span>
<span data-ttu-id="fad35-260">Pares de valor-chave na forma de uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="fad35-260">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="fad35-261">Por exemplo: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="fad35-261">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="fad35-262">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="fad35-262">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span></span>
<span data-ttu-id="fad35-263">Duração configurável (em minutos) que uma Máquina Virtual seja excluída terá que aprovar potencialmente o Evento Agendado para que o evento seja aprovado automaticamente (com tempo de tempo).</span><span class="sxs-lookup"><span data-stu-id="fad35-263">Configurable length of time (in minutes) a Virtual Machine being deleted will have to potentially approve the Terminate Scheduled Event before the event is auto approved (timed out).</span></span>

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

### <span data-ttu-id="fad35-264">-TerminateScheduledEvents</span><span class="sxs-lookup"><span data-stu-id="fad35-264">-TerminateScheduledEvents</span></span>
<span data-ttu-id="fad35-265">Especifica se o evento Encerrar Agendado está habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="fad35-265">Specifies whether the Terminate Scheduled event is enabled or disabled.</span></span>

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

### <span data-ttu-id="fad35-266">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="fad35-266">-TimeZone</span></span>
<span data-ttu-id="fad35-267">Especifica o fuso horário do sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="fad35-267">Specifies the time zone for Windows OS.</span></span> <span data-ttu-id="fad35-268">por exemplo, Hora \" Padrão do \" Pacífico.</span><span class="sxs-lookup"><span data-stu-id="fad35-268">e.g. \"Pacific Standard Time\".</span></span> <br>
<span data-ttu-id="fad35-269">Os valores possíveis podem [TimeZoneInfo.Id](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) de fusos horário retornados pelo [TimeZoneInfo.GetSystemTimeZones.](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones)</span><span class="sxs-lookup"><span data-stu-id="fad35-269">Possible values can be [TimeZoneInfo.Id](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) value from time zones returned by [TimeZoneInfo.GetSystemTimeZones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones).</span></span>

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

### <span data-ttu-id="fad35-270">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="fad35-270">-UltraSSDEnabled</span></span>
<span data-ttu-id="fad35-271">O sinalizador que habilita ou desabilita um recurso de ter um ou mais discos de dados gerenciados com UltraSSD_LRS de armazenamento no conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="fad35-271">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="fad35-272">Os discos gerenciados com tipo de conta de armazenamento UltraSSD_LRS podem ser adicionados a um VMSS somente se essa propriedade estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="fad35-272">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="fad35-273">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="fad35-273">-UpgradePolicyMode</span></span>
<span data-ttu-id="fad35-274">Especificou o modo de uma atualização para máquinas virtuais no conjunto de escalas.</span><span class="sxs-lookup"><span data-stu-id="fad35-274">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="fad35-275">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="fad35-275">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fad35-276">Automático</span><span class="sxs-lookup"><span data-stu-id="fad35-276">Automatic</span></span>
- <span data-ttu-id="fad35-277">Manual</span><span class="sxs-lookup"><span data-stu-id="fad35-277">Manual</span></span>
- <span data-ttu-id="fad35-278">Rolando</span><span class="sxs-lookup"><span data-stu-id="fad35-278">Rolling</span></span>

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

### <span data-ttu-id="fad35-279">-HighdContainer</span><span class="sxs-lookup"><span data-stu-id="fad35-279">-VhdContainer</span></span>
<span data-ttu-id="fad35-280">Especifica as URLs de contêiner que são usadas para armazenar discos do sistema operacional para o VMSS.</span><span class="sxs-lookup"><span data-stu-id="fad35-280">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

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

### <span data-ttu-id="fad35-281">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="fad35-281">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="fad35-282">Especifica um objeto VMSS local.</span><span class="sxs-lookup"><span data-stu-id="fad35-282">Specifies a local VMSS object.</span></span>
<span data-ttu-id="fad35-283">Para obter um objeto VMSS, use Get-AzVmss cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fad35-283">To obtain a VMSS object, use the Get-AzVmss cmdlet.</span></span>
<span data-ttu-id="fad35-284">Este objeto virtual de máquina contém o estado atualizado para o VMSS.</span><span class="sxs-lookup"><span data-stu-id="fad35-284">This virtual machine object contains the updated state for the VMSS.</span></span>

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

### <span data-ttu-id="fad35-285">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="fad35-285">-VMScaleSetName</span></span>
<span data-ttu-id="fad35-286">Especifica o nome do VMSS que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="fad35-286">Specifies the name of the VMSS that this cmdlet creates.</span></span>

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

### <span data-ttu-id="fad35-287">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="fad35-287">-Confirm</span></span>
<span data-ttu-id="fad35-288">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fad35-288">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fad35-289">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fad35-289">-WhatIf</span></span>
<span data-ttu-id="fad35-290">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="fad35-290">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fad35-291">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fad35-291">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fad35-292">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fad35-292">CommonParameters</span></span>
<span data-ttu-id="fad35-293">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fad35-293">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fad35-294">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fad35-294">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fad35-295">Entradas</span><span class="sxs-lookup"><span data-stu-id="fad35-295">INPUTS</span></span>

### <span data-ttu-id="fad35-296">System.String</span><span class="sxs-lookup"><span data-stu-id="fad35-296">System.String</span></span>

### <span data-ttu-id="fad35-297">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="fad35-297">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="fad35-298">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fad35-298">System.Boolean</span></span>

## <span data-ttu-id="fad35-299">Saídas</span><span class="sxs-lookup"><span data-stu-id="fad35-299">OUTPUTS</span></span>

### <span data-ttu-id="fad35-300">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="fad35-300">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="fad35-301">Notas</span><span class="sxs-lookup"><span data-stu-id="fad35-301">NOTES</span></span>

## <span data-ttu-id="fad35-302">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fad35-302">RELATED LINKS</span></span>

[<span data-ttu-id="fad35-303">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fad35-303">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="fad35-304">Novos AzVmss</span><span class="sxs-lookup"><span data-stu-id="fad35-304">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="fad35-305">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fad35-305">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="fad35-306">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fad35-306">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="fad35-307">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fad35-307">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="fad35-308">Iniciar-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fad35-308">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="fad35-309">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fad35-309">Stop-AzVmss</span></span>](./Stop-AzVmss.md)


