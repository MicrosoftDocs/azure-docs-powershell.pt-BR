---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 38917534-49C6-47EA-B815-240F794EE655
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
ms.openlocfilehash: e9ec68d7c3991d7a3eded2566d8e299ddcc36c85
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111065"
---
# <span data-ttu-id="992b5-101">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="992b5-101">Update-AzVM</span></span>

## <span data-ttu-id="992b5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="992b5-102">SYNOPSIS</span></span>
<span data-ttu-id="992b5-103">Atualiza o estado de uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="992b5-103">Updates the state of an Azure virtual machine.</span></span>

## <span data-ttu-id="992b5-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="992b5-104">SYNTAX</span></span>

### <span data-ttu-id="992b5-105">ResourceGroupNameParameterSetName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="992b5-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>]
 [-ProximityPlacementGroupId <String>] [-HostId <String>] [-EncryptionAtHost <Boolean>] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="992b5-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="992b5-106">ExplicitIdentityParameterSet</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>] [-ProximityPlacementGroupId <String>] [-HostId <String>]
 [-EncryptionAtHost <Boolean>] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="992b5-107">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="992b5-107">IdParameterSetName</span></span>
```
Update-AzVM [-Id] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>] [-ProximityPlacementGroupId <String>] [-HostId <String>]
 [-EncryptionAtHost <Boolean>] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="992b5-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="992b5-108">DESCRIPTION</span></span>
<span data-ttu-id="992b5-109">O **cmdlet Update-AzVM** atualiza o estado de uma máquina virtual do Azure para o estado de um objeto de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="992b5-109">The **Update-AzVM** cmdlet updates the state of an Azure virtual machine to the state of a virtual machine object.</span></span>

## <span data-ttu-id="992b5-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="992b5-110">EXAMPLES</span></span>

### <span data-ttu-id="992b5-111">Exemplo 1: Atualizar uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="992b5-111">Example 1: Update a virtual machine</span></span>
```
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="992b5-112">Este comando atualiza a máquina virtual, $VirtualMachine, no ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="992b5-112">This command updates the virtual machine, $VirtualMachine, in ResourceGroup11.</span></span>
<span data-ttu-id="992b5-113">O comando o atualiza usando o objeto de máquina virtual armazenado na variável $VirtualMachine dados.</span><span class="sxs-lookup"><span data-stu-id="992b5-113">The command updates it by using the virtual machine object stored in the $VirtualMachine variable.</span></span>
<span data-ttu-id="992b5-114">Para obter um objeto de máquina virtual, use **o cmdlet Get-AzVM.**</span><span class="sxs-lookup"><span data-stu-id="992b5-114">To obtain a virtual machine object, use the **Get-AzVM** cmdlet.</span></span>

## <span data-ttu-id="992b5-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="992b5-115">PARAMETERS</span></span>

### <span data-ttu-id="992b5-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="992b5-116">-AsJob</span></span>
<span data-ttu-id="992b5-117">Execute o cmdlet em segundo plano e retorne um Trabalho para controlar o andamento.</span><span class="sxs-lookup"><span data-stu-id="992b5-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="992b5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="992b5-118">-DefaultProfile</span></span>
<span data-ttu-id="992b5-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="992b5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="992b5-120">-HostId</span><span class="sxs-lookup"><span data-stu-id="992b5-120">-HostId</span></span>
<span data-ttu-id="992b5-121">A ID do Host</span><span class="sxs-lookup"><span data-stu-id="992b5-121">The Id of Host</span></span>

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

### <span data-ttu-id="992b5-122">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="992b5-122">-EncryptionAtHost</span></span>
<span data-ttu-id="992b5-123">A propriedade EncryptionAtHost pode ser usada pelo usuário na solicitação para habilitar ou desabilitar a Criptografia de Host para o conjunto de escala de máquina virtual ou de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="992b5-123">EncryptionAtHost property can be used by user in the request to enable or disable the Host Encryption for the virtual machine or virtual machine scale set.</span></span> <span data-ttu-id="992b5-124">Isso habilitará a criptografia para todos os discos, incluindo o disco Resource/Temp no próprio host.</span><span class="sxs-lookup"><span data-stu-id="992b5-124">This will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> 

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

