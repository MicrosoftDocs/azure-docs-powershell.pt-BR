---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 38917534-49C6-47EA-B815-240F794EE655
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVM.md
ms.openlocfilehash: ad337c07f22b2805002347758f91bf0ea781adad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431788"
---
# <span data-ttu-id="e92c1-101">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e92c1-101">Update-AzureRmVM</span></span>

## <span data-ttu-id="e92c1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e92c1-102">SYNOPSIS</span></span>
<span data-ttu-id="e92c1-103">Atualiza o estado de uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="e92c1-103">Updates the state of an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e92c1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e92c1-104">SYNTAX</span></span>

### <span data-ttu-id="e92c1-105">ResourceGroupNameParameterSetName (padrão)</span><span class="sxs-lookup"><span data-stu-id="e92c1-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Update-AzureRmVM -VM <PSVirtualMachine> [-Tags <Hashtable>] [-IdentityType <ResourceIdentityType>]
 [-AssignIdentity] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e92c1-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="e92c1-106">IdParameterSetName</span></span>
```
Update-AzureRmVM -VM <PSVirtualMachine> [-Tags <Hashtable>] [-IdentityType <ResourceIdentityType>]
 [-AssignIdentity] [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e92c1-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e92c1-107">DESCRIPTION</span></span>
<span data-ttu-id="e92c1-108">O cmdlet **Update-AzureRmVM** atualiza o estado de uma máquina virtual do Azure para o estado de um objeto de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e92c1-108">The **Update-AzureRmVM** cmdlet updates the state of an Azure virtual machine to the state of a virtual machine object.</span></span>

## <span data-ttu-id="e92c1-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e92c1-109">EXAMPLES</span></span>

### <span data-ttu-id="e92c1-110">Exemplo 1: atualizar uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="e92c1-110">Example 1: Update a virtual machine</span></span>
```
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="e92c1-111">Esse comando atualiza a máquina virtual, $VirtualMachine, no ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="e92c1-111">This command updates the virtual machine, $VirtualMachine, in ResourceGroup11.</span></span>
<span data-ttu-id="e92c1-112">O comando atualiza-o usando o objeto da máquina virtual armazenado na variável $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="e92c1-112">The command updates it by using the virtual machine object stored in the $VirtualMachine variable.</span></span>
<span data-ttu-id="e92c1-113">Para obter um objeto de máquina virtual, use o cmdlet **Get-AzureRmVM** .</span><span class="sxs-lookup"><span data-stu-id="e92c1-113">To obtain a virtual machine object, use the **Get-AzureRmVM** cmdlet.</span></span>

## <span data-ttu-id="e92c1-114">OS</span><span class="sxs-lookup"><span data-stu-id="e92c1-114">PARAMETERS</span></span>

### <span data-ttu-id="e92c1-115">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="e92c1-115">-AssignIdentity</span></span>
<span data-ttu-id="e92c1-116">Especifique a identidade atribuída ao sistema para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e92c1-116">Specify the system assigned identity for the virtual machine.</span></span>

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

### <span data-ttu-id="e92c1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e92c1-117">-DefaultProfile</span></span>
<span data-ttu-id="e92c1-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e92c1-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e92c1-119">-ID</span><span class="sxs-lookup"><span data-stu-id="e92c1-119">-Id</span></span>
<span data-ttu-id="e92c1-120">Especifica a ID do recurso da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e92c1-120">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="e92c1-121">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="e92c1-121">-IdentityType</span></span>
<span data-ttu-id="e92c1-122">O tipo de identidade usado para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e92c1-122">The type of identity used for the virtual machine.</span></span> <span data-ttu-id="e92c1-123">Atualmente, o único tipo com suporte é ' SystemAssigned ', que implicitamente cria uma identidade.</span><span class="sxs-lookup"><span data-stu-id="e92c1-123">Currently, the only supported type is 'SystemAssigned', which implicitly creates an identity.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: (All)
Aliases: 
Accepted values: SystemAssigned

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e92c1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e92c1-124">-ResourceGroupName</span></span>
<span data-ttu-id="e92c1-125">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e92c1-125">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e92c1-126">-Marcas</span><span class="sxs-lookup"><span data-stu-id="e92c1-126">-Tags</span></span>
<span data-ttu-id="e92c1-127">Especifica os recursos e grupos de recursos que podem ser marcados com um conjunto de pares de nome-valor.</span><span class="sxs-lookup"><span data-stu-id="e92c1-127">Specifies the resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="e92c1-128">Adicionar marcas a recursos permite que você agrupe recursos em grupos de recursos e crie seus próprios modos de exibição.</span><span class="sxs-lookup"><span data-stu-id="e92c1-128">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="e92c1-129">Cada recurso ou grupo de recursos pode ter no máximo 15 marcas.</span><span class="sxs-lookup"><span data-stu-id="e92c1-129">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="e92c1-130">-VM</span><span class="sxs-lookup"><span data-stu-id="e92c1-130">-VM</span></span>
<span data-ttu-id="e92c1-131">Especifica um objeto de máquina virtual local.</span><span class="sxs-lookup"><span data-stu-id="e92c1-131">Specifies a local virtual machine object.</span></span>
<span data-ttu-id="e92c1-132">Para obter um objeto de máquina virtual, use o cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="e92c1-132">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="e92c1-133">Esse objeto da máquina virtual contém o estado atualizado para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e92c1-133">This virtual machine object contains the updated state for the virtual machine.</span></span>

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

### <span data-ttu-id="e92c1-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e92c1-134">-Confirm</span></span>
<span data-ttu-id="e92c1-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e92c1-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e92c1-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e92c1-136">-WhatIf</span></span>
<span data-ttu-id="e92c1-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e92c1-137">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="e92c1-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e92c1-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e92c1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e92c1-139">CommonParameters</span></span>
<span data-ttu-id="e92c1-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e92c1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e92c1-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e92c1-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e92c1-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e92c1-142">INPUTS</span></span>

## <span data-ttu-id="e92c1-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e92c1-143">OUTPUTS</span></span>

## <span data-ttu-id="e92c1-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e92c1-144">NOTES</span></span>

## <span data-ttu-id="e92c1-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e92c1-145">RELATED LINKS</span></span>

[<span data-ttu-id="e92c1-146">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e92c1-146">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="e92c1-147">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e92c1-147">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="e92c1-148">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e92c1-148">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="e92c1-149">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e92c1-149">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="e92c1-150">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e92c1-150">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="e92c1-151">Parar-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e92c1-151">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="e92c1-152">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="e92c1-152">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)


