---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 38917534-49C6-47EA-B815-240F794EE655
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzVM.md
ms.openlocfilehash: 8dd18c97a1636e4b6422d58fa7aca28d8798001b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775938"
---
# <span data-ttu-id="3eab7-101">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="3eab7-101">Update-AzVM</span></span>

## <span data-ttu-id="3eab7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3eab7-102">SYNOPSIS</span></span>
<span data-ttu-id="3eab7-103">Atualiza o estado de uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="3eab7-103">Updates the state of an Azure virtual machine.</span></span>

## <span data-ttu-id="3eab7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3eab7-104">SYNTAX</span></span>

### <span data-ttu-id="3eab7-105">ResourceGroupNameParameterSetName (padrão)</span><span class="sxs-lookup"><span data-stu-id="3eab7-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 [-OsDiskWriteAccelerator <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3eab7-106">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="3eab7-106">AssignIdentityParameterSet</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-AssignIdentity]
 [-OsDiskWriteAccelerator <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3eab7-107">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="3eab7-107">ExplicitIdentityParameterSet</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsDiskWriteAccelerator <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3eab7-108">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="3eab7-108">IdParameterSetName</span></span>
```
Update-AzVM [-Id] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-OsDiskWriteAccelerator <Boolean>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3eab7-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3eab7-109">DESCRIPTION</span></span>
<span data-ttu-id="3eab7-110">O cmdlet **Update-AzVM** atualiza o estado de uma máquina virtual do Azure para o estado de um objeto de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3eab7-110">The **Update-AzVM** cmdlet updates the state of an Azure virtual machine to the state of a virtual machine object.</span></span>

## <span data-ttu-id="3eab7-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3eab7-111">EXAMPLES</span></span>

### <span data-ttu-id="3eab7-112">Exemplo 1: atualizar uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="3eab7-112">Example 1: Update a virtual machine</span></span>
```
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="3eab7-113">Esse comando atualiza a máquina virtual, $VirtualMachine, no ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="3eab7-113">This command updates the virtual machine, $VirtualMachine, in ResourceGroup11.</span></span>
<span data-ttu-id="3eab7-114">O comando atualiza-o usando o objeto da máquina virtual armazenado na variável $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="3eab7-114">The command updates it by using the virtual machine object stored in the $VirtualMachine variable.</span></span>
<span data-ttu-id="3eab7-115">Para obter um objeto de máquina virtual, use o cmdlet **Get-AzVM** .</span><span class="sxs-lookup"><span data-stu-id="3eab7-115">To obtain a virtual machine object, use the **Get-AzVM** cmdlet.</span></span>

## <span data-ttu-id="3eab7-116">OS</span><span class="sxs-lookup"><span data-stu-id="3eab7-116">PARAMETERS</span></span>

### <span data-ttu-id="3eab7-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3eab7-117">-AsJob</span></span>
<span data-ttu-id="3eab7-118">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="3eab7-118">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="3eab7-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="3eab7-119">-AssignIdentity</span></span>
<span data-ttu-id="3eab7-120">Especifique a identidade atribuída ao sistema para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3eab7-120">Specify the system assigned identity for the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AssignIdentityParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eab7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3eab7-121">-DefaultProfile</span></span>
<span data-ttu-id="3eab7-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3eab7-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3eab7-123">-ID</span><span class="sxs-lookup"><span data-stu-id="3eab7-123">-Id</span></span>
<span data-ttu-id="3eab7-124">Especifica a ID do recurso da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3eab7-124">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3eab7-125">-Identityid</span><span class="sxs-lookup"><span data-stu-id="3eab7-125">-IdentityId</span></span>
<span data-ttu-id="3eab7-126">Especifica a lista de identidades de usuário associadas ao conjunto de escalas da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3eab7-126">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="3eab7-127">As referências de identidade do usuário serão identificadores de recurso ARM no formato: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="3eab7-127">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="3eab7-128">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="3eab7-128">-IdentityType</span></span>
<span data-ttu-id="3eab7-129">O tipo de identidade usado para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3eab7-129">The type of identity used for the virtual machine.</span></span> <span data-ttu-id="3eab7-130">Atualmente, o único tipo com suporte é ' SystemAssigned ', que implicitamente cria uma identidade.</span><span class="sxs-lookup"><span data-stu-id="3eab7-130">Currently, the only supported type is 'SystemAssigned', which implicitly creates an identity.</span></span>

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

### <span data-ttu-id="3eab7-131">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="3eab7-131">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="3eab7-132">Especifica se o WriteAccelerator deve ser habilitado ou desabilitado no disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="3eab7-132">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="3eab7-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3eab7-133">-ResourceGroupName</span></span>
<span data-ttu-id="3eab7-134">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3eab7-134">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSetName, AssignIdentityParameterSet, ExplicitIdentityParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3eab7-135">-Marca</span><span class="sxs-lookup"><span data-stu-id="3eab7-135">-Tag</span></span>
<span data-ttu-id="3eab7-136">Especifica os recursos e grupos de recursos que podem ser marcados com um conjunto de pares de nome-valor.</span><span class="sxs-lookup"><span data-stu-id="3eab7-136">Specifies the resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="3eab7-137">Adicionar marcas a recursos permite que você agrupe recursos em grupos de recursos e crie seus próprios modos de exibição.</span><span class="sxs-lookup"><span data-stu-id="3eab7-137">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="3eab7-138">Cada recurso ou grupo de recursos pode ter no máximo 15 marcas.</span><span class="sxs-lookup"><span data-stu-id="3eab7-138">Each resource or resource group can have a maximum of 15 tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eab7-139">-VM</span><span class="sxs-lookup"><span data-stu-id="3eab7-139">-VM</span></span>
<span data-ttu-id="3eab7-140">Especifica um objeto de máquina virtual local.</span><span class="sxs-lookup"><span data-stu-id="3eab7-140">Specifies a local virtual machine object.</span></span>
<span data-ttu-id="3eab7-141">Para obter um objeto de máquina virtual, use o cmdlet Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="3eab7-141">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="3eab7-142">Esse objeto da máquina virtual contém o estado atualizado para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3eab7-142">This virtual machine object contains the updated state for the virtual machine.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3eab7-143">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3eab7-143">-Confirm</span></span>
<span data-ttu-id="3eab7-144">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3eab7-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3eab7-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3eab7-145">-WhatIf</span></span>
<span data-ttu-id="3eab7-146">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3eab7-146">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="3eab7-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3eab7-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3eab7-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3eab7-148">CommonParameters</span></span>
<span data-ttu-id="3eab7-149">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3eab7-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3eab7-150">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3eab7-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3eab7-151">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3eab7-151">INPUTS</span></span>

### <span data-ttu-id="3eab7-152">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="3eab7-152">PSVirtualMachine</span></span>
<span data-ttu-id="3eab7-153">O parâmetro ' VM ' aceita o valor do tipo ' PSVirtualMachine ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="3eab7-153">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="3eab7-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3eab7-154">OUTPUTS</span></span>

### <span data-ttu-id="3eab7-155">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="3eab7-155">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="3eab7-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3eab7-156">NOTES</span></span>

## <span data-ttu-id="3eab7-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3eab7-157">RELATED LINKS</span></span>

[<span data-ttu-id="3eab7-158">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="3eab7-158">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="3eab7-159">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="3eab7-159">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="3eab7-160">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="3eab7-160">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="3eab7-161">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="3eab7-161">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="3eab7-162">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="3eab7-162">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="3eab7-163">Parar-AzVM</span><span class="sxs-lookup"><span data-stu-id="3eab7-163">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="3eab7-164">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="3eab7-164">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


