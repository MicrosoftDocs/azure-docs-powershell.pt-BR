---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 38917534-49C6-47EA-B815-240F794EE655
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermvm
schema: 2.0.0
ms.openlocfilehash: 55f7b56f57bf18c4a3bf3198e8335cff08caae97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426763"
---
# <span data-ttu-id="9fa25-101">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9fa25-101">Update-AzureRmVM</span></span>

## <span data-ttu-id="9fa25-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9fa25-102">SYNOPSIS</span></span>
<span data-ttu-id="9fa25-103">Atualiza o estado de uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="9fa25-103">Updates the state of an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9fa25-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9fa25-104">SYNTAX</span></span>

### <span data-ttu-id="9fa25-105">ResourceGroupNameParameterSetName (padrão)</span><span class="sxs-lookup"><span data-stu-id="9fa25-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Update-AzureRmVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 [-OsDiskWriteAccelerator <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9fa25-106">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="9fa25-106">AssignIdentityParameterSet</span></span>
```
Update-AzureRmVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-AssignIdentity]
 [-OsDiskWriteAccelerator <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9fa25-107">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="9fa25-107">ExplicitIdentityParameterSet</span></span>
```
Update-AzureRmVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsDiskWriteAccelerator <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fa25-108">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="9fa25-108">IdParameterSetName</span></span>
```
Update-AzureRmVM [-Id] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-OsDiskWriteAccelerator <Boolean>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9fa25-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9fa25-109">DESCRIPTION</span></span>
<span data-ttu-id="9fa25-110">O cmdlet **Update-AzureRmVM** atualiza o estado de uma máquina virtual do Azure para o estado de um objeto de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9fa25-110">The **Update-AzureRmVM** cmdlet updates the state of an Azure virtual machine to the state of a virtual machine object.</span></span>

## <span data-ttu-id="9fa25-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9fa25-111">EXAMPLES</span></span>

### <span data-ttu-id="9fa25-112">Exemplo 1: atualizar uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="9fa25-112">Example 1: Update a virtual machine</span></span>
```
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="9fa25-113">Esse comando atualiza a máquina virtual, $VirtualMachine, no ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="9fa25-113">This command updates the virtual machine, $VirtualMachine, in ResourceGroup11.</span></span>
<span data-ttu-id="9fa25-114">O comando atualiza-o usando o objeto da máquina virtual armazenado na variável $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="9fa25-114">The command updates it by using the virtual machine object stored in the $VirtualMachine variable.</span></span>
<span data-ttu-id="9fa25-115">Para obter um objeto de máquina virtual, use o cmdlet **Get-AzureRmVM** .</span><span class="sxs-lookup"><span data-stu-id="9fa25-115">To obtain a virtual machine object, use the **Get-AzureRmVM** cmdlet.</span></span>

## <span data-ttu-id="9fa25-116">OS</span><span class="sxs-lookup"><span data-stu-id="9fa25-116">PARAMETERS</span></span>

### <span data-ttu-id="9fa25-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9fa25-117">-AsJob</span></span>
<span data-ttu-id="9fa25-118">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="9fa25-118">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="9fa25-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="9fa25-119">-AssignIdentity</span></span>
<span data-ttu-id="9fa25-120">Especifique a identidade atribuída ao sistema para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9fa25-120">Specify the system assigned identity for the virtual machine.</span></span>

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