### <span data-ttu-id="992b5-125">-ID</span><span class="sxs-lookup"><span data-stu-id="992b5-125">-Id</span></span>
<span data-ttu-id="992b5-126">Especifica a ID de recurso da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="992b5-126">Specifies the resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="992b5-127">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="992b5-127">-IdentityId</span></span>
<span data-ttu-id="992b5-128">Especifica a lista de identidades de usuário associadas à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="992b5-128">Specifies the list of user identities associated with the virtual machine.</span></span>
<span data-ttu-id="992b5-129">As referências de identidade do usuário serão IDs de recurso ARM no formulário: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span><span class="sxs-lookup"><span data-stu-id="992b5-129">The user identity references will be ARM resource IDs in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="992b5-130">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="992b5-130">-IdentityType</span></span>
<span data-ttu-id="992b5-131">O tipo de identidade usado para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="992b5-131">The type of identity used for the virtual machine.</span></span> <span data-ttu-id="992b5-132">Os valores válidos são SystemAssigned, UserAssigned, SystemAssignedUserAssigned e None.</span><span class="sxs-lookup"><span data-stu-id="992b5-132">Valid values are SystemAssigned, UserAssigned, SystemAssignedUserAssigned, and None.</span></span>

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

### <span data-ttu-id="992b5-133">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="992b5-133">-MaxPrice</span></span>
<span data-ttu-id="992b5-134">Especifica o preço máximo que você está disposto a pagar por um VM/VMSS de baixa prioridade.</span><span class="sxs-lookup"><span data-stu-id="992b5-134">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="992b5-135">Este preço está em dólares americanos.</span><span class="sxs-lookup"><span data-stu-id="992b5-135">This price is in US Dollars.</span></span> <span data-ttu-id="992b5-136">Esse preço será comparado com o preço atual de baixa prioridade para o tamanho do VM.</span><span class="sxs-lookup"><span data-stu-id="992b5-136">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="992b5-137">Além disso, os preços são comparados no momento da criação/atualização de VM/VMSS de baixa prioridade e a operação só será bem-sucedida se o preço máximo for maior do que o preço de baixa prioridade atual.</span><span class="sxs-lookup"><span data-stu-id="992b5-137">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="992b5-138">O maxPrice também será usado para desapropriar um VM/VMSS de baixa prioridade se o preço atual de baixa prioridade ultrapassar o máximoPrice após a criação do VM/VMSS.</span><span class="sxs-lookup"><span data-stu-id="992b5-138">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="992b5-139">Os valores possíveis são: qualquer valor decimal maior que zero.</span><span class="sxs-lookup"><span data-stu-id="992b5-139">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="992b5-140">Exemplo: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="992b5-140">Example: 0.01538.</span></span>  <span data-ttu-id="992b5-141">-1 indica que o VM/VMSS de baixa prioridade não deve ser despejado por motivos de preço.</span><span class="sxs-lookup"><span data-stu-id="992b5-141">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="992b5-142">Além disso, o preço máximo padrão será -1 se ele não for fornecido por você.</span><span class="sxs-lookup"><span data-stu-id="992b5-142">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="992b5-143">-NoWait</span><span class="sxs-lookup"><span data-stu-id="992b5-143">-NoWait</span></span>
<span data-ttu-id="992b5-144">Inicia a operação e retorna imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="992b5-144">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="992b5-145">Para determinar se a operação foi concluída com êxito, use algum outro mecanismo.</span><span class="sxs-lookup"><span data-stu-id="992b5-145">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="992b5-146">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="992b5-146">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="992b5-147">Especifica se o WriteAccelerator deve estar habilitado ou desabilitado no disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="992b5-147">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="992b5-148">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="992b5-148">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="992b5-149">A ID do recurso do Grupo de Posicionamento de Proximidade a ser usado com esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="992b5-149">The resource id of the Proximity Placement Group to use with this virtual machine.</span></span>

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

