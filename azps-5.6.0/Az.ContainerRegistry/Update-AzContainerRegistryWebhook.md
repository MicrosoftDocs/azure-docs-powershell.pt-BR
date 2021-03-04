---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/update-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryWebhook.md
ms.openlocfilehash: cede1001f475d820dfec7131a8c86815bd98adb7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885917"
---
# <span data-ttu-id="3d2d6-101">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="3d2d6-101">Update-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="3d2d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d2d6-102">SYNOPSIS</span></span>
<span data-ttu-id="3d2d6-103">Atualiza um webhook de registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="3d2d6-103">Updates a container registry webhook.</span></span>

## <span data-ttu-id="3d2d6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3d2d6-104">SYNTAX</span></span>

### <span data-ttu-id="3d2d6-105">ResourceIdParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3d2d6-105">ResourceIdParameterSet (Default)</span></span>
```
Update-AzContainerRegistryWebhook [-Uri <Uri>] [-Action <String[]>] [-Header <Hashtable>] [-Tag <Hashtable>]
 [-Status <String>] [-Scope <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d2d6-106">NameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d2d6-106">NameResourceGroupParameterSet</span></span>
```
Update-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-Uri <Uri>] [-Action <String[]>] [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>]
 [-Scope <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d2d6-107">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d2d6-107">WebhookObjectParameterSet</span></span>
```
Update-AzContainerRegistryWebhook [-Uri <Uri>] [-Action <String[]>] -Webhook <PSContainerRegistryWebhook>
 [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>] [-Scope <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d2d6-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3d2d6-108">DESCRIPTION</span></span>
<span data-ttu-id="3d2d6-109">O Update-AzContainerRegistryWebhook cmdlet atualiza um webhook de registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="3d2d6-109">The Update-AzContainerRegistryWebhook cmdlet updates a container registry webhook.</span></span>

## <span data-ttu-id="3d2d6-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3d2d6-110">EXAMPLES</span></span>

### <span data-ttu-id="3d2d6-111">Exemplo 1: atualizar um webhook de registro de contêiner existente.</span><span class="sxs-lookup"><span data-stu-id="3d2d6-111">Example 1: Update an existing container registry webhook.</span></span>
```powershell
PS C:\>Update-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -Uri http://www.bing.com -Action Delete,Push -Header @{SpecialHeader='headerVal'} -Tag @{Key='val'} -Status Enabled -Scope 'foo:*'

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled    foo:*           {push, delete}  Succeeded
```

<span data-ttu-id="3d2d6-112">Atualize um webhook de registro de contêiner existente.</span><span class="sxs-lookup"><span data-stu-id="3d2d6-112">Update an existing container registry webhook.</span></span>

## <span data-ttu-id="3d2d6-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3d2d6-113">PARAMETERS</span></span>

### <span data-ttu-id="3d2d6-114">-Action</span><span class="sxs-lookup"><span data-stu-id="3d2d6-114">-Action</span></span>
<span data-ttu-id="3d2d6-115">Lista separada de espaços de ações que disparam o webhook para postar notificações.</span><span class="sxs-lookup"><span data-stu-id="3d2d6-115">Space separated list of actions that trigger the webhook to post notifications.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: WebhookActions
Accepted values: delete, push

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d2d6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d2d6-116">-DefaultProfile</span></span>
<span data-ttu-id="3d2d6-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="3d2d6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d2d6-118">-Header</span><span class="sxs-lookup"><span data-stu-id="3d2d6-118">-Header</span></span>
<span data-ttu-id="3d2d6-119">Espaços separados de headers personalizados no formato 'key \[ =value ' que serão adicionados às notificações \] de webhook.</span><span class="sxs-lookup"><span data-stu-id="3d2d6-119">Space separated custom headers in 'key\[=value\]' format that will be added to the webhook notifications.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: WebhookHeaders

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d2d6-120">-Name</span><span class="sxs-lookup"><span data-stu-id="3d2d6-120">-Name</span></span>
<span data-ttu-id="3d2d6-121">Nome do webhook.</span><span class="sxs-lookup"><span data-stu-id="3d2d6-121">Webhook Name.</span></span>

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

### <span data-ttu-id="3d2d6-122">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="3d2d6-122">-RegistryName</span></span>
<span data-ttu-id="3d2d6-123">Nome do Registro do Contêiner.</span><span class="sxs-lookup"><span data-stu-id="3d2d6-123">Container Registry Name.</span></span>

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

### <span data-ttu-id="3d2d6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d2d6-124">-ResourceGroupName</span></span>
<span data-ttu-id="3d2d6-125">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="3d2d6-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="3d2d6-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3d2d6-126">-ResourceId</span></span>
<span data-ttu-id="3d2d6-127">A ID do recurso Webhook do registro de contêiner</span><span class="sxs-lookup"><span data-stu-id="3d2d6-127">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="3d2d6-128">-Scope</span><span class="sxs-lookup"><span data-stu-id="3d2d6-128">-Scope</span></span>
<span data-ttu-id="3d2d6-129">Escopo webhook.</span><span class="sxs-lookup"><span data-stu-id="3d2d6-129">Webhook scope.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WebhookScope

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d2d6-130">-Status</span><span class="sxs-lookup"><span data-stu-id="3d2d6-130">-Status</span></span>
<span data-ttu-id="3d2d6-131">Status do webhook</span><span class="sxs-lookup"><span data-stu-id="3d2d6-131">Webhook status</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WebhookStatus
Accepted values: enabled, disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d2d6-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="3d2d6-132">-Tag</span></span>
<span data-ttu-id="3d2d6-133">Marcas separadas por espaço no formato 'key \[ =value \] '.</span><span class="sxs-lookup"><span data-stu-id="3d2d6-133">Space separated tags in 'key\[=value\]' format.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d2d6-134">-Uri</span><span class="sxs-lookup"><span data-stu-id="3d2d6-134">-Uri</span></span>
<span data-ttu-id="3d2d6-135">O URI de serviço para o webhook para postar notificações.</span><span class="sxs-lookup"><span data-stu-id="3d2d6-135">The service URI for the webhook to post notifications.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: WebhookUri

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d2d6-136">-Webhook</span><span class="sxs-lookup"><span data-stu-id="3d2d6-136">-Webhook</span></span>
<span data-ttu-id="3d2d6-137">Objeto Webhook do Registro de Contêiner.</span><span class="sxs-lookup"><span data-stu-id="3d2d6-137">Container Registry Webhook Object.</span></span>

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

### <span data-ttu-id="3d2d6-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3d2d6-138">-Confirm</span></span>
<span data-ttu-id="3d2d6-139">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d2d6-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d2d6-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d2d6-140">-WhatIf</span></span>
<span data-ttu-id="3d2d6-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3d2d6-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3d2d6-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3d2d6-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d2d6-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d2d6-143">CommonParameters</span></span>
<span data-ttu-id="3d2d6-144">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d2d6-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d2d6-145">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3d2d6-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d2d6-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3d2d6-146">INPUTS</span></span>

### <span data-ttu-id="3d2d6-147">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="3d2d6-147">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

### <span data-ttu-id="3d2d6-148">System.String</span><span class="sxs-lookup"><span data-stu-id="3d2d6-148">System.String</span></span>

## <span data-ttu-id="3d2d6-149">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3d2d6-149">OUTPUTS</span></span>

### <span data-ttu-id="3d2d6-150">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="3d2d6-150">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="3d2d6-151">NOTES</span><span class="sxs-lookup"><span data-stu-id="3d2d6-151">NOTES</span></span>

## <span data-ttu-id="3d2d6-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3d2d6-152">RELATED LINKS</span></span>

[<span data-ttu-id="3d2d6-153">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="3d2d6-153">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="3d2d6-154">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="3d2d6-154">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="3d2d6-155">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="3d2d6-155">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)

[<span data-ttu-id="3d2d6-156">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="3d2d6-156">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)