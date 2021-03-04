---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/remove-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryWebhook.md
ms.openlocfilehash: e189be8f04081bbc51c5cc19b981c164ce4e9c2c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885935"
---
# <span data-ttu-id="db64d-101">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="db64d-101">Remove-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="db64d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db64d-102">SYNOPSIS</span></span>
<span data-ttu-id="db64d-103">Remove um webhook de registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="db64d-103">Removes a container registry webhook.</span></span>

## <span data-ttu-id="db64d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="db64d-104">SYNTAX</span></span>

### <span data-ttu-id="db64d-105">NameResourceGroupParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="db64d-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db64d-106">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="db64d-106">WebhookObjectParameterSet</span></span>
```
Remove-AzContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db64d-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="db64d-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistryWebhook -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db64d-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="db64d-108">DESCRIPTION</span></span>
<span data-ttu-id="db64d-109">O Remove-AzContainerRegistryWebhook cmdlet remove um webhook de registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="db64d-109">The Remove-AzContainerRegistryWebhook cmdlet removes a container registry webhook.</span></span>

## <span data-ttu-id="db64d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="db64d-110">EXAMPLES</span></span>

### <span data-ttu-id="db64d-111">Exemplo 1: Remover um webhook de registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="db64d-111">Example 1: Remove a container registry webhook.</span></span>
```powershell
PS C:\> Remove-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"
```

<span data-ttu-id="db64d-112">Remove um webhook de registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="db64d-112">Removes a container registry webhook.</span></span>

## <span data-ttu-id="db64d-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="db64d-113">PARAMETERS</span></span>

### <span data-ttu-id="db64d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db64d-114">-DefaultProfile</span></span>
<span data-ttu-id="db64d-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="db64d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db64d-116">-Name</span><span class="sxs-lookup"><span data-stu-id="db64d-116">-Name</span></span>
<span data-ttu-id="db64d-117">Nome do webhook.</span><span class="sxs-lookup"><span data-stu-id="db64d-117">Webhook Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: WebhookName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db64d-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="db64d-118">-PassThru</span></span>
<span data-ttu-id="db64d-119">Indica que esse cmdlet retornará true se a remoção tiver sido bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="db64d-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="db64d-120">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="db64d-120">-RegistryName</span></span>
<span data-ttu-id="db64d-121">Nome do Registro do Contêiner.</span><span class="sxs-lookup"><span data-stu-id="db64d-121">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db64d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db64d-122">-ResourceGroupName</span></span>
<span data-ttu-id="db64d-123">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="db64d-123">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db64d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="db64d-124">-ResourceId</span></span>
<span data-ttu-id="db64d-125">A ID do recurso Webhook do registro de contêiner</span><span class="sxs-lookup"><span data-stu-id="db64d-125">The container registry Webhook resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db64d-126">-Webhook</span><span class="sxs-lookup"><span data-stu-id="db64d-126">-Webhook</span></span>
<span data-ttu-id="db64d-127">Objeto Container Registry.</span><span class="sxs-lookup"><span data-stu-id="db64d-127">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook
Parameter Sets: WebhookObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db64d-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="db64d-128">-Confirm</span></span>
<span data-ttu-id="db64d-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db64d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db64d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db64d-130">-WhatIf</span></span>
<span data-ttu-id="db64d-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="db64d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db64d-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="db64d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db64d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db64d-133">CommonParameters</span></span>
<span data-ttu-id="db64d-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db64d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db64d-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="db64d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db64d-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="db64d-136">INPUTS</span></span>

### <span data-ttu-id="db64d-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="db64d-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

### <span data-ttu-id="db64d-138">System.String</span><span class="sxs-lookup"><span data-stu-id="db64d-138">System.String</span></span>

## <span data-ttu-id="db64d-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="db64d-139">OUTPUTS</span></span>

### <span data-ttu-id="db64d-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="db64d-140">System.Boolean</span></span>

## <span data-ttu-id="db64d-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="db64d-141">NOTES</span></span>

## <span data-ttu-id="db64d-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="db64d-142">RELATED LINKS</span></span>

[<span data-ttu-id="db64d-143">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="db64d-143">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="db64d-144">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="db64d-144">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="db64d-145">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="db64d-145">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="db64d-146">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="db64d-146">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)