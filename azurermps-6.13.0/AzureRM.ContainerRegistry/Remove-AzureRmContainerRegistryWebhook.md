---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/remove-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistryWebhook.md
ms.openlocfilehash: c1ba245f83db386e39f9fecf22f95d3681452d7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610097"
---
# <span data-ttu-id="fba3b-101">Remove-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="fba3b-101">Remove-AzureRmContainerRegistryWebhook</span></span>

## <span data-ttu-id="fba3b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fba3b-102">SYNOPSIS</span></span>
<span data-ttu-id="fba3b-103">Remove um webhook do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="fba3b-103">Removes a container registry webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fba3b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fba3b-104">SYNTAX</span></span>

### <span data-ttu-id="fba3b-105">NameResourceGroupParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="fba3b-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fba3b-106">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fba3b-106">WebhookObjectParameterSet</span></span>
```
Remove-AzureRmContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fba3b-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fba3b-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmContainerRegistryWebhook -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fba3b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fba3b-108">DESCRIPTION</span></span>
<span data-ttu-id="fba3b-109">O cmdlet Remove-AzureRmContainerRegistryWebhook remove um webhook do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="fba3b-109">The Remove-AzureRmContainerRegistryWebhook cmdlet removes a container registry webhook.</span></span>

## <span data-ttu-id="fba3b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fba3b-110">EXAMPLES</span></span>

### <span data-ttu-id="fba3b-111">Exemplo 1: remover um webhook do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="fba3b-111">Example 1: Remove a container registry webhook.</span></span>
```powershell
PS C:\> Remove-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"
```

<span data-ttu-id="fba3b-112">Remove um webhook do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="fba3b-112">Removes a container registry webhook.</span></span>

## <span data-ttu-id="fba3b-113">OS</span><span class="sxs-lookup"><span data-stu-id="fba3b-113">PARAMETERS</span></span>

### <span data-ttu-id="fba3b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fba3b-114">-DefaultProfile</span></span>
<span data-ttu-id="fba3b-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fba3b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fba3b-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="fba3b-116">-Name</span></span>
<span data-ttu-id="fba3b-117">Nome do webhook.</span><span class="sxs-lookup"><span data-stu-id="fba3b-117">Webhook Name.</span></span>

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

### <span data-ttu-id="fba3b-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fba3b-118">-PassThru</span></span>
<span data-ttu-id="fba3b-119">Indica que esse cmdlet retorna true se a remoção tiver sido bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="fba3b-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="fba3b-120">-Registryname</span><span class="sxs-lookup"><span data-stu-id="fba3b-120">-RegistryName</span></span>
<span data-ttu-id="fba3b-121">Nome do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="fba3b-121">Container Registry Name.</span></span>

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

### <span data-ttu-id="fba3b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fba3b-122">-ResourceGroupName</span></span>
<span data-ttu-id="fba3b-123">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fba3b-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="fba3b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fba3b-124">-ResourceId</span></span>
<span data-ttu-id="fba3b-125">A ID do recurso de webhook do registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="fba3b-125">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="fba3b-126">-Webhook</span><span class="sxs-lookup"><span data-stu-id="fba3b-126">-Webhook</span></span>
<span data-ttu-id="fba3b-127">Objeto do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="fba3b-127">Container Registry Object.</span></span>

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

### <span data-ttu-id="fba3b-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fba3b-128">-Confirm</span></span>
<span data-ttu-id="fba3b-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fba3b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fba3b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fba3b-130">-WhatIf</span></span>
<span data-ttu-id="fba3b-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fba3b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fba3b-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fba3b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fba3b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fba3b-133">CommonParameters</span></span>
<span data-ttu-id="fba3b-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fba3b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fba3b-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fba3b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fba3b-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fba3b-136">INPUTS</span></span>

### <span data-ttu-id="fba3b-137">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="fba3b-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>
<span data-ttu-id="fba3b-138">Parâmetros: webhook (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fba3b-138">Parameters: Webhook (ByValue)</span></span>

### <span data-ttu-id="fba3b-139">System. String</span><span class="sxs-lookup"><span data-stu-id="fba3b-139">System.String</span></span>

## <span data-ttu-id="fba3b-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fba3b-140">OUTPUTS</span></span>

### <span data-ttu-id="fba3b-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fba3b-141">System.Boolean</span></span>

## <span data-ttu-id="fba3b-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fba3b-142">NOTES</span></span>

## <span data-ttu-id="fba3b-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fba3b-143">RELATED LINKS</span></span>

[<span data-ttu-id="fba3b-144">New-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="fba3b-144">New-AzureRmContainerRegistryWebhook</span></span>](New-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="fba3b-145">Get-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="fba3b-145">Get-AzureRmContainerRegistryWebhook</span></span>](Get-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="fba3b-146">Update-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="fba3b-146">Update-AzureRmContainerRegistryWebhook</span></span>](Update-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="fba3b-147">Test-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="fba3b-147">Test-AzureRmContainerRegistryWebhook</span></span>](Test-AzureRmContainerRegistryWebhook.md)