### <span data-ttu-id="992b5-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="992b5-150">-ResourceGroupName</span></span>
<span data-ttu-id="992b5-151">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="992b5-151">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="992b5-152">-Tag</span><span class="sxs-lookup"><span data-stu-id="992b5-152">-Tag</span></span>
<span data-ttu-id="992b5-153">Especifica que os recursos e grupos de recursos podem ser marcados com um conjunto de pares de nome e valor.</span><span class="sxs-lookup"><span data-stu-id="992b5-153">Specifies the resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="992b5-154">Adicionar marcas aos recursos permite agrupar recursos entre grupos de recursos e criar seus próprios modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="992b5-154">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="992b5-155">Cada grupo de recursos ou recursos pode ter no máximo 15 marcas.</span><span class="sxs-lookup"><span data-stu-id="992b5-155">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="992b5-156">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="992b5-156">-UltraSSDEnabled</span></span>
<span data-ttu-id="992b5-157">O sinalizador que habilita ou desabilita um recurso de ter um ou mais discos de dados gerenciados com UltraSSD_LRS de armazenamento no VM.</span><span class="sxs-lookup"><span data-stu-id="992b5-157">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="992b5-158">Os discos gerenciados com tipo de conta de armazenamento UltraSSD_LRS podem ser adicionados a uma máquina virtual somente se essa propriedade estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="992b5-158">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>

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

### <span data-ttu-id="992b5-159">-VM</span><span class="sxs-lookup"><span data-stu-id="992b5-159">-VM</span></span>
<span data-ttu-id="992b5-160">Especifica um objeto de máquina virtual local.</span><span class="sxs-lookup"><span data-stu-id="992b5-160">Specifies a local virtual machine object.</span></span>
<span data-ttu-id="992b5-161">Para obter um objeto virtual de máquina, use o cmdlet Get-AzVM computador.</span><span class="sxs-lookup"><span data-stu-id="992b5-161">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="992b5-162">Este objeto virtual de máquina contém o estado atualizado para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="992b5-162">This virtual machine object contains the updated state for the virtual machine.</span></span>

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

### <span data-ttu-id="992b5-163">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="992b5-163">-Confirm</span></span>
<span data-ttu-id="992b5-164">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="992b5-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="992b5-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="992b5-165">-WhatIf</span></span>
<span data-ttu-id="992b5-166">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="992b5-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="992b5-167">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="992b5-167">The cmdlet is not run.</span></span>

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


### <span data-ttu-id="992b5-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="992b5-168">CommonParameters</span></span>
<span data-ttu-id="992b5-169">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="992b5-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="992b5-170">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="992b5-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="992b5-171">Entradas</span><span class="sxs-lookup"><span data-stu-id="992b5-171">INPUTS</span></span>

### <span data-ttu-id="992b5-172">System.String</span><span class="sxs-lookup"><span data-stu-id="992b5-172">System.String</span></span>

### <span data-ttu-id="992b5-173">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="992b5-173">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="992b5-174">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="992b5-174">System.Boolean</span></span>

## <span data-ttu-id="992b5-175">Saídas</span><span class="sxs-lookup"><span data-stu-id="992b5-175">OUTPUTS</span></span>

### <span data-ttu-id="992b5-176">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="992b5-176">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="992b5-177">Notas</span><span class="sxs-lookup"><span data-stu-id="992b5-177">NOTES</span></span>

## <span data-ttu-id="992b5-178">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="992b5-178">RELATED LINKS</span></span>

[<span data-ttu-id="992b5-179">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="992b5-179">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="992b5-180">Novo-AzVM</span><span class="sxs-lookup"><span data-stu-id="992b5-180">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="992b5-181">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="992b5-181">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="992b5-182">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="992b5-182">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="992b5-183">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="992b5-183">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="992b5-184">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="992b5-184">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="992b5-185">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="992b5-185">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


