---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryWebhook.md
ms.openlocfilehash: 1c96b33fd93082c33dfb49abdf23fac8795b2b28
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601177"
---
# <span data-ttu-id="46d12-101">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="46d12-101">Remove-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="46d12-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="46d12-102">SYNOPSIS</span></span>
<span data-ttu-id="46d12-103">Remove um webhook do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="46d12-103">Removes a container registry webhook.</span></span>

## <span data-ttu-id="46d12-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="46d12-104">SYNTAX</span></span>

### <span data-ttu-id="46d12-105">NameResourceGroupParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="46d12-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46d12-106">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="46d12-106">WebhookObjectParameterSet</span></span>
```
Remove-AzContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46d12-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="46d12-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistryWebhook -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46d12-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="46d12-108">DESCRIPTION</span></span>
<span data-ttu-id="46d12-109">O cmdlet Remove-AzContainerRegistryWebhook remove um webhook do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="46d12-109">The Remove-AzContainerRegistryWebhook cmdlet removes a container registry webhook.</span></span>

## <span data-ttu-id="46d12-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="46d12-110">EXAMPLES</span></span>

### <span data-ttu-id="46d12-111">Exemplo 1: remover um webhook do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="46d12-111">Example 1: Remove a container registry webhook.</span></span>
```powershell
PS C:\> Remove-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"
```

<span data-ttu-id="46d12-112">Remove um webhook do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="46d12-112">Removes a container registry webhook.</span></span>

## <span data-ttu-id="46d12-113">OS</span><span class="sxs-lookup"><span data-stu-id="46d12-113">PARAMETERS</span></span>

### <span data-ttu-id="46d12-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46d12-114">-DefaultProfile</span></span>
<span data-ttu-id="46d12-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="46d12-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46d12-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="46d12-116">-Name</span></span>
<span data-ttu-id="46d12-117">Nome do webhook.</span><span class="sxs-lookup"><span data-stu-id="46d12-117">Webhook Name.</span></span>

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

### <span data-ttu-id="46d12-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="46d12-118">-PassThru</span></span>
<span data-ttu-id="46d12-119">Indica que esse cmdlet retorna true se a remoção tiver sido bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="46d12-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="46d12-120">-Registryname</span><span class="sxs-lookup"><span data-stu-id="46d12-120">-RegistryName</span></span>
<span data-ttu-id="46d12-121">Nome do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="46d12-121">Container Registry Name.</span></span>

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

### <span data-ttu-id="46d12-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46d12-122">-ResourceGroupName</span></span>
<span data-ttu-id="46d12-123">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="46d12-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="46d12-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="46d12-124">-ResourceId</span></span>
<span data-ttu-id="46d12-125">A ID do recurso de webhook do registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="46d12-125">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="46d12-126">-Webhook</span><span class="sxs-lookup"><span data-stu-id="46d12-126">-Webhook</span></span>
<span data-ttu-id="46d12-127">Objeto do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="46d12-127">Container Registry Object.</span></span>

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

### <span data-ttu-id="46d12-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="46d12-128">-Confirm</span></span>
<span data-ttu-id="46d12-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46d12-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46d12-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46d12-130">-WhatIf</span></span>
<span data-ttu-id="46d12-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="46d12-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46d12-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="46d12-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46d12-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46d12-133">CommonParameters</span></span>
<span data-ttu-id="46d12-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46d12-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46d12-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46d12-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46d12-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="46d12-136">INPUTS</span></span>

### <span data-ttu-id="46d12-137">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="46d12-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

### <span data-ttu-id="46d12-138">System. String</span><span class="sxs-lookup"><span data-stu-id="46d12-138">System.String</span></span>

## <span data-ttu-id="46d12-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="46d12-139">OUTPUTS</span></span>

### <span data-ttu-id="46d12-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="46d12-140">System.Boolean</span></span>

## <span data-ttu-id="46d12-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="46d12-141">NOTES</span></span>

## <span data-ttu-id="46d12-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="46d12-142">RELATED LINKS</span></span>

[<span data-ttu-id="46d12-143">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="46d12-143">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="46d12-144">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="46d12-144">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="46d12-145">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="46d12-145">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="46d12-146">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="46d12-146">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)