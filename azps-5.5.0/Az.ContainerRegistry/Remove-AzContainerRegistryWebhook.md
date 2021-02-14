---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryWebhook.md
ms.openlocfilehash: 4064728aeffb53fe9f6065d295455738b6a0f046
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115939"
---
# <span data-ttu-id="fff1c-101">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="fff1c-101">Remove-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="fff1c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fff1c-102">SYNOPSIS</span></span>
<span data-ttu-id="fff1c-103">Remove um contêiner da Web de registro.</span><span class="sxs-lookup"><span data-stu-id="fff1c-103">Removes a container registry webhook.</span></span>

## <span data-ttu-id="fff1c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fff1c-104">SYNTAX</span></span>

### <span data-ttu-id="fff1c-105">NameResourceGroupParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="fff1c-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fff1c-106">WebbjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fff1c-106">WebhookObjectParameterSet</span></span>
```
Remove-AzContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fff1c-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fff1c-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistryWebhook -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fff1c-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="fff1c-108">DESCRIPTION</span></span>
<span data-ttu-id="fff1c-109">O Remove-AzContainerRegistryWebhook cmdlet remove um web registry de contêiner.</span><span class="sxs-lookup"><span data-stu-id="fff1c-109">The Remove-AzContainerRegistryWebhook cmdlet removes a container registry webhook.</span></span>

## <span data-ttu-id="fff1c-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fff1c-110">EXAMPLES</span></span>

### <span data-ttu-id="fff1c-111">Exemplo 1: Remover um contêiner web browser do registro.</span><span class="sxs-lookup"><span data-stu-id="fff1c-111">Example 1: Remove a container registry webhook.</span></span>
```powershell
PS C:\> Remove-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"
```

<span data-ttu-id="fff1c-112">Remove um contêiner da Web de registro.</span><span class="sxs-lookup"><span data-stu-id="fff1c-112">Removes a container registry webhook.</span></span>

## <span data-ttu-id="fff1c-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fff1c-113">PARAMETERS</span></span>

### <span data-ttu-id="fff1c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fff1c-114">-DefaultProfile</span></span>
<span data-ttu-id="fff1c-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="fff1c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fff1c-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="fff1c-116">-Name</span></span>
<span data-ttu-id="fff1c-117">Nome Web browser.</span><span class="sxs-lookup"><span data-stu-id="fff1c-117">Webhook Name.</span></span>

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

### <span data-ttu-id="fff1c-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fff1c-118">-PassThru</span></span>
<span data-ttu-id="fff1c-119">Indica que esse cmdlet retornará verdadeiro se a remoção tiver sido bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="fff1c-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="fff1c-120">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="fff1c-120">-RegistryName</span></span>
<span data-ttu-id="fff1c-121">Nome do Registro do Contêiner.</span><span class="sxs-lookup"><span data-stu-id="fff1c-121">Container Registry Name.</span></span>

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

### <span data-ttu-id="fff1c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fff1c-122">-ResourceGroupName</span></span>
<span data-ttu-id="fff1c-123">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fff1c-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="fff1c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fff1c-124">-ResourceId</span></span>
<span data-ttu-id="fff1c-125">A ID de recurso Web browser do registro de contêineres</span><span class="sxs-lookup"><span data-stu-id="fff1c-125">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="fff1c-126">-Web browser</span><span class="sxs-lookup"><span data-stu-id="fff1c-126">-Webhook</span></span>
<span data-ttu-id="fff1c-127">Objeto do Registro de Contêineres.</span><span class="sxs-lookup"><span data-stu-id="fff1c-127">Container Registry Object.</span></span>

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

### <span data-ttu-id="fff1c-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="fff1c-128">-Confirm</span></span>
<span data-ttu-id="fff1c-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fff1c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fff1c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fff1c-130">-WhatIf</span></span>
<span data-ttu-id="fff1c-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="fff1c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fff1c-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fff1c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fff1c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fff1c-133">CommonParameters</span></span>
<span data-ttu-id="fff1c-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fff1c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fff1c-135">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fff1c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fff1c-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="fff1c-136">INPUTS</span></span>

### <span data-ttu-id="fff1c-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebweb</span><span class="sxs-lookup"><span data-stu-id="fff1c-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

### <span data-ttu-id="fff1c-138">System.String</span><span class="sxs-lookup"><span data-stu-id="fff1c-138">System.String</span></span>

## <span data-ttu-id="fff1c-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="fff1c-139">OUTPUTS</span></span>

### <span data-ttu-id="fff1c-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fff1c-140">System.Boolean</span></span>

## <span data-ttu-id="fff1c-141">Notas</span><span class="sxs-lookup"><span data-stu-id="fff1c-141">NOTES</span></span>

## <span data-ttu-id="fff1c-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fff1c-142">RELATED LINKS</span></span>

[<span data-ttu-id="fff1c-143">New-AzContainerRegistryWebweb</span><span class="sxs-lookup"><span data-stu-id="fff1c-143">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="fff1c-144">Get-AzContainerRegistryWebweb</span><span class="sxs-lookup"><span data-stu-id="fff1c-144">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="fff1c-145">Update-AzContainerRegistryWebweb</span><span class="sxs-lookup"><span data-stu-id="fff1c-145">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="fff1c-146">Test-AzContainerRegistryWebweb</span><span class="sxs-lookup"><span data-stu-id="fff1c-146">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)