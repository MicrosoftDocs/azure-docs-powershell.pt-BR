---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryWebhook.md
ms.openlocfilehash: 2343b58891109d829a37131dff084b2b51e7f8ad
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111048"
---
# <span data-ttu-id="432df-101">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="432df-101">Update-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="432df-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="432df-102">SYNOPSIS</span></span>
<span data-ttu-id="432df-103">Atualiza um contêiner da Web de registro.</span><span class="sxs-lookup"><span data-stu-id="432df-103">Updates a container registry webhook.</span></span>

## <span data-ttu-id="432df-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="432df-104">SYNTAX</span></span>

### <span data-ttu-id="432df-105">ResourceIdParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="432df-105">ResourceIdParameterSet (Default)</span></span>
```
Update-AzContainerRegistryWebhook [-Uri <Uri>] [-Action <String[]>] [-Header <Hashtable>] [-Tag <Hashtable>]
 [-Status <String>] [-Scope <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="432df-106">NameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="432df-106">NameResourceGroupParameterSet</span></span>
```
Update-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-Uri <Uri>] [-Action <String[]>] [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>]
 [-Scope <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="432df-107">WebbjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="432df-107">WebhookObjectParameterSet</span></span>
```
Update-AzContainerRegistryWebhook [-Uri <Uri>] [-Action <String[]>] -Webhook <PSContainerRegistryWebhook>
 [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>] [-Scope <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="432df-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="432df-108">DESCRIPTION</span></span>
<span data-ttu-id="432df-109">O Update-AzContainerRegistryWebhook cmdlet atualiza um web registry de contêiner.</span><span class="sxs-lookup"><span data-stu-id="432df-109">The Update-AzContainerRegistryWebhook cmdlet updates a container registry webhook.</span></span>

## <span data-ttu-id="432df-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="432df-110">EXAMPLES</span></span>

### <span data-ttu-id="432df-111">Exemplo 1: Atualizar um webtare de registro de contêiner existente.</span><span class="sxs-lookup"><span data-stu-id="432df-111">Example 1: Update an existing container registry webhook.</span></span>
```powershell
PS C:\>Update-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -Uri http://www.bing.com -Action Delete,Push -Header @{SpecialHeader='headerVal'} -Tag @{Key='val'} -Status Enabled -Scope 'foo:*'

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled    foo:*           {push, delete}  Succeeded
```

<span data-ttu-id="432df-112">Atualize uma Web de registro de contêiner existente.</span><span class="sxs-lookup"><span data-stu-id="432df-112">Update an existing container registry webhook.</span></span>

## <span data-ttu-id="432df-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="432df-113">PARAMETERS</span></span>

### <span data-ttu-id="432df-114">-Ação</span><span class="sxs-lookup"><span data-stu-id="432df-114">-Action</span></span>
<span data-ttu-id="432df-115">Lista de ações separadas por espaços que acionam a Webção para postar notificações.</span><span class="sxs-lookup"><span data-stu-id="432df-115">Space separated list of actions that trigger the webhook to post notifications.</span></span>

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

### <span data-ttu-id="432df-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="432df-116">-DefaultProfile</span></span>
<span data-ttu-id="432df-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="432df-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="432df-118">-Header</span><span class="sxs-lookup"><span data-stu-id="432df-118">-Header</span></span>
<span data-ttu-id="432df-119">Espaços separados por headers personalizados no formato 'key \[ \] =value' que serão adicionados às notificações web widget.</span><span class="sxs-lookup"><span data-stu-id="432df-119">Space separated custom headers in 'key\[=value\]' format that will be added to the webhook notifications.</span></span>

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

### <span data-ttu-id="432df-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="432df-120">-Name</span></span>
<span data-ttu-id="432df-121">Nome Web browser.</span><span class="sxs-lookup"><span data-stu-id="432df-121">Webhook Name.</span></span>

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

### <span data-ttu-id="432df-122">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="432df-122">-RegistryName</span></span>
<span data-ttu-id="432df-123">Nome do Registro do Contêiner.</span><span class="sxs-lookup"><span data-stu-id="432df-123">Container Registry Name.</span></span>

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

### <span data-ttu-id="432df-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="432df-124">-ResourceGroupName</span></span>
<span data-ttu-id="432df-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="432df-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="432df-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="432df-126">-ResourceId</span></span>
<span data-ttu-id="432df-127">A ID de recurso Web browser do registro de contêineres</span><span class="sxs-lookup"><span data-stu-id="432df-127">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="432df-128">-Escopo</span><span class="sxs-lookup"><span data-stu-id="432df-128">-Scope</span></span>
<span data-ttu-id="432df-129">Escopo web scope.</span><span class="sxs-lookup"><span data-stu-id="432df-129">Webhook scope.</span></span>

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

### <span data-ttu-id="432df-130">-Status</span><span class="sxs-lookup"><span data-stu-id="432df-130">-Status</span></span>
<span data-ttu-id="432df-131">Status da Webção</span><span class="sxs-lookup"><span data-stu-id="432df-131">Webhook status</span></span>

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

### <span data-ttu-id="432df-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="432df-132">-Tag</span></span>
<span data-ttu-id="432df-133">Marcas separadas por espaço no formato 'key \[ \] =value'.</span><span class="sxs-lookup"><span data-stu-id="432df-133">Space separated tags in 'key\[=value\]' format.</span></span>

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

### <span data-ttu-id="432df-134">-Uri</span><span class="sxs-lookup"><span data-stu-id="432df-134">-Uri</span></span>
<span data-ttu-id="432df-135">O URI de serviço do web browser para postar notificações.</span><span class="sxs-lookup"><span data-stu-id="432df-135">The service URI for the webhook to post notifications.</span></span>

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

### <span data-ttu-id="432df-136">-Web browser</span><span class="sxs-lookup"><span data-stu-id="432df-136">-Webhook</span></span>
<span data-ttu-id="432df-137">Objeto Web browser do Registro de Contêineres.</span><span class="sxs-lookup"><span data-stu-id="432df-137">Container Registry Webhook Object.</span></span>

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

### <span data-ttu-id="432df-138">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="432df-138">-Confirm</span></span>
<span data-ttu-id="432df-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="432df-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="432df-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="432df-140">-WhatIf</span></span>
<span data-ttu-id="432df-141">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="432df-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="432df-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="432df-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="432df-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="432df-143">CommonParameters</span></span>
<span data-ttu-id="432df-144">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="432df-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="432df-145">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="432df-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="432df-146">Entradas</span><span class="sxs-lookup"><span data-stu-id="432df-146">INPUTS</span></span>

### <span data-ttu-id="432df-147">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebweb</span><span class="sxs-lookup"><span data-stu-id="432df-147">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

### <span data-ttu-id="432df-148">System.String</span><span class="sxs-lookup"><span data-stu-id="432df-148">System.String</span></span>

## <span data-ttu-id="432df-149">Saídas</span><span class="sxs-lookup"><span data-stu-id="432df-149">OUTPUTS</span></span>

### <span data-ttu-id="432df-150">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebweb</span><span class="sxs-lookup"><span data-stu-id="432df-150">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="432df-151">Notas</span><span class="sxs-lookup"><span data-stu-id="432df-151">NOTES</span></span>

## <span data-ttu-id="432df-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="432df-152">RELATED LINKS</span></span>

[<span data-ttu-id="432df-153">New-AzContainerRegistryWebweb</span><span class="sxs-lookup"><span data-stu-id="432df-153">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="432df-154">Get-AzContainerRegistryWebweb</span><span class="sxs-lookup"><span data-stu-id="432df-154">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="432df-155">Test-AzContainerRegistryWebweb</span><span class="sxs-lookup"><span data-stu-id="432df-155">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)

[<span data-ttu-id="432df-156">Remove-AzContainerRegistryWebweb</span><span class="sxs-lookup"><span data-stu-id="432df-156">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)