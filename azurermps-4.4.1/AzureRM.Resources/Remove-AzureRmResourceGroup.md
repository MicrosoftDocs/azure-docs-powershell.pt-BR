---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 880D321E-30F2-4CAE-B14A-5F6DD8E1DB99
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroup.md
ms.openlocfilehash: 6938cf80f3fa6fb20252e1e4a212133ecd1c62a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432557"
---
# <span data-ttu-id="6c7f5-101">Remove-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6c7f5-101">Remove-AzureRmResourceGroup</span></span>

## <span data-ttu-id="6c7f5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6c7f5-102">SYNOPSIS</span></span>
<span data-ttu-id="6c7f5-103">Remove um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6c7f5-103">Removes a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c7f5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6c7f5-104">SYNTAX</span></span>

### <span data-ttu-id="6c7f5-105">Lista o grupo de recursos com base no nome.</span><span class="sxs-lookup"><span data-stu-id="6c7f5-105">Lists the resource group based in the name.</span></span> <span data-ttu-id="6c7f5-106">Assume</span><span class="sxs-lookup"><span data-stu-id="6c7f5-106">(Default)</span></span>
```
Remove-AzureRmResourceGroup [-Name] <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c7f5-107">Lista o grupo de recursos com base na ID.</span><span class="sxs-lookup"><span data-stu-id="6c7f5-107">Lists the resource group based in the Id.</span></span>
```
Remove-AzureRmResourceGroup [-Id] <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c7f5-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6c7f5-108">DESCRIPTION</span></span>
<span data-ttu-id="6c7f5-109">O cmdlet **Remove-AzureRmResourceGroup** remove um grupo de recursos do Azure e seus recursos da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="6c7f5-109">The **Remove-AzureRmResourceGroup** cmdlet removes an Azure resource group and its resources from the current subscription.</span></span>
<span data-ttu-id="6c7f5-110">Para excluir um recurso, mas deixe o grupo de recursos, use o cmdlet Remove-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="6c7f5-110">To delete a resource, but leave the resource group, use the Remove-AzureRmResource cmdlet.</span></span>

## <span data-ttu-id="6c7f5-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6c7f5-111">EXAMPLES</span></span>

### <span data-ttu-id="6c7f5-112">Exemplo 1: remover um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="6c7f5-112">Example 1: Remove a resource group</span></span>
```
PS C:\>Remove-AzureRmResourceGroup -Name "ContosoRG01"
```

<span data-ttu-id="6c7f5-113">Este comando Remove o grupo de recursos ContosoRG01 da assinatura.</span><span class="sxs-lookup"><span data-stu-id="6c7f5-113">This command removes the ContosoRG01 resource group from the subscription.</span></span>
<span data-ttu-id="6c7f5-114">O cmdlet solicita confirmação e não retorna nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="6c7f5-114">The cmdlet prompts you for confirmation and returns no output.</span></span>

### <span data-ttu-id="6c7f5-115">Exemplo 2: remover um grupo de recursos sem confirmação</span><span class="sxs-lookup"><span data-stu-id="6c7f5-115">Example 2: Remove a resource group without confirmation</span></span>
```
PS C:\>Get-AzureRmResourceGroup -Name "ContosoRG01" | Remove-AzureRmResourceGroup -Verbose -Force
```

<span data-ttu-id="6c7f5-116">Esse comando usa o cmdlet Get-AzureRmResourceGroup para obter a ContosoRG01 do grupo de recursos e, em seguida, passa-a para **Remove-AzureRmResourceGroup** usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="6c7f5-116">This command uses the Get-AzureRmResourceGroup cmdlet to get the resource group ContosoRG01, and then passes it to **Remove-AzureRmResourceGroup** by using the pipeline operator.</span></span>
<span data-ttu-id="6c7f5-117">O parâmetro comum *Verbose* Obtém informações de status sobre a operação, e o parâmetro *Force* suprime o prompt de confirmação.</span><span class="sxs-lookup"><span data-stu-id="6c7f5-117">The *Verbose* common parameter gets status information about the operation, and the *Force* parameter suppresses the confirmation prompt.</span></span>

