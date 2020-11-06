---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 38917534-49C6-47EA-B815-240F794EE655
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmVM.md
ms.openlocfilehash: e29eb849dfd7ec3417daaea1b0cae447d20f1322
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432027"
---
# <span data-ttu-id="3b667-101">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="3b667-101">Update-AzureRmVM</span></span>

## <span data-ttu-id="3b667-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3b667-102">SYNOPSIS</span></span>
<span data-ttu-id="3b667-103">Atualiza o estado de uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="3b667-103">Updates the state of an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b667-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3b667-104">SYNTAX</span></span>

### <span data-ttu-id="3b667-105">ResourceGroupNameParameterSetName (padrão)</span><span class="sxs-lookup"><span data-stu-id="3b667-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Update-AzureRmVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b667-106">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b667-106">AssignIdentityParameterSet</span></span>
```
Update-AzureRmVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-AssignIdentity]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b667-107">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b667-107">ExplicitIdentityParameterSet</span></span>
```
Update-AzureRmVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3b667-108">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="3b667-108">IdParameterSetName</span></span>
```
Update-AzureRmVM [-Id] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3b667-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3b667-109">DESCRIPTION</span></span>
<span data-ttu-id="3b667-110">O cmdlet **Update-AzureRmVM** atualiza o estado de uma máquina virtual do Azure para o estado de um objeto de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3b667-110">The **Update-AzureRmVM** cmdlet updates the state of an Azure virtual machine to the state of a virtual machine object.</span></span>

## <span data-ttu-id="3b667-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3b667-111">EXAMPLES</span></span>

### <span data-ttu-id="3b667-112">Exemplo 1: atualizar uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="3b667-112">Example 1: Update a virtual machine</span></span>
```
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="3b667-113">Esse comando atualiza a máquina virtual, $VirtualMachine, no ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="3b667-113">This command updates the virtual machine, $VirtualMachine, in ResourceGroup11.</span></span>
<span data-ttu-id="3b667-114">O comando atualiza-o usando o objeto da máquina virtual armazenado na variável $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="3b667-114">The command updates it by using the virtual machine object stored in the $VirtualMachine variable.</span></span>
<span data-ttu-id="3b667-115">Para obter um objeto de máquina virtual, use o cmdlet **Get-AzureRmVM** .</span><span class="sxs-lookup"><span data-stu-id="3b667-115">To obtain a virtual machine object, use the **Get-AzureRmVM** cmdlet.</span></span>

## <span data-ttu-id="3b667-116">OS</span><span class="sxs-lookup"><span data-stu-id="3b667-116">PARAMETERS</span></span>

### <span data-ttu-id="3b667-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3b667-117">-AsJob</span></span>
<span data-ttu-id="3b667-118">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="3b667-118">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="3b667-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="3b667-119">-AssignIdentity</span></span>
<span data-ttu-id="3b667-120">Especifique a identidade atribuída ao sistema para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3b667-120">Specify the system assigned identity for the virtual machine.</span></span>

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

### <span data-ttu-id="3b667-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b667-121">-DefaultProfile</span></span>
<span data-ttu-id="3b667-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3b667-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b667-123">-ID</span><span class="sxs-lookup"><span data-stu-id="3b667-123">-Id</span></span>
<span data-ttu-id="3b667-124">Especifica a ID do recurso da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3b667-124">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="3b667-125">-Identityid</span><span class="sxs-lookup"><span data-stu-id="3b667-125">-IdentityId</span></span>
<span data-ttu-id="3b667-126">Especifica a lista de identidades de usuário associadas ao conjunto de escalas da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3b667-126">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="3b667-127">As referências de identidade do usuário serão identificadores de recurso ARM no formato: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="3b667-127">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="3b667-128">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="3b667-128">-IdentityType</span></span>
<span data-ttu-id="3b667-129">O tipo de identidade usado para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3b667-129">The type of identity used for the virtual machine.</span></span> <span data-ttu-id="3b667-130">Atualmente, o único tipo com suporte é ' SystemAssigned ', que implicitamente cria uma identidade.</span><span class="sxs-lookup"><span data-stu-id="3b667-130">Currently, the only supported type is 'SystemAssigned', which implicitly creates an identity.</span></span>

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

