---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagedApplication.md
ms.openlocfilehash: 75e750aa13df16deb5c281a5914a6c21a1740e88
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610186"
---
# <span data-ttu-id="22de6-101">Remove-AzureRmManagedApplication</span><span class="sxs-lookup"><span data-stu-id="22de6-101">Remove-AzureRmManagedApplication</span></span>

## <span data-ttu-id="22de6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="22de6-102">SYNOPSIS</span></span>
<span data-ttu-id="22de6-103">Remove um aplicativo gerenciado</span><span class="sxs-lookup"><span data-stu-id="22de6-103">Removes a managed application</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22de6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="22de6-104">SYNTAX</span></span>

### <span data-ttu-id="22de6-105">O conjunto de parâmetros de nome do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="22de6-105">The managed application name parameter set.</span></span> <span data-ttu-id="22de6-106">Assume</span><span class="sxs-lookup"><span data-stu-id="22de6-106">(Default)</span></span>
```
Remove-AzureRmManagedApplication -Name <String> -ResourceGroupName <String> [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22de6-107">O conjunto de parâmetros de ID do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="22de6-107">The managed application Id parameter set.</span></span>
```
Remove-AzureRmManagedApplication -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22de6-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="22de6-108">DESCRIPTION</span></span>
<span data-ttu-id="22de6-109">O cmdlet **Remove-AzureRmManagedApplication** remove um aplicativo gerenciado</span><span class="sxs-lookup"><span data-stu-id="22de6-109">The **Remove-AzureRmManagedApplication** cmdlet removes a managed application</span></span>

## <span data-ttu-id="22de6-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="22de6-110">EXAMPLES</span></span>

### <span data-ttu-id="22de6-111">Exemplo 1: remover o aplicativo gerenciado por ID do recurso</span><span class="sxs-lookup"><span data-stu-id="22de6-111">Example 1: Remove managed application by resource ID</span></span>
```
PS C:\>$Application = Get-AzureRmManagedApplication -Name "myApp" -ResourceGroupName "myRG"
PS C:\>Remove-AzureRmManagedApplication -Id $Application.ResourceId -Force
```

<span data-ttu-id="22de6-112">O primeiro comando obtém um aplicativo gerenciado chamado myApp usando o cmdlet Get-AzureRmManagedApplication.</span><span class="sxs-lookup"><span data-stu-id="22de6-112">The first command gets a managed application named myApp by using the Get-AzureRmManagedApplication cmdlet.</span></span>
<span data-ttu-id="22de6-113">O comando o armazena na variável $Application.</span><span class="sxs-lookup"><span data-stu-id="22de6-113">The command stores it in the $Application variable.</span></span>

<span data-ttu-id="22de6-114">O segundo comando Remove o aplicativo gerenciado identificado pela propriedade **ResourceId** de $Application.</span><span class="sxs-lookup"><span data-stu-id="22de6-114">The second command removes the managed application identified by the **ResourceId** property of $Application.</span></span>

## <span data-ttu-id="22de6-115">OS</span><span class="sxs-lookup"><span data-stu-id="22de6-115">PARAMETERS</span></span>

### <span data-ttu-id="22de6-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="22de6-116">-ApiVersion</span></span>
<span data-ttu-id="22de6-117">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="22de6-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="22de6-118">Se não for especificado, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="22de6-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="22de6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22de6-119">-DefaultProfile</span></span>
<span data-ttu-id="22de6-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="22de6-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22de6-121">-Force</span><span class="sxs-lookup"><span data-stu-id="22de6-121">-Force</span></span>
<span data-ttu-id="22de6-122">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="22de6-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="22de6-123">-ID</span><span class="sxs-lookup"><span data-stu-id="22de6-123">-Id</span></span>
<span data-ttu-id="22de6-124">A ID de aplicativo gerenciada totalmente qualificada, incluindo a assinatura.</span><span class="sxs-lookup"><span data-stu-id="22de6-124">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="22de6-125">por exemplo,/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="22de6-125">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22de6-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="22de6-126">-Name</span></span>
<span data-ttu-id="22de6-127">O nome do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="22de6-127">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22de6-128">-Pre</span><span class="sxs-lookup"><span data-stu-id="22de6-128">-Pre</span></span>
<span data-ttu-id="22de6-129">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="22de6-129">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="22de6-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22de6-130">-ResourceGroupName</span></span>
<span data-ttu-id="22de6-131">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="22de6-131">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22de6-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="22de6-132">-Confirm</span></span>
<span data-ttu-id="22de6-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22de6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22de6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22de6-134">-WhatIf</span></span>
<span data-ttu-id="22de6-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="22de6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22de6-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="22de6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22de6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22de6-137">CommonParameters</span></span>
<span data-ttu-id="22de6-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22de6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22de6-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22de6-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22de6-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="22de6-140">INPUTS</span></span>

### <span data-ttu-id="22de6-141">System. String</span><span class="sxs-lookup"><span data-stu-id="22de6-141">System.String</span></span>

## <span data-ttu-id="22de6-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="22de6-142">OUTPUTS</span></span>

### <span data-ttu-id="22de6-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="22de6-143">System.Boolean</span></span>

## <span data-ttu-id="22de6-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="22de6-144">NOTES</span></span>

## <span data-ttu-id="22de6-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="22de6-145">RELATED LINKS</span></span>