### <span data-ttu-id="6c7f5-118">Exemplo 3: remover todos os grupos de recursos</span><span class="sxs-lookup"><span data-stu-id="6c7f5-118">Example 3: Remove all resource groups</span></span>
```
PS C:\>Get-AzureRmResourceGroup | Remove-AzureRmResourceGroup
```

<span data-ttu-id="6c7f5-119">Esse comando usa o cmdlet **Get-AzureRmResourceGroup** para obter todos os grupos de recursos e, em seguida, passa-os para **Remove-AzureRmResourceGroup** usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="6c7f5-119">This command uses the **Get-AzureRmResourceGroup** cmdlet to get all resource groups, and then passes them to **Remove-AzureRmResourceGroup** by using the pipeline operator.</span></span>

## <span data-ttu-id="6c7f5-120">OS</span><span class="sxs-lookup"><span data-stu-id="6c7f5-120">PARAMETERS</span></span>

### <span data-ttu-id="6c7f5-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6c7f5-121">-ApiVersion</span></span>
<span data-ttu-id="6c7f5-122">Especifica a versão da API que é suportada pelo provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="6c7f5-122">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="6c7f5-123">Você pode especificar uma versão diferente da versão padrão.</span><span class="sxs-lookup"><span data-stu-id="6c7f5-123">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="6c7f5-124">-Force</span><span class="sxs-lookup"><span data-stu-id="6c7f5-124">-Force</span></span>
<span data-ttu-id="6c7f5-125">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="6c7f5-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6c7f5-126">-ID</span><span class="sxs-lookup"><span data-stu-id="6c7f5-126">-Id</span></span>
<span data-ttu-id="6c7f5-127">Especifica a ID do grupo de recursos a ser removida.</span><span class="sxs-lookup"><span data-stu-id="6c7f5-127">Specifies the ID of resource group to remove.</span></span>
<span data-ttu-id="6c7f5-128">Caracteres curinga não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="6c7f5-128">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resource group based in the Id.
Aliases: ResourceGroupId, ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c7f5-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="6c7f5-129">-Name</span></span>
<span data-ttu-id="6c7f5-130">Especifica os nomes dos grupos de recursos a serem removidos.</span><span class="sxs-lookup"><span data-stu-id="6c7f5-130">Specifies the names of resource groups to remove.</span></span>
<span data-ttu-id="6c7f5-131">Caracteres curinga não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="6c7f5-131">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resource group based in the name.
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c7f5-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="6c7f5-132">-Pre</span></span>
<span data-ttu-id="6c7f5-133">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="6c7f5-133">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="6c7f5-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6c7f5-134">-Confirm</span></span>
<span data-ttu-id="6c7f5-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c7f5-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c7f5-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c7f5-136">-WhatIf</span></span>
<span data-ttu-id="6c7f5-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6c7f5-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c7f5-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6c7f5-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c7f5-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c7f5-139">-DefaultProfile</span></span>
<span data-ttu-id="6c7f5-140">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6c7f5-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6c7f5-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c7f5-141">CommonParameters</span></span>
<span data-ttu-id="6c7f5-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c7f5-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c7f5-143">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c7f5-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c7f5-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6c7f5-144">INPUTS</span></span>

### <span data-ttu-id="6c7f5-145">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="6c7f5-145">None</span></span>

## <span data-ttu-id="6c7f5-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6c7f5-146">OUTPUTS</span></span>

### <span data-ttu-id="6c7f5-147">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="6c7f5-147">None</span></span>

## <span data-ttu-id="6c7f5-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6c7f5-148">NOTES</span></span>

## <span data-ttu-id="6c7f5-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6c7f5-149">RELATED LINKS</span></span>

[<span data-ttu-id="6c7f5-150">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6c7f5-150">Get-AzureRmResourceGroup</span></span>](./Get-AzureRmResourceGroup.md)

[<span data-ttu-id="6c7f5-151">New-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6c7f5-151">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="6c7f5-152">Set-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6c7f5-152">Set-AzureRmResourceGroup</span></span>](./Set-AzureRmResourceGroup.md)