### <span data-ttu-id="3b667-131">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="3b667-131">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="3b667-132">Especifica se o WriteAccelerator deve ser habilitado ou desabilitado no disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="3b667-132">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="3b667-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b667-133">-ResourceGroupName</span></span>
<span data-ttu-id="3b667-134">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3b667-134">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="3b667-135">-Marca</span><span class="sxs-lookup"><span data-stu-id="3b667-135">-Tag</span></span>
<span data-ttu-id="3b667-136">Especifica os recursos e grupos de recursos que podem ser marcados com um conjunto de pares de nome-valor.</span><span class="sxs-lookup"><span data-stu-id="3b667-136">Specifies the resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="3b667-137">Adicionar marcas a recursos permite que você agrupe recursos em grupos de recursos e crie seus próprios modos de exibição.</span><span class="sxs-lookup"><span data-stu-id="3b667-137">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="3b667-138">Cada recurso ou grupo de recursos pode ter no máximo 15 marcas.</span><span class="sxs-lookup"><span data-stu-id="3b667-138">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="3b667-139">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="3b667-139">-UltraSSDEnabled</span></span>
<span data-ttu-id="3b667-140">O sinalizador que habilita ou desabilita uma funcionalidade para ter um ou mais discos de dados gerenciados com o tipo de conta de armazenamento UltraSSD_LRS na VM.</span><span class="sxs-lookup"><span data-stu-id="3b667-140">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="3b667-141">Discos gerenciados com o tipo de conta de armazenamento UltraSSD_LRS podem ser adicionados a uma máquina virtual apenas se essa propriedade estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="3b667-141">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>

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

### <span data-ttu-id="3b667-142">-VM</span><span class="sxs-lookup"><span data-stu-id="3b667-142">-VM</span></span>
<span data-ttu-id="3b667-143">Especifica um objeto de máquina virtual local.</span><span class="sxs-lookup"><span data-stu-id="3b667-143">Specifies a local virtual machine object.</span></span>
<span data-ttu-id="3b667-144">Para obter um objeto de máquina virtual, use o cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="3b667-144">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="3b667-145">Esse objeto da máquina virtual contém o estado atualizado para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3b667-145">This virtual machine object contains the updated state for the virtual machine.</span></span>

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

### <span data-ttu-id="3b667-146">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3b667-146">-Confirm</span></span>
<span data-ttu-id="3b667-147">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b667-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b667-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b667-148">-WhatIf</span></span>
<span data-ttu-id="3b667-149">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3b667-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b667-150">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3b667-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b667-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b667-151">CommonParameters</span></span>
<span data-ttu-id="3b667-152">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b667-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b667-153">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b667-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b667-154">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3b667-154">INPUTS</span></span>

### <span data-ttu-id="3b667-155">System. String</span><span class="sxs-lookup"><span data-stu-id="3b667-155">System.String</span></span>

### <span data-ttu-id="3b667-156">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="3b667-156">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="3b667-157">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3b667-157">OUTPUTS</span></span>

### <span data-ttu-id="3b667-158">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="3b667-158">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="3b667-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3b667-159">NOTES</span></span>

## <span data-ttu-id="3b667-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3b667-160">RELATED LINKS</span></span>

[<span data-ttu-id="3b667-161">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="3b667-161">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="3b667-162">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="3b667-162">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="3b667-163">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="3b667-163">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="3b667-164">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="3b667-164">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="3b667-165">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="3b667-165">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="3b667-166">Parar-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="3b667-166">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="3b667-167">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="3b667-167">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)


