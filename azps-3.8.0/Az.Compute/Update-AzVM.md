---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 38917534-49C6-47EA-B815-240F794EE655
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
ms.openlocfilehash: 6be4e505dfdacdc95e6ab3c9f7229fa4d1e470f1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942564"
---
# <span data-ttu-id="dfe83-101">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="dfe83-101">Update-AzVM</span></span>

## <span data-ttu-id="dfe83-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dfe83-102">SYNOPSIS</span></span>
<span data-ttu-id="dfe83-103">Atualiza o estado de uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="dfe83-103">Updates the state of an Azure virtual machine.</span></span>

## <span data-ttu-id="dfe83-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dfe83-104">SYNTAX</span></span>

### <span data-ttu-id="dfe83-105">ResourceGroupNameParameterSetName (padrão)</span><span class="sxs-lookup"><span data-stu-id="dfe83-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>]
 [-ProximityPlacementGroupId <String>] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfe83-106">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="dfe83-106">AssignIdentityParameterSet</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-AssignIdentity]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>]
 [-ProximityPlacementGroupId <String>] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfe83-107">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="dfe83-107">ExplicitIdentityParameterSet</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>] [-ProximityPlacementGroupId <String>] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfe83-108">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="dfe83-108">IdParameterSetName</span></span>
```
Update-AzVM [-Id] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>] [-ProximityPlacementGroupId <String>] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dfe83-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dfe83-109">DESCRIPTION</span></span>
<span data-ttu-id="dfe83-110">O cmdlet **Update-AzVM** atualiza o estado de uma máquina virtual do Azure para o estado de um objeto de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dfe83-110">The **Update-AzVM** cmdlet updates the state of an Azure virtual machine to the state of a virtual machine object.</span></span>

## <span data-ttu-id="dfe83-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dfe83-111">EXAMPLES</span></span>

### <span data-ttu-id="dfe83-112">Exemplo 1: atualizar uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="dfe83-112">Example 1: Update a virtual machine</span></span>
```
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="dfe83-113">Esse comando atualiza a máquina virtual, $VirtualMachine, no ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="dfe83-113">This command updates the virtual machine, $VirtualMachine, in ResourceGroup11.</span></span>
<span data-ttu-id="dfe83-114">O comando atualiza-o usando o objeto da máquina virtual armazenado na variável $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="dfe83-114">The command updates it by using the virtual machine object stored in the $VirtualMachine variable.</span></span>
<span data-ttu-id="dfe83-115">Para obter um objeto de máquina virtual, use o cmdlet **Get-AzVM** .</span><span class="sxs-lookup"><span data-stu-id="dfe83-115">To obtain a virtual machine object, use the **Get-AzVM** cmdlet.</span></span>

## <span data-ttu-id="dfe83-116">OS</span><span class="sxs-lookup"><span data-stu-id="dfe83-116">PARAMETERS</span></span>

### <span data-ttu-id="dfe83-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dfe83-117">-AsJob</span></span>
<span data-ttu-id="dfe83-118">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="dfe83-118">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="dfe83-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="dfe83-119">-AssignIdentity</span></span>
<span data-ttu-id="dfe83-120">Especifique a identidade atribuída pelo sistema para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dfe83-120">Specify the system-assigned identity for the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AssignIdentityParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfe83-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfe83-121">-DefaultProfile</span></span>
<span data-ttu-id="dfe83-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dfe83-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dfe83-123">-ID</span><span class="sxs-lookup"><span data-stu-id="dfe83-123">-Id</span></span>
<span data-ttu-id="dfe83-124">Especifica a ID do recurso da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dfe83-124">Specifies the resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="dfe83-125">-Identityid</span><span class="sxs-lookup"><span data-stu-id="dfe83-125">-IdentityId</span></span>
<span data-ttu-id="dfe83-126">Especifica a lista de identidades de usuário associadas à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dfe83-126">Specifies the list of user identities associated with the virtual machine.</span></span>
<span data-ttu-id="dfe83-127">As referências de identidade do usuário serão identificadores de recurso ARM no formato: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="dfe83-127">The user identity references will be ARM resource IDs in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="dfe83-128">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="dfe83-128">-IdentityType</span></span>
<span data-ttu-id="dfe83-129">O tipo de identidade usado para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dfe83-129">The type of identity used for the virtual machine.</span></span> <span data-ttu-id="dfe83-130">Os valores válidos são SystemAssigned, userassign, SystemAssignedUserAssigned e None.</span><span class="sxs-lookup"><span data-stu-id="dfe83-130">Valid values are SystemAssigned, UserAssigned, SystemAssignedUserAssigned, and None.</span></span>

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

