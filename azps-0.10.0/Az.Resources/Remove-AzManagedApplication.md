---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzManagedApplication.md
ms.openlocfilehash: a1dbab8cdb3416809a7200d91f718475334b2d9c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776356"
---
# <span data-ttu-id="578b1-101">Remove-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="578b1-101">Remove-AzManagedApplication</span></span>

## <span data-ttu-id="578b1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="578b1-102">SYNOPSIS</span></span>
<span data-ttu-id="578b1-103">Remove um aplicativo gerenciado</span><span class="sxs-lookup"><span data-stu-id="578b1-103">Removes a managed application</span></span>

## <span data-ttu-id="578b1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="578b1-104">SYNTAX</span></span>

### <span data-ttu-id="578b1-105">RemoveByNameAndResourceGroup (padrão)</span><span class="sxs-lookup"><span data-stu-id="578b1-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzManagedApplication -Name <String> -ResourceGroupName <String> [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="578b1-106">RemoveById</span><span class="sxs-lookup"><span data-stu-id="578b1-106">RemoveById</span></span>
```
Remove-AzManagedApplication -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="578b1-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="578b1-107">DESCRIPTION</span></span>
<span data-ttu-id="578b1-108">O cmdlet **Remove-AzManagedApplication** remove um aplicativo gerenciado</span><span class="sxs-lookup"><span data-stu-id="578b1-108">The **Remove-AzManagedApplication** cmdlet removes a managed application</span></span>

## <span data-ttu-id="578b1-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="578b1-109">EXAMPLES</span></span>

### <span data-ttu-id="578b1-110">Exemplo 1: remover o aplicativo gerenciado por ID do recurso</span><span class="sxs-lookup"><span data-stu-id="578b1-110">Example 1: Remove managed application by resource ID</span></span>
```
PS C:\>$Application = Get-AzManagedApplication -Name "myApp" -ResourceGroupName "myRG"
PS C:\>Remove-AzManagedApplication -Id $Application.ResourceId -Force
```

<span data-ttu-id="578b1-111">O primeiro comando obtém um aplicativo gerenciado chamado myApp usando o cmdlet Get-AzManagedApplication.</span><span class="sxs-lookup"><span data-stu-id="578b1-111">The first command gets a managed application named myApp by using the Get-AzManagedApplication cmdlet.</span></span>
<span data-ttu-id="578b1-112">O comando o armazena na variável $Application.</span><span class="sxs-lookup"><span data-stu-id="578b1-112">The command stores it in the $Application variable.</span></span>
<span data-ttu-id="578b1-113">O segundo comando Remove o aplicativo gerenciado identificado pela propriedade **ResourceId** de $Application.</span><span class="sxs-lookup"><span data-stu-id="578b1-113">The second command removes the managed application identified by the **ResourceId** property of $Application.</span></span>

## <span data-ttu-id="578b1-114">OS</span><span class="sxs-lookup"><span data-stu-id="578b1-114">PARAMETERS</span></span>

### <span data-ttu-id="578b1-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="578b1-115">-ApiVersion</span></span>
<span data-ttu-id="578b1-116">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="578b1-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="578b1-117">Se não for especificado, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="578b1-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="578b1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="578b1-118">-DefaultProfile</span></span>
<span data-ttu-id="578b1-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="578b1-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="578b1-120">-Force</span><span class="sxs-lookup"><span data-stu-id="578b1-120">-Force</span></span>
<span data-ttu-id="578b1-121">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="578b1-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="578b1-122">-ID</span><span class="sxs-lookup"><span data-stu-id="578b1-122">-Id</span></span>
<span data-ttu-id="578b1-123">A ID de aplicativo gerenciada totalmente qualificada, incluindo a assinatura.</span><span class="sxs-lookup"><span data-stu-id="578b1-123">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="578b1-124">por exemplo,/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="578b1-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="578b1-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="578b1-125">-Name</span></span>
<span data-ttu-id="578b1-126">O nome do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="578b1-126">The managed application name.</span></span>

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

### <span data-ttu-id="578b1-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="578b1-127">-Pre</span></span>
<span data-ttu-id="578b1-128">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="578b1-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="578b1-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="578b1-129">-ResourceGroupName</span></span>
<span data-ttu-id="578b1-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="578b1-130">The resource group name.</span></span>

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

### <span data-ttu-id="578b1-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="578b1-131">-Confirm</span></span>
<span data-ttu-id="578b1-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="578b1-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="578b1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="578b1-133">-WhatIf</span></span>
<span data-ttu-id="578b1-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="578b1-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="578b1-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="578b1-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="578b1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="578b1-136">CommonParameters</span></span>
<span data-ttu-id="578b1-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="578b1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="578b1-138">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="578b1-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="578b1-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="578b1-139">INPUTS</span></span>

### <span data-ttu-id="578b1-140">System. String</span><span class="sxs-lookup"><span data-stu-id="578b1-140">System.String</span></span>

## <span data-ttu-id="578b1-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="578b1-141">OUTPUTS</span></span>

### <span data-ttu-id="578b1-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="578b1-142">System.Boolean</span></span>

## <span data-ttu-id="578b1-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="578b1-143">NOTES</span></span>

## <span data-ttu-id="578b1-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="578b1-144">RELATED LINKS</span></span>