### <span data-ttu-id="9fa25-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fa25-121">-DefaultProfile</span></span>
<span data-ttu-id="9fa25-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9fa25-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9fa25-123">-ID</span><span class="sxs-lookup"><span data-stu-id="9fa25-123">-Id</span></span>
<span data-ttu-id="9fa25-124">Especifica a ID do recurso da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9fa25-124">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="9fa25-125">-Identityid</span><span class="sxs-lookup"><span data-stu-id="9fa25-125">-IdentityId</span></span>
<span data-ttu-id="9fa25-126">Especifica a lista de identidades de usuário associadas ao conjunto de escalas da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9fa25-126">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="9fa25-127">As referências de identidade do usuário serão identificadores de recurso ARM no formato: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="9fa25-127">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="9fa25-128">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="9fa25-128">-IdentityType</span></span>
<span data-ttu-id="9fa25-129">O tipo de identidade usado para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9fa25-129">The type of identity used for the virtual machine.</span></span> <span data-ttu-id="9fa25-130">Atualmente, o único tipo com suporte é ' SystemAssigned ', que implicitamente cria uma identidade.</span><span class="sxs-lookup"><span data-stu-id="9fa25-130">Currently, the only supported type is 'SystemAssigned', which implicitly creates an identity.</span></span>

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

### <span data-ttu-id="9fa25-131">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="9fa25-131">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="9fa25-132">Especifica se o WriteAccelerator deve ser habilitado ou desabilitado no disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="9fa25-132">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="9fa25-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fa25-133">-ResourceGroupName</span></span>
<span data-ttu-id="9fa25-134">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9fa25-134">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="9fa25-135">-Marca</span><span class="sxs-lookup"><span data-stu-id="9fa25-135">-Tag</span></span>
<span data-ttu-id="9fa25-136">Especifica os recursos e grupos de recursos que podem ser marcados com um conjunto de pares de nome-valor.</span><span class="sxs-lookup"><span data-stu-id="9fa25-136">Specifies the resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="9fa25-137">Adicionar marcas a recursos permite que você agrupe recursos em grupos de recursos e crie seus próprios modos de exibição.</span><span class="sxs-lookup"><span data-stu-id="9fa25-137">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="9fa25-138">Cada recurso ou grupo de recursos pode ter no máximo 15 marcas.</span><span class="sxs-lookup"><span data-stu-id="9fa25-138">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="9fa25-139">-VM</span><span class="sxs-lookup"><span data-stu-id="9fa25-139">-VM</span></span>
<span data-ttu-id="9fa25-140">Especifica um objeto de máquina virtual local.</span><span class="sxs-lookup"><span data-stu-id="9fa25-140">Specifies a local virtual machine object.</span></span>
<span data-ttu-id="9fa25-141">Para obter um objeto de máquina virtual, use o cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="9fa25-141">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="9fa25-142">Esse objeto da máquina virtual contém o estado atualizado para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9fa25-142">This virtual machine object contains the updated state for the virtual machine.</span></span>

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

### <span data-ttu-id="9fa25-143">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9fa25-143">-Confirm</span></span>
<span data-ttu-id="9fa25-144">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9fa25-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9fa25-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fa25-145">-WhatIf</span></span>
<span data-ttu-id="9fa25-146">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9fa25-146">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="9fa25-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9fa25-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9fa25-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fa25-148">CommonParameters</span></span>
<span data-ttu-id="9fa25-149">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fa25-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fa25-150">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fa25-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fa25-151">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9fa25-151">INPUTS</span></span>

### <span data-ttu-id="9fa25-152">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="9fa25-152">PSVirtualMachine</span></span>
<span data-ttu-id="9fa25-153">O parâmetro ' VM ' aceita o valor do tipo ' PSVirtualMachine ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="9fa25-153">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="9fa25-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9fa25-154">OUTPUTS</span></span>

### <span data-ttu-id="9fa25-155">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="9fa25-155">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="9fa25-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9fa25-156">NOTES</span></span>

## <span data-ttu-id="9fa25-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9fa25-157">RELATED LINKS</span></span>

[<span data-ttu-id="9fa25-158">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9fa25-158">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="9fa25-159">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9fa25-159">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="9fa25-160">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9fa25-160">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="9fa25-161">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9fa25-161">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="9fa25-162">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9fa25-162">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="9fa25-163">Parar-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9fa25-163">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="9fa25-164">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="9fa25-164">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)


