---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 38917534-49C6-47EA-B815-240F794EE655
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
ms.openlocfilehash: e9ec68d7c3991d7a3eded2566d8e299ddcc36c85
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434150"
---
# <span data-ttu-id="3b599-101">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="3b599-101">Update-AzVM</span></span>

## <span data-ttu-id="3b599-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3b599-102">SYNOPSIS</span></span>
<span data-ttu-id="3b599-103">Atualiza o estado de uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="3b599-103">Updates the state of an Azure virtual machine.</span></span>

## <span data-ttu-id="3b599-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3b599-104">SYNTAX</span></span>

### <span data-ttu-id="3b599-105">ResourceGroupNameParameterSetName (padrão)</span><span class="sxs-lookup"><span data-stu-id="3b599-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>]
 [-ProximityPlacementGroupId <String>] [-HostId <String>] [-EncryptionAtHost <Boolean>] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b599-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b599-106">ExplicitIdentityParameterSet</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>] [-ProximityPlacementGroupId <String>] [-HostId <String>]
 [-EncryptionAtHost <Boolean>] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b599-107">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="3b599-107">IdParameterSetName</span></span>
```
Update-AzVM [-Id] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>] [-ProximityPlacementGroupId <String>] [-HostId <String>]
 [-EncryptionAtHost <Boolean>] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b599-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3b599-108">DESCRIPTION</span></span>
<span data-ttu-id="3b599-109">O cmdlet **Update-AzVM** atualiza o estado de uma máquina virtual do Azure para o estado de um objeto de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3b599-109">The **Update-AzVM** cmdlet updates the state of an Azure virtual machine to the state of a virtual machine object.</span></span>

## <span data-ttu-id="3b599-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3b599-110">EXAMPLES</span></span>

### <span data-ttu-id="3b599-111">Exemplo 1: atualizar uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="3b599-111">Example 1: Update a virtual machine</span></span>
```
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="3b599-112">Esse comando atualiza a máquina virtual, $VirtualMachine, no ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="3b599-112">This command updates the virtual machine, $VirtualMachine, in ResourceGroup11.</span></span>
<span data-ttu-id="3b599-113">O comando atualiza-o usando o objeto da máquina virtual armazenado na variável $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="3b599-113">The command updates it by using the virtual machine object stored in the $VirtualMachine variable.</span></span>
<span data-ttu-id="3b599-114">Para obter um objeto de máquina virtual, use o cmdlet **Get-AzVM** .</span><span class="sxs-lookup"><span data-stu-id="3b599-114">To obtain a virtual machine object, use the **Get-AzVM** cmdlet.</span></span>

## <span data-ttu-id="3b599-115">OS</span><span class="sxs-lookup"><span data-stu-id="3b599-115">PARAMETERS</span></span>

### <span data-ttu-id="3b599-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3b599-116">-AsJob</span></span>
<span data-ttu-id="3b599-117">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="3b599-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="3b599-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b599-118">-DefaultProfile</span></span>
<span data-ttu-id="3b599-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3b599-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b599-120">-Hostid</span><span class="sxs-lookup"><span data-stu-id="3b599-120">-HostId</span></span>
<span data-ttu-id="3b599-121">A ID do host</span><span class="sxs-lookup"><span data-stu-id="3b599-121">The Id of Host</span></span>

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

### <span data-ttu-id="3b599-122">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="3b599-122">-EncryptionAtHost</span></span>
<span data-ttu-id="3b599-123">A propriedade EncryptionAtHost pode ser usada pelo usuário na solicitação para habilitar ou desabilitar a criptografia do host para a máquina virtual ou o conjunto de escala da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3b599-123">EncryptionAtHost property can be used by user in the request to enable or disable the Host Encryption for the virtual machine or virtual machine scale set.</span></span> <span data-ttu-id="3b599-124">Isso habilitará a criptografia para todos os discos, incluindo o disco de recursos/temporários no próprio host.</span><span class="sxs-lookup"><span data-stu-id="3b599-124">This will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> 

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

### <span data-ttu-id="3b599-125">-ID</span><span class="sxs-lookup"><span data-stu-id="3b599-125">-Id</span></span>
<span data-ttu-id="3b599-126">Especifica a ID do recurso da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3b599-126">Specifies the resource ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b599-127">-Identityid</span><span class="sxs-lookup"><span data-stu-id="3b599-127">-IdentityId</span></span>
<span data-ttu-id="3b599-128">Especifica a lista de identidades de usuário associadas à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3b599-128">Specifies the list of user identities associated with the virtual machine.</span></span>
<span data-ttu-id="3b599-129">As referências de identidade do usuário serão identificadores de recurso ARM no formato: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="3b599-129">The user identity references will be ARM resource IDs in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="3b599-130">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="3b599-130">-IdentityType</span></span>
<span data-ttu-id="3b599-131">O tipo de identidade usado para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3b599-131">The type of identity used for the virtual machine.</span></span> <span data-ttu-id="3b599-132">Os valores válidos são SystemAssigned, userassign, SystemAssignedUserAssigned e None.</span><span class="sxs-lookup"><span data-stu-id="3b599-132">Valid values are SystemAssigned, UserAssigned, SystemAssignedUserAssigned, and None.</span></span>

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