### <span data-ttu-id="dfe83-131">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="dfe83-131">-MaxPrice</span></span>
<span data-ttu-id="dfe83-132">Especifica o preço máximo que você está disposto a pagar por uma VM/VMSS de baixa prioridade.</span><span class="sxs-lookup"><span data-stu-id="dfe83-132">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="dfe83-133">Este preço está em dólares americanos.</span><span class="sxs-lookup"><span data-stu-id="dfe83-133">This price is in US Dollars.</span></span> <span data-ttu-id="dfe83-134">Esse preço será comparado com o preço de baixa prioridade atual para o tamanho da VM.</span><span class="sxs-lookup"><span data-stu-id="dfe83-134">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="dfe83-135">Além disso, os preços são comparados no momento da criação/atualização de VMs/VMSS de baixa prioridade e a operação será bem-sucedida apenas se o maxPrice for maior do que o preço de baixa prioridade atual.</span><span class="sxs-lookup"><span data-stu-id="dfe83-135">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="dfe83-136">O maxPrice também será usado para remover uma VM/VMSS de baixa prioridade se o preço atual de baixa prioridade vai além do maxPrice após a criação de VM/VMSS.</span><span class="sxs-lookup"><span data-stu-id="dfe83-136">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="dfe83-137">Os valores possíveis são: qualquer valor decimal maior do que zero.</span><span class="sxs-lookup"><span data-stu-id="dfe83-137">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="dfe83-138">Exemplo: 0, 1538.</span><span class="sxs-lookup"><span data-stu-id="dfe83-138">Example: 0.01538.</span></span>  <span data-ttu-id="dfe83-139">-1 indica que a VM de baixa prioridade/VMSS não deve ser removida por motivos de preço.</span><span class="sxs-lookup"><span data-stu-id="dfe83-139">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="dfe83-140">Além disso, o preço máximo padrão é-1 se não for fornecido por você.</span><span class="sxs-lookup"><span data-stu-id="dfe83-140">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="dfe83-141">-Nowait</span><span class="sxs-lookup"><span data-stu-id="dfe83-141">-NoWait</span></span>
<span data-ttu-id="dfe83-142">Inicia a operação e retorna imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="dfe83-142">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="dfe83-143">Para determinar se a operação foi concluída com êxito, use outro mecanismo.</span><span class="sxs-lookup"><span data-stu-id="dfe83-143">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="dfe83-144">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="dfe83-144">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="dfe83-145">Especifica se o WriteAccelerator deve ser habilitado ou desabilitado no disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="dfe83-145">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="dfe83-146">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="dfe83-146">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="dfe83-147">A ID do recurso do grupo de posicionamento de proximidade a ser usado com esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dfe83-147">The resource id of the Proximity Placement Group to use with this virtual machine.</span></span>

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

### <span data-ttu-id="dfe83-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfe83-148">-ResourceGroupName</span></span>
<span data-ttu-id="dfe83-149">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dfe83-149">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName, AssignIdentityParameterSet, ExplicitIdentityParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfe83-150">-Marca</span><span class="sxs-lookup"><span data-stu-id="dfe83-150">-Tag</span></span>
<span data-ttu-id="dfe83-151">Especifica os recursos e grupos de recursos que podem ser marcados com um conjunto de pares de nome-valor.</span><span class="sxs-lookup"><span data-stu-id="dfe83-151">Specifies the resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="dfe83-152">Adicionar marcas a recursos permite que você agrupe recursos em grupos de recursos e crie seus próprios modos de exibição.</span><span class="sxs-lookup"><span data-stu-id="dfe83-152">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="dfe83-153">Cada recurso ou grupo de recursos pode ter no máximo 15 marcas.</span><span class="sxs-lookup"><span data-stu-id="dfe83-153">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="dfe83-154">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="dfe83-154">-UltraSSDEnabled</span></span>
<span data-ttu-id="dfe83-155">O sinalizador que habilita ou desabilita uma funcionalidade para ter um ou mais discos de dados gerenciados com o tipo de conta de armazenamento UltraSSD_LRS na VM.</span><span class="sxs-lookup"><span data-stu-id="dfe83-155">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="dfe83-156">Discos gerenciados com o tipo de conta de armazenamento UltraSSD_LRS podem ser adicionados a uma máquina virtual apenas se essa propriedade estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="dfe83-156">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>

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

### <span data-ttu-id="dfe83-157">-VM</span><span class="sxs-lookup"><span data-stu-id="dfe83-157">-VM</span></span>
<span data-ttu-id="dfe83-158">Especifica um objeto de máquina virtual local.</span><span class="sxs-lookup"><span data-stu-id="dfe83-158">Specifies a local virtual machine object.</span></span>
<span data-ttu-id="dfe83-159">Para obter um objeto de máquina virtual, use o cmdlet Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="dfe83-159">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="dfe83-160">Esse objeto da máquina virtual contém o estado atualizado para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dfe83-160">This virtual machine object contains the updated state for the virtual machine.</span></span>

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

### <span data-ttu-id="dfe83-161">-Confirme</span><span class="sxs-lookup"><span data-stu-id="dfe83-161">-Confirm</span></span>
<span data-ttu-id="dfe83-162">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dfe83-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfe83-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfe83-163">-WhatIf</span></span>
<span data-ttu-id="dfe83-164">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="dfe83-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dfe83-165">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dfe83-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfe83-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfe83-166">CommonParameters</span></span>
<span data-ttu-id="dfe83-167">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfe83-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfe83-168">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dfe83-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfe83-169">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dfe83-169">INPUTS</span></span>

### <span data-ttu-id="dfe83-170">System. String</span><span class="sxs-lookup"><span data-stu-id="dfe83-170">System.String</span></span>

### <span data-ttu-id="dfe83-171">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="dfe83-171">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="dfe83-172">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dfe83-172">System.Boolean</span></span>

## <span data-ttu-id="dfe83-173">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dfe83-173">OUTPUTS</span></span>

### <span data-ttu-id="dfe83-174">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="dfe83-174">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="dfe83-175">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dfe83-175">NOTES</span></span>

## <span data-ttu-id="dfe83-176">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dfe83-176">RELATED LINKS</span></span>

[<span data-ttu-id="dfe83-177">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="dfe83-177">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="dfe83-178">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="dfe83-178">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="dfe83-179">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="dfe83-179">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="dfe83-180">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="dfe83-180">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="dfe83-181">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="dfe83-181">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="dfe83-182">Parar-AzVM</span><span class="sxs-lookup"><span data-stu-id="dfe83-182">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="dfe83-183">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="dfe83-183">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


