---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplication.md
ms.openlocfilehash: 17a28da26aa26860b7fd4a28ec922932bb089da3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940795"
---
# <span data-ttu-id="9778d-101">Remove-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="9778d-101">Remove-AzManagedApplication</span></span>

## <span data-ttu-id="9778d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9778d-102">SYNOPSIS</span></span>
<span data-ttu-id="9778d-103">Remove um aplicativo gerenciado</span><span class="sxs-lookup"><span data-stu-id="9778d-103">Removes a managed application</span></span>

## <span data-ttu-id="9778d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9778d-104">SYNTAX</span></span>

### <span data-ttu-id="9778d-105">RemoveByNameAndResourceGroup (padrão)</span><span class="sxs-lookup"><span data-stu-id="9778d-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzManagedApplication -Name <String> -ResourceGroupName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9778d-106">RemoveById</span><span class="sxs-lookup"><span data-stu-id="9778d-106">RemoveById</span></span>
```
Remove-AzManagedApplication -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9778d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9778d-107">DESCRIPTION</span></span>
<span data-ttu-id="9778d-108">O cmdlet **Remove-AzManagedApplication** remove um aplicativo gerenciado</span><span class="sxs-lookup"><span data-stu-id="9778d-108">The **Remove-AzManagedApplication** cmdlet removes a managed application</span></span>

## <span data-ttu-id="9778d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9778d-109">EXAMPLES</span></span>

### <span data-ttu-id="9778d-110">Exemplo 1: remover o aplicativo gerenciado por ID do recurso</span><span class="sxs-lookup"><span data-stu-id="9778d-110">Example 1: Remove managed application by resource ID</span></span>
```
PS C:\>$Application = Get-AzManagedApplication -Name "myApp" -ResourceGroupName "myRG"
PS C:\>Remove-AzManagedApplication -Id $Application.ResourceId -Force
```

<span data-ttu-id="9778d-111">O primeiro comando obtém um aplicativo gerenciado chamado myApp usando o cmdlet Get-AzManagedApplication.</span><span class="sxs-lookup"><span data-stu-id="9778d-111">The first command gets a managed application named myApp by using the Get-AzManagedApplication cmdlet.</span></span>
<span data-ttu-id="9778d-112">O comando o armazena na variável $Application.</span><span class="sxs-lookup"><span data-stu-id="9778d-112">The command stores it in the $Application variable.</span></span>
<span data-ttu-id="9778d-113">O segundo comando Remove o aplicativo gerenciado identificado pela propriedade **ResourceId** de $Application.</span><span class="sxs-lookup"><span data-stu-id="9778d-113">The second command removes the managed application identified by the **ResourceId** property of $Application.</span></span>

## <span data-ttu-id="9778d-114">OS</span><span class="sxs-lookup"><span data-stu-id="9778d-114">PARAMETERS</span></span>

### <span data-ttu-id="9778d-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9778d-115">-ApiVersion</span></span>
<span data-ttu-id="9778d-116">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="9778d-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="9778d-117">Se não for especificado, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="9778d-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="9778d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9778d-118">-DefaultProfile</span></span>
<span data-ttu-id="9778d-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9778d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9778d-120">-Force</span><span class="sxs-lookup"><span data-stu-id="9778d-120">-Force</span></span>
<span data-ttu-id="9778d-121">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="9778d-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="9778d-122">-ID</span><span class="sxs-lookup"><span data-stu-id="9778d-122">-Id</span></span>
<span data-ttu-id="9778d-123">A ID de aplicativo gerenciada totalmente qualificada, incluindo a assinatura.</span><span class="sxs-lookup"><span data-stu-id="9778d-123">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="9778d-124">por exemplo,/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="9778d-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9778d-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="9778d-125">-Name</span></span>
<span data-ttu-id="9778d-126">O nome do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="9778d-126">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9778d-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="9778d-127">-Pre</span></span>
<span data-ttu-id="9778d-128">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="9778d-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="9778d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9778d-129">-ResourceGroupName</span></span>
<span data-ttu-id="9778d-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9778d-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9778d-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9778d-131">-Confirm</span></span>
<span data-ttu-id="9778d-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9778d-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9778d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9778d-133">-WhatIf</span></span>
<span data-ttu-id="9778d-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9778d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9778d-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9778d-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9778d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9778d-136">CommonParameters</span></span>
<span data-ttu-id="9778d-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9778d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9778d-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9778d-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9778d-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9778d-139">INPUTS</span></span>

### <span data-ttu-id="9778d-140">System. String</span><span class="sxs-lookup"><span data-stu-id="9778d-140">System.String</span></span>

## <span data-ttu-id="9778d-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9778d-141">OUTPUTS</span></span>

### <span data-ttu-id="9778d-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9778d-142">System.Boolean</span></span>

## <span data-ttu-id="9778d-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9778d-143">NOTES</span></span>

## <span data-ttu-id="9778d-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9778d-144">RELATED LINKS</span></span>
