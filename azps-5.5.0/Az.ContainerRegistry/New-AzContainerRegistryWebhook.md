---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryWebhook.md
ms.openlocfilehash: 8ea10f2acbe69e31bf80e35f0a8ea1577ffac6f5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116499"
---
# <span data-ttu-id="330e7-101">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="330e7-101">New-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="330e7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="330e7-102">SYNOPSIS</span></span>
<span data-ttu-id="330e7-103">Cria um contêiner da Web de registro.</span><span class="sxs-lookup"><span data-stu-id="330e7-103">Creates a container registry webhook.</span></span>

## <span data-ttu-id="330e7-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="330e7-104">SYNTAX</span></span>

### <span data-ttu-id="330e7-105">NameResourceGroupParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="330e7-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>]
 [-Scope <String>] [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="330e7-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="330e7-106">RegistryObjectParameterSet</span></span>
```
New-AzContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]>
 -Registry <PSContainerRegistry> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>] [-Scope <String>]
 [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="330e7-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="330e7-107">ResourceIdParameterSet</span></span>
```
New-AzContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>]
 [-Tag <Hashtable>] [-Status <String>] [-Scope <String>] [-Location <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="330e7-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="330e7-108">DESCRIPTION</span></span>
<span data-ttu-id="330e7-109">O New-AzContainerRegistryWebhook cmdlet cria um webtare de registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="330e7-109">The New-AzContainerRegistryWebhook cmdlet creates a container registry webhook.</span></span>

## <span data-ttu-id="330e7-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="330e7-110">EXAMPLES</span></span>

### <span data-ttu-id="330e7-111">Exemplo 1: Criar um contêiner de registro web browser.</span><span class="sxs-lookup"><span data-stu-id="330e7-111">Example 1: Create a container registry webhook.</span></span>
```
PS C:\> New-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -Uri http://www.bing.com -Action Delete,Push -Header @{SpecialHeader='headerVal'} -Tag @{Key="val"} -Location "east us" -Status Enabled -Scope "foo:*"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled    foo:*           {push, delete}  Succeeded
```

<span data-ttu-id="330e7-112">Criar um contêiner da Web de registro.</span><span class="sxs-lookup"><span data-stu-id="330e7-112">Create a container registry webhook.</span></span>

## <span data-ttu-id="330e7-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="330e7-113">PARAMETERS</span></span>

### <span data-ttu-id="330e7-114">-Ação</span><span class="sxs-lookup"><span data-stu-id="330e7-114">-Action</span></span>
<span data-ttu-id="330e7-115">Lista de ações separadas por espaços que acionam a Webção para postar notificações.</span><span class="sxs-lookup"><span data-stu-id="330e7-115">Space separated list of actions that trigger the webhook to post notifications.</span></span>

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

### <span data-ttu-id="330e7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="330e7-116">-DefaultProfile</span></span>
<span data-ttu-id="330e7-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="330e7-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="330e7-118">-Header</span><span class="sxs-lookup"><span data-stu-id="330e7-118">-Header</span></span>
<span data-ttu-id="330e7-119">Headers personalizados que serão adicionados às notificações de web notifications.</span><span class="sxs-lookup"><span data-stu-id="330e7-119">Custom headers that will be added to the webhook notifications.</span></span>

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

### <span data-ttu-id="330e7-120">-Local</span><span class="sxs-lookup"><span data-stu-id="330e7-120">-Location</span></span>
<span data-ttu-id="330e7-121">Localização web browser.</span><span class="sxs-lookup"><span data-stu-id="330e7-121">Webhook Location.</span></span>
<span data-ttu-id="330e7-122">Padrão para o local do registro.</span><span class="sxs-lookup"><span data-stu-id="330e7-122">Default to the location of the registry.</span></span>

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

### <span data-ttu-id="330e7-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="330e7-123">-Name</span></span>
<span data-ttu-id="330e7-124">Nome Web browser.</span><span class="sxs-lookup"><span data-stu-id="330e7-124">Webhook Name.</span></span>

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

### <span data-ttu-id="330e7-125">-Registro</span><span class="sxs-lookup"><span data-stu-id="330e7-125">-Registry</span></span>
<span data-ttu-id="330e7-126">Objeto do Registro de Contêineres.</span><span class="sxs-lookup"><span data-stu-id="330e7-126">Container Registry Object.</span></span>

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

### <span data-ttu-id="330e7-127">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="330e7-127">-RegistryName</span></span>
<span data-ttu-id="330e7-128">Nome do Registro do Contêiner.</span><span class="sxs-lookup"><span data-stu-id="330e7-128">Container Registry Name.</span></span>

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

### <span data-ttu-id="330e7-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="330e7-129">-ResourceGroupName</span></span>
<span data-ttu-id="330e7-130">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="330e7-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="330e7-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="330e7-131">-ResourceId</span></span>
<span data-ttu-id="330e7-132">A ID do recurso de registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="330e7-132">The container registry resource id</span></span>

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

### <span data-ttu-id="330e7-133">-Escopo</span><span class="sxs-lookup"><span data-stu-id="330e7-133">-Scope</span></span>
<span data-ttu-id="330e7-134">Escopo web scope.</span><span class="sxs-lookup"><span data-stu-id="330e7-134">Webhook scope.</span></span>

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

### <span data-ttu-id="330e7-135">-Status</span><span class="sxs-lookup"><span data-stu-id="330e7-135">-Status</span></span>
<span data-ttu-id="330e7-136">Status web browser, valor padrão habilitado</span><span class="sxs-lookup"><span data-stu-id="330e7-136">Webhook status, default value is enabled</span></span>

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

### <span data-ttu-id="330e7-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="330e7-137">-Tag</span></span>
<span data-ttu-id="330e7-138">Marcas Web browser.</span><span class="sxs-lookup"><span data-stu-id="330e7-138">Webhook tags.</span></span>

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

### <span data-ttu-id="330e7-139">-Uri</span><span class="sxs-lookup"><span data-stu-id="330e7-139">-Uri</span></span>
<span data-ttu-id="330e7-140">O URI de serviço do web browser para postar notificações.</span><span class="sxs-lookup"><span data-stu-id="330e7-140">The service URI for the webhook to post notifications.</span></span>

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

### <span data-ttu-id="330e7-141">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="330e7-141">-Confirm</span></span>
<span data-ttu-id="330e7-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="330e7-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="330e7-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="330e7-143">-WhatIf</span></span>
<span data-ttu-id="330e7-144">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="330e7-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="330e7-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="330e7-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="330e7-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="330e7-146">CommonParameters</span></span>
<span data-ttu-id="330e7-147">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="330e7-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="330e7-148">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="330e7-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="330e7-149">Entradas</span><span class="sxs-lookup"><span data-stu-id="330e7-149">INPUTS</span></span>

### <span data-ttu-id="330e7-150">System.String</span><span class="sxs-lookup"><span data-stu-id="330e7-150">System.String</span></span>

## <span data-ttu-id="330e7-151">Saídas</span><span class="sxs-lookup"><span data-stu-id="330e7-151">OUTPUTS</span></span>

### <span data-ttu-id="330e7-152">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebweb</span><span class="sxs-lookup"><span data-stu-id="330e7-152">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="330e7-153">Notas</span><span class="sxs-lookup"><span data-stu-id="330e7-153">NOTES</span></span>

## <span data-ttu-id="330e7-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="330e7-154">RELATED LINKS</span></span>

[<span data-ttu-id="330e7-155">Get-AzContainerRegistryWebweb</span><span class="sxs-lookup"><span data-stu-id="330e7-155">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="330e7-156">Update-AzContainerRegistryWebweb</span><span class="sxs-lookup"><span data-stu-id="330e7-156">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="330e7-157">Remove-AzContainerRegistryWebweb</span><span class="sxs-lookup"><span data-stu-id="330e7-157">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)

[<span data-ttu-id="330e7-158">Test-AzContainerRegistryWebweb</span><span class="sxs-lookup"><span data-stu-id="330e7-158">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)