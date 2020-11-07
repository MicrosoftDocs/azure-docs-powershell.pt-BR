---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 38917534-49C6-47EA-B815-240F794EE655
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
ms.openlocfilehash: e87536a524766ac86b80d790ee1372336fedba17
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771079"
---
# <span data-ttu-id="c8829-101">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="c8829-101">Update-AzVM</span></span>

## <span data-ttu-id="c8829-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c8829-102">SYNOPSIS</span></span>
<span data-ttu-id="c8829-103">Atualiza o estado de uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="c8829-103">Updates the state of an Azure virtual machine.</span></span>

## <span data-ttu-id="c8829-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c8829-104">SYNTAX</span></span>

### <span data-ttu-id="c8829-105">ResourceGroupNameParameterSetName (padrão)</span><span class="sxs-lookup"><span data-stu-id="c8829-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8829-106">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8829-106">AssignIdentityParameterSet</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-AssignIdentity]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8829-107">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8829-107">ExplicitIdentityParameterSet</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c8829-108">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="c8829-108">IdParameterSetName</span></span>
```
Update-AzVM [-Id] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c8829-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c8829-109">DESCRIPTION</span></span>
<span data-ttu-id="c8829-110">O cmdlet **Update-AzVM** atualiza o estado de uma máquina virtual do Azure para o estado de um objeto de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c8829-110">The **Update-AzVM** cmdlet updates the state of an Azure virtual machine to the state of a virtual machine object.</span></span>

## <span data-ttu-id="c8829-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c8829-111">EXAMPLES</span></span>

### <span data-ttu-id="c8829-112">Exemplo 1: atualizar uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="c8829-112">Example 1: Update a virtual machine</span></span>
```
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="c8829-113">Esse comando atualiza a máquina virtual, $VirtualMachine, no ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="c8829-113">This command updates the virtual machine, $VirtualMachine, in ResourceGroup11.</span></span>
<span data-ttu-id="c8829-114">O comando atualiza-o usando o objeto da máquina virtual armazenado na variável $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="c8829-114">The command updates it by using the virtual machine object stored in the $VirtualMachine variable.</span></span>
<span data-ttu-id="c8829-115">Para obter um objeto de máquina virtual, use o cmdlet **Get-AzVM** .</span><span class="sxs-lookup"><span data-stu-id="c8829-115">To obtain a virtual machine object, use the **Get-AzVM** cmdlet.</span></span>

## <span data-ttu-id="c8829-116">OS</span><span class="sxs-lookup"><span data-stu-id="c8829-116">PARAMETERS</span></span>

### <span data-ttu-id="c8829-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c8829-117">-AsJob</span></span>
<span data-ttu-id="c8829-118">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="c8829-118">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="c8829-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="c8829-119">-AssignIdentity</span></span>
<span data-ttu-id="c8829-120">Especifique a identidade atribuída pelo sistema para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c8829-120">Specify the system-assigned identity for the virtual machine.</span></span>

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

### <span data-ttu-id="c8829-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8829-121">-DefaultProfile</span></span>
<span data-ttu-id="c8829-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c8829-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8829-123">-ID</span><span class="sxs-lookup"><span data-stu-id="c8829-123">-Id</span></span>
<span data-ttu-id="c8829-124">Especifica a ID do recurso da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c8829-124">Specifies the resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="c8829-125">-Identityid</span><span class="sxs-lookup"><span data-stu-id="c8829-125">-IdentityId</span></span>
<span data-ttu-id="c8829-126">Especifica a lista de identidades de usuário associadas à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c8829-126">Specifies the list of user identities associated with the virtual machine.</span></span>
<span data-ttu-id="c8829-127">As referências de identidade do usuário serão identificadores de recurso ARM no formato: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="c8829-127">The user identity references will be ARM resource IDs in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="c8829-128">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="c8829-128">-IdentityType</span></span>
<span data-ttu-id="c8829-129">O tipo de identidade usado para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c8829-129">The type of identity used for the virtual machine.</span></span> <span data-ttu-id="c8829-130">Os valores válidos são SystemAssigned, userassign, SystemAssignedUserAssigned e None.</span><span class="sxs-lookup"><span data-stu-id="c8829-130">Valid values are SystemAssigned, UserAssigned, SystemAssignedUserAssigned, and None.</span></span>

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

### <span data-ttu-id="c8829-131">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="c8829-131">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="c8829-132">Especifica se o WriteAccelerator deve ser habilitado ou desabilitado no disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="c8829-132">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="c8829-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8829-133">-ResourceGroupName</span></span>
<span data-ttu-id="c8829-134">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c8829-134">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="c8829-135">-Marca</span><span class="sxs-lookup"><span data-stu-id="c8829-135">-Tag</span></span>
<span data-ttu-id="c8829-136">Especifica os recursos e grupos de recursos que podem ser marcados com um conjunto de pares de nome-valor.</span><span class="sxs-lookup"><span data-stu-id="c8829-136">Specifies the resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="c8829-137">Adicionar marcas a recursos permite que você agrupe recursos em grupos de recursos e crie seus próprios modos de exibição.</span><span class="sxs-lookup"><span data-stu-id="c8829-137">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="c8829-138">Cada recurso ou grupo de recursos pode ter no máximo 15 marcas.</span><span class="sxs-lookup"><span data-stu-id="c8829-138">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="c8829-139">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="c8829-139">-UltraSSDEnabled</span></span>
<span data-ttu-id="c8829-140">O sinalizador que habilita ou desabilita uma funcionalidade para ter um ou mais discos de dados gerenciados com o tipo de conta de armazenamento UltraSSD_LRS na VM.</span><span class="sxs-lookup"><span data-stu-id="c8829-140">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="c8829-141">Discos gerenciados com o tipo de conta de armazenamento UltraSSD_LRS podem ser adicionados a uma máquina virtual apenas se essa propriedade estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="c8829-141">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>

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

### <span data-ttu-id="c8829-142">-VM</span><span class="sxs-lookup"><span data-stu-id="c8829-142">-VM</span></span>
<span data-ttu-id="c8829-143">Especifica um objeto de máquina virtual local.</span><span class="sxs-lookup"><span data-stu-id="c8829-143">Specifies a local virtual machine object.</span></span>
<span data-ttu-id="c8829-144">Para obter um objeto de máquina virtual, use o cmdlet Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="c8829-144">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="c8829-145">Esse objeto da máquina virtual contém o estado atualizado para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c8829-145">This virtual machine object contains the updated state for the virtual machine.</span></span>

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

### <span data-ttu-id="c8829-146">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c8829-146">-Confirm</span></span>
<span data-ttu-id="c8829-147">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8829-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8829-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8829-148">-WhatIf</span></span>
<span data-ttu-id="c8829-149">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c8829-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8829-150">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c8829-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8829-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8829-151">CommonParameters</span></span>
<span data-ttu-id="c8829-152">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8829-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8829-153">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8829-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8829-154">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c8829-154">INPUTS</span></span>

### <span data-ttu-id="c8829-155">System. String</span><span class="sxs-lookup"><span data-stu-id="c8829-155">System.String</span></span>

### <span data-ttu-id="c8829-156">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="c8829-156">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="c8829-157">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c8829-157">System.Boolean</span></span>

## <span data-ttu-id="c8829-158">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c8829-158">OUTPUTS</span></span>

### <span data-ttu-id="c8829-159">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="c8829-159">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="c8829-160">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c8829-160">NOTES</span></span>

## <span data-ttu-id="c8829-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c8829-161">RELATED LINKS</span></span>

[<span data-ttu-id="c8829-162">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="c8829-162">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="c8829-163">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="c8829-163">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="c8829-164">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="c8829-164">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="c8829-165">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="c8829-165">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="c8829-166">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="c8829-166">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="c8829-167">Parar-AzVM</span><span class="sxs-lookup"><span data-stu-id="c8829-167">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="c8829-168">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="c8829-168">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