### <span data-ttu-id="3b599-133">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="3b599-133">-MaxPrice</span></span>
<span data-ttu-id="3b599-134">Especifica o preço máximo que você está disposto a pagar por uma VM/VMSS de baixa prioridade.</span><span class="sxs-lookup"><span data-stu-id="3b599-134">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="3b599-135">Este preço está em dólares americanos.</span><span class="sxs-lookup"><span data-stu-id="3b599-135">This price is in US Dollars.</span></span> <span data-ttu-id="3b599-136">Esse preço será comparado com o preço de baixa prioridade atual para o tamanho da VM.</span><span class="sxs-lookup"><span data-stu-id="3b599-136">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="3b599-137">Além disso, os preços são comparados no momento da criação/atualização de VMs/VMSS de baixa prioridade e a operação será bem-sucedida apenas se o maxPrice for maior do que o preço de baixa prioridade atual.</span><span class="sxs-lookup"><span data-stu-id="3b599-137">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="3b599-138">O maxPrice também será usado para remover uma VM/VMSS de baixa prioridade se o preço atual de baixa prioridade vai além do maxPrice após a criação de VM/VMSS.</span><span class="sxs-lookup"><span data-stu-id="3b599-138">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="3b599-139">Os valores possíveis são: qualquer valor decimal maior do que zero.</span><span class="sxs-lookup"><span data-stu-id="3b599-139">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="3b599-140">Exemplo: 0, 1538.</span><span class="sxs-lookup"><span data-stu-id="3b599-140">Example: 0.01538.</span></span>  <span data-ttu-id="3b599-141">-1 indica que a VM de baixa prioridade/VMSS não deve ser removida por motivos de preço.</span><span class="sxs-lookup"><span data-stu-id="3b599-141">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="3b599-142">Além disso, o preço máximo padrão é-1 se não for fornecido por você.</span><span class="sxs-lookup"><span data-stu-id="3b599-142">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="3b599-143">-Nowait</span><span class="sxs-lookup"><span data-stu-id="3b599-143">-NoWait</span></span>
<span data-ttu-id="3b599-144">Inicia a operação e retorna imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="3b599-144">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="3b599-145">Para determinar se a operação foi concluída com êxito, use outro mecanismo.</span><span class="sxs-lookup"><span data-stu-id="3b599-145">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="3b599-146">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="3b599-146">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="3b599-147">Especifica se o WriteAccelerator deve ser habilitado ou desabilitado no disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="3b599-147">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="3b599-148">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="3b599-148">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="3b599-149">A ID do recurso do grupo de posicionamento de proximidade a ser usado com esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3b599-149">The resource id of the Proximity Placement Group to use with this virtual machine.</span></span>

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

### <span data-ttu-id="3b599-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b599-150">-ResourceGroupName</span></span>
<span data-ttu-id="3b599-151">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3b599-151">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName, ExplicitIdentityParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b599-152">-Marca</span><span class="sxs-lookup"><span data-stu-id="3b599-152">-Tag</span></span>
<span data-ttu-id="3b599-153">Especifica os recursos e grupos de recursos que podem ser marcados com um conjunto de pares de nome-valor.</span><span class="sxs-lookup"><span data-stu-id="3b599-153">Specifies the resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="3b599-154">Adicionar marcas a recursos permite que você agrupe recursos em grupos de recursos e crie seus próprios modos de exibição.</span><span class="sxs-lookup"><span data-stu-id="3b599-154">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="3b599-155">Cada recurso ou grupo de recursos pode ter no máximo 15 marcas.</span><span class="sxs-lookup"><span data-stu-id="3b599-155">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="3b599-156">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="3b599-156">-UltraSSDEnabled</span></span>
<span data-ttu-id="3b599-157">O sinalizador que habilita ou desabilita uma funcionalidade para ter um ou mais discos de dados gerenciados com o tipo de conta de armazenamento UltraSSD_LRS na VM.</span><span class="sxs-lookup"><span data-stu-id="3b599-157">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="3b599-158">Discos gerenciados com o tipo de conta de armazenamento UltraSSD_LRS podem ser adicionados a uma máquina virtual apenas se essa propriedade estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="3b599-158">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>

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

### <span data-ttu-id="3b599-159">-VM</span><span class="sxs-lookup"><span data-stu-id="3b599-159">-VM</span></span>
<span data-ttu-id="3b599-160">Especifica um objeto de máquina virtual local.</span><span class="sxs-lookup"><span data-stu-id="3b599-160">Specifies a local virtual machine object.</span></span>
<span data-ttu-id="3b599-161">Para obter um objeto de máquina virtual, use o cmdlet Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="3b599-161">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="3b599-162">Esse objeto da máquina virtual contém o estado atualizado para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3b599-162">This virtual machine object contains the updated state for the virtual machine.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b599-163">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3b599-163">-Confirm</span></span>
<span data-ttu-id="3b599-164">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b599-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b599-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b599-165">-WhatIf</span></span>
<span data-ttu-id="3b599-166">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3b599-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b599-167">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3b599-167">The cmdlet is not run.</span></span>

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


### <span data-ttu-id="3b599-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b599-168">CommonParameters</span></span>
<span data-ttu-id="3b599-169">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b599-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b599-170">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3b599-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b599-171">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3b599-171">INPUTS</span></span>

### <span data-ttu-id="3b599-172">System. String</span><span class="sxs-lookup"><span data-stu-id="3b599-172">System.String</span></span>

### <span data-ttu-id="3b599-173">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="3b599-173">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="3b599-174">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3b599-174">System.Boolean</span></span>

## <span data-ttu-id="3b599-175">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3b599-175">OUTPUTS</span></span>

### <span data-ttu-id="3b599-176">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="3b599-176">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="3b599-177">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3b599-177">NOTES</span></span>

## <span data-ttu-id="3b599-178">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3b599-178">RELATED LINKS</span></span>

[<span data-ttu-id="3b599-179">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="3b599-179">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="3b599-180">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="3b599-180">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="3b599-181">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="3b599-181">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="3b599-182">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="3b599-182">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="3b599-183">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="3b599-183">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="3b599-184">Parar-AzVM</span><span class="sxs-lookup"><span data-stu-id="3b599-184">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="3b599-185">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="3b599-185">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


