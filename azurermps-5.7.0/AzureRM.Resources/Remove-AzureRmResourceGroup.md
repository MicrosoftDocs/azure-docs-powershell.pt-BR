---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 880D321E-30F2-4CAE-B14A-5F6DD8E1DB99
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroup.md
ms.openlocfilehash: ce028e52d893372f4a668a278466d4cdc51655f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431621"
---
# <span data-ttu-id="20311-101">Remove-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="20311-101">Remove-AzureRmResourceGroup</span></span>

## <span data-ttu-id="20311-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="20311-102">SYNOPSIS</span></span>
<span data-ttu-id="20311-103">Remove um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="20311-103">Removes a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20311-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="20311-104">SYNTAX</span></span>

### <span data-ttu-id="20311-105">RemoveByResourceGroupName (padrão)</span><span class="sxs-lookup"><span data-stu-id="20311-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzureRmResourceGroup [-Name] <String> [-Force] [-AsJob] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20311-106">RemoveByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="20311-106">RemoveByResourceGroupId</span></span>
```
Remove-AzureRmResourceGroup [-Id] <String> [-Force] [-AsJob] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20311-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="20311-107">DESCRIPTION</span></span>
<span data-ttu-id="20311-108">O cmdlet **Remove-AzureRmResourceGroup** remove um grupo de recursos do Azure e seus recursos da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="20311-108">The **Remove-AzureRmResourceGroup** cmdlet removes an Azure resource group and its resources from the current subscription.</span></span>
<span data-ttu-id="20311-109">Para excluir um recurso, mas deixe o grupo de recursos, use o cmdlet Remove-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="20311-109">To delete a resource, but leave the resource group, use the Remove-AzureRmResource cmdlet.</span></span>

## <span data-ttu-id="20311-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="20311-110">EXAMPLES</span></span>

### <span data-ttu-id="20311-111">Exemplo 1: remover um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="20311-111">Example 1: Remove a resource group</span></span>
```
PS C:\>Remove-AzureRmResourceGroup -Name "ContosoRG01"
```

<span data-ttu-id="20311-112">Este comando Remove o grupo de recursos ContosoRG01 da assinatura.</span><span class="sxs-lookup"><span data-stu-id="20311-112">This command removes the ContosoRG01 resource group from the subscription.</span></span>
<span data-ttu-id="20311-113">O cmdlet solicita confirmação e não retorna nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="20311-113">The cmdlet prompts you for confirmation and returns no output.</span></span>

### <span data-ttu-id="20311-114">Exemplo 2: remover um grupo de recursos sem confirmação</span><span class="sxs-lookup"><span data-stu-id="20311-114">Example 2: Remove a resource group without confirmation</span></span>
```
PS C:\>Get-AzureRmResourceGroup -Name "ContosoRG01" | Remove-AzureRmResourceGroup -Verbose -Force
```

<span data-ttu-id="20311-115">Esse comando usa o cmdlet Get-AzureRmResourceGroup para obter a ContosoRG01 do grupo de recursos e, em seguida, passa-a para **Remove-AzureRmResourceGroup** usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="20311-115">This command uses the Get-AzureRmResourceGroup cmdlet to get the resource group ContosoRG01, and then passes it to **Remove-AzureRmResourceGroup** by using the pipeline operator.</span></span>
<span data-ttu-id="20311-116">O parâmetro comum *Verbose* Obtém informações de status sobre a operação, e o parâmetro *Force* suprime o prompt de confirmação.</span><span class="sxs-lookup"><span data-stu-id="20311-116">The *Verbose* common parameter gets status information about the operation, and the *Force* parameter suppresses the confirmation prompt.</span></span>

### <span data-ttu-id="20311-117">Exemplo 3: remover todos os grupos de recursos</span><span class="sxs-lookup"><span data-stu-id="20311-117">Example 3: Remove all resource groups</span></span>
```
PS C:\>Get-AzureRmResourceGroup | Remove-AzureRmResourceGroup
```

<span data-ttu-id="20311-118">Esse comando usa o cmdlet **Get-AzureRmResourceGroup** para obter todos os grupos de recursos e, em seguida, passa-os para **Remove-AzureRmResourceGroup** usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="20311-118">This command uses the **Get-AzureRmResourceGroup** cmdlet to get all resource groups, and then passes them to **Remove-AzureRmResourceGroup** by using the pipeline operator.</span></span>

## <span data-ttu-id="20311-119">OS</span><span class="sxs-lookup"><span data-stu-id="20311-119">PARAMETERS</span></span>

### <span data-ttu-id="20311-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="20311-120">-ApiVersion</span></span>
<span data-ttu-id="20311-121">Especifica a versão da API que é suportada pelo provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="20311-121">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="20311-122">Você pode especificar uma versão diferente da versão padrão.</span><span class="sxs-lookup"><span data-stu-id="20311-122">You can specify a different version than the default version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20311-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="20311-123">-AsJob</span></span>
<span data-ttu-id="20311-124">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="20311-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="20311-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20311-125">-DefaultProfile</span></span>
<span data-ttu-id="20311-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="20311-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="20311-127">-Force</span><span class="sxs-lookup"><span data-stu-id="20311-127">-Force</span></span>
<span data-ttu-id="20311-128">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="20311-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="20311-129">-ID</span><span class="sxs-lookup"><span data-stu-id="20311-129">-Id</span></span>
<span data-ttu-id="20311-130">Especifica a ID do grupo de recursos a ser removida.</span><span class="sxs-lookup"><span data-stu-id="20311-130">Specifies the ID of resource group to remove.</span></span>
<span data-ttu-id="20311-131">Caracteres curinga não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="20311-131">Wildcard characters are not permitted.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20311-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="20311-132">-Name</span></span>
<span data-ttu-id="20311-133">Especifica os nomes dos grupos de recursos a serem removidos.</span><span class="sxs-lookup"><span data-stu-id="20311-133">Specifies the names of resource groups to remove.</span></span>
<span data-ttu-id="20311-134">Caracteres curinga não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="20311-134">Wildcard characters are not permitted.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByResourceGroupName
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20311-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="20311-135">-Pre</span></span>
<span data-ttu-id="20311-136">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="20311-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="20311-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="20311-137">-Confirm</span></span>
<span data-ttu-id="20311-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20311-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20311-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20311-139">-WhatIf</span></span>
<span data-ttu-id="20311-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="20311-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20311-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="20311-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20311-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20311-142">CommonParameters</span></span>
<span data-ttu-id="20311-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20311-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20311-144">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20311-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20311-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="20311-145">INPUTS</span></span>

### <span data-ttu-id="20311-146">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="20311-146">None</span></span>

## <span data-ttu-id="20311-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="20311-147">OUTPUTS</span></span>

### <span data-ttu-id="20311-148">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="20311-148">None</span></span>

## <span data-ttu-id="20311-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="20311-149">NOTES</span></span>

## <span data-ttu-id="20311-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="20311-150">RELATED LINKS</span></span>

[<span data-ttu-id="20311-151">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="20311-151">Get-AzureRmResourceGroup</span></span>](./Get-AzureRmResourceGroup.md)

[<span data-ttu-id="20311-152">New-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="20311-152">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="20311-153">Set-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="20311-153">Set-AzureRmResourceGroup</span></span>](./Set-AzureRmResourceGroup.md)


