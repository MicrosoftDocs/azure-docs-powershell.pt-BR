---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/new-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryWebhook.md
ms.openlocfilehash: 10acca5a89c4ea84d475e5eea2e89e18942116f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888318"
---
# <span data-ttu-id="ca985-101">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="ca985-101">New-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="ca985-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca985-102">SYNOPSIS</span></span>
<span data-ttu-id="ca985-103">Cria um webhook de registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="ca985-103">Creates a container registry webhook.</span></span>

## <span data-ttu-id="ca985-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ca985-104">SYNTAX</span></span>

### <span data-ttu-id="ca985-105">NameResourceGroupParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ca985-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>]
 [-Scope <String>] [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ca985-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca985-106">RegistryObjectParameterSet</span></span>
```
New-AzContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]>
 -Registry <PSContainerRegistry> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>] [-Scope <String>]
 [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca985-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca985-107">ResourceIdParameterSet</span></span>
```
New-AzContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>]
 [-Tag <Hashtable>] [-Status <String>] [-Scope <String>] [-Location <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca985-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ca985-108">DESCRIPTION</span></span>
<span data-ttu-id="ca985-109">O New-AzContainerRegistryWebhook cmdlet cria um webhook de registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="ca985-109">The New-AzContainerRegistryWebhook cmdlet creates a container registry webhook.</span></span>

## <span data-ttu-id="ca985-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ca985-110">EXAMPLES</span></span>

### <span data-ttu-id="ca985-111">Exemplo 1: Criar um webhook de registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="ca985-111">Example 1: Create a container registry webhook.</span></span>
```
PS C:\> New-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -Uri http://www.bing.com -Action Delete,Push -Header @{SpecialHeader='headerVal'} -Tag @{Key="val"} -Location "east us" -Status Enabled -Scope "foo:*"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled    foo:*           {push, delete}  Succeeded
```

<span data-ttu-id="ca985-112">Crie um webhook de registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="ca985-112">Create a container registry webhook.</span></span>

## <span data-ttu-id="ca985-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ca985-113">PARAMETERS</span></span>

### <span data-ttu-id="ca985-114">-Action</span><span class="sxs-lookup"><span data-stu-id="ca985-114">-Action</span></span>
<span data-ttu-id="ca985-115">Lista separada de espaços de ações que disparam o webhook para postar notificações.</span><span class="sxs-lookup"><span data-stu-id="ca985-115">Space separated list of actions that trigger the webhook to post notifications.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: WebhookActions
Accepted values: delete, push

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca985-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca985-116">-DefaultProfile</span></span>
<span data-ttu-id="ca985-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="ca985-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca985-118">-Header</span><span class="sxs-lookup"><span data-stu-id="ca985-118">-Header</span></span>
<span data-ttu-id="ca985-119">Headers personalizados que serão adicionados às notificações de webhook.</span><span class="sxs-lookup"><span data-stu-id="ca985-119">Custom headers that will be added to the webhook notifications.</span></span>

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

### <span data-ttu-id="ca985-120">-Location</span><span class="sxs-lookup"><span data-stu-id="ca985-120">-Location</span></span>
<span data-ttu-id="ca985-121">Local do webhook.</span><span class="sxs-lookup"><span data-stu-id="ca985-121">Webhook Location.</span></span>
<span data-ttu-id="ca985-122">Padrão para o local do Registro.</span><span class="sxs-lookup"><span data-stu-id="ca985-122">Default to the location of the registry.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WebhookLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca985-123">-Name</span><span class="sxs-lookup"><span data-stu-id="ca985-123">-Name</span></span>
<span data-ttu-id="ca985-124">Nome do webhook.</span><span class="sxs-lookup"><span data-stu-id="ca985-124">Webhook Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WebhookName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca985-125">-Registry</span><span class="sxs-lookup"><span data-stu-id="ca985-125">-Registry</span></span>
<span data-ttu-id="ca985-126">Objeto Container Registry.</span><span class="sxs-lookup"><span data-stu-id="ca985-126">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca985-127">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="ca985-127">-RegistryName</span></span>
<span data-ttu-id="ca985-128">Nome do Registro do Contêiner.</span><span class="sxs-lookup"><span data-stu-id="ca985-128">Container Registry Name.</span></span>

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

### <span data-ttu-id="ca985-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca985-129">-ResourceGroupName</span></span>
<span data-ttu-id="ca985-130">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="ca985-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="ca985-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ca985-131">-ResourceId</span></span>
<span data-ttu-id="ca985-132">A ID de recurso do Registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="ca985-132">The container registry resource id</span></span>

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

### <span data-ttu-id="ca985-133">-Scope</span><span class="sxs-lookup"><span data-stu-id="ca985-133">-Scope</span></span>
<span data-ttu-id="ca985-134">Escopo webhook.</span><span class="sxs-lookup"><span data-stu-id="ca985-134">Webhook scope.</span></span>

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

### <span data-ttu-id="ca985-135">-Status</span><span class="sxs-lookup"><span data-stu-id="ca985-135">-Status</span></span>
<span data-ttu-id="ca985-136">Status do webhook, valor padrão habilitado</span><span class="sxs-lookup"><span data-stu-id="ca985-136">Webhook status, default value is enabled</span></span>

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

### <span data-ttu-id="ca985-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="ca985-137">-Tag</span></span>
<span data-ttu-id="ca985-138">Marcas webhook.</span><span class="sxs-lookup"><span data-stu-id="ca985-138">Webhook tags.</span></span>

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

### <span data-ttu-id="ca985-139">-Uri</span><span class="sxs-lookup"><span data-stu-id="ca985-139">-Uri</span></span>
<span data-ttu-id="ca985-140">O URI de serviço para o webhook para postar notificações.</span><span class="sxs-lookup"><span data-stu-id="ca985-140">The service URI for the webhook to post notifications.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: WebhookUri

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca985-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ca985-141">-Confirm</span></span>
<span data-ttu-id="ca985-142">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca985-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca985-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca985-143">-WhatIf</span></span>
<span data-ttu-id="ca985-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ca985-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca985-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ca985-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca985-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca985-146">CommonParameters</span></span>
<span data-ttu-id="ca985-147">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca985-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca985-148">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ca985-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca985-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ca985-149">INPUTS</span></span>

### <span data-ttu-id="ca985-150">System.String</span><span class="sxs-lookup"><span data-stu-id="ca985-150">System.String</span></span>

## <span data-ttu-id="ca985-151">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ca985-151">OUTPUTS</span></span>

### <span data-ttu-id="ca985-152">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="ca985-152">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="ca985-153">NOTES</span><span class="sxs-lookup"><span data-stu-id="ca985-153">NOTES</span></span>

## <span data-ttu-id="ca985-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ca985-154">RELATED LINKS</span></span>

[<span data-ttu-id="ca985-155">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="ca985-155">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="ca985-156">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="ca985-156">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="ca985-157">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="ca985-157">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)

[<span data-ttu-id="ca985-158">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="ca985-158">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)