---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryWebhook.md
ms.openlocfilehash: 061b712f0c9e2d77d4dab70a0e39051d5f92d7ff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771069"
---
# <span data-ttu-id="cfd03-101">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="cfd03-101">New-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="cfd03-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cfd03-102">SYNOPSIS</span></span>
<span data-ttu-id="cfd03-103">Cria um webhook do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="cfd03-103">Creates a container registry webhook.</span></span>

## <span data-ttu-id="cfd03-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cfd03-104">SYNTAX</span></span>

### <span data-ttu-id="cfd03-105">NameResourceGroupParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="cfd03-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>]
 [-Scope <String>] [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cfd03-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cfd03-106">RegistryObjectParameterSet</span></span>
```
New-AzContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]>
 -Registry <PSContainerRegistry> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>] [-Scope <String>]
 [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfd03-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cfd03-107">ResourceIdParameterSet</span></span>
```
New-AzContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>]
 [-Tag <Hashtable>] [-Status <String>] [-Scope <String>] [-Location <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cfd03-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cfd03-108">DESCRIPTION</span></span>
<span data-ttu-id="cfd03-109">O cmdlet New-AzContainerRegistryWebhook cria um webhook do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="cfd03-109">The New-AzContainerRegistryWebhook cmdlet creates a container registry webhook.</span></span>

## <span data-ttu-id="cfd03-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cfd03-110">EXAMPLES</span></span>

### <span data-ttu-id="cfd03-111">Exemplo 1: criar um webhook do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="cfd03-111">Example 1: Create a container registry webhook.</span></span>
```
PS C:\> New-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -Uri http://www.bing.com -Action Delete,Push -Header @{SpecialHeader='headerVal'} -Tag @{Key="val"} -Location "east us" -Status Enabled -Scope "foo:*"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled    foo:*           {push, delete}  Succeeded
```

<span data-ttu-id="cfd03-112">Crie um webhook do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="cfd03-112">Create a container registry webhook.</span></span>

## <span data-ttu-id="cfd03-113">OS</span><span class="sxs-lookup"><span data-stu-id="cfd03-113">PARAMETERS</span></span>

### <span data-ttu-id="cfd03-114">-Ação</span><span class="sxs-lookup"><span data-stu-id="cfd03-114">-Action</span></span>
<span data-ttu-id="cfd03-115">Lista separada por espaço de ações que disparam o webhook para postar notificações.</span><span class="sxs-lookup"><span data-stu-id="cfd03-115">Space separated list of actions that trigger the webhook to post notifications.</span></span>

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

### <span data-ttu-id="cfd03-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfd03-116">-DefaultProfile</span></span>
<span data-ttu-id="cfd03-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cfd03-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cfd03-118">-Header</span><span class="sxs-lookup"><span data-stu-id="cfd03-118">-Header</span></span>
<span data-ttu-id="cfd03-119">Cabeçalhos personalizados que serão adicionados às notificações do webhook.</span><span class="sxs-lookup"><span data-stu-id="cfd03-119">Custom headers that will be added to the webhook notifications.</span></span>

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

### <span data-ttu-id="cfd03-120">-Local</span><span class="sxs-lookup"><span data-stu-id="cfd03-120">-Location</span></span>
<span data-ttu-id="cfd03-121">Local do webhook.</span><span class="sxs-lookup"><span data-stu-id="cfd03-121">Webhook Location.</span></span>
<span data-ttu-id="cfd03-122">Padrão para o local do registro.</span><span class="sxs-lookup"><span data-stu-id="cfd03-122">Default to the location of the registry.</span></span>

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

### <span data-ttu-id="cfd03-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="cfd03-123">-Name</span></span>
<span data-ttu-id="cfd03-124">Nome do webhook.</span><span class="sxs-lookup"><span data-stu-id="cfd03-124">Webhook Name.</span></span>

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

### <span data-ttu-id="cfd03-125">-Registro</span><span class="sxs-lookup"><span data-stu-id="cfd03-125">-Registry</span></span>
<span data-ttu-id="cfd03-126">Objeto do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="cfd03-126">Container Registry Object.</span></span>

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

### <span data-ttu-id="cfd03-127">-Registryname</span><span class="sxs-lookup"><span data-stu-id="cfd03-127">-RegistryName</span></span>
<span data-ttu-id="cfd03-128">Nome do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="cfd03-128">Container Registry Name.</span></span>

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

### <span data-ttu-id="cfd03-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfd03-129">-ResourceGroupName</span></span>
<span data-ttu-id="cfd03-130">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cfd03-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="cfd03-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cfd03-131">-ResourceId</span></span>
<span data-ttu-id="cfd03-132">A ID do recurso do registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="cfd03-132">The container registry resource id</span></span>

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

### <span data-ttu-id="cfd03-133">-Escopo</span><span class="sxs-lookup"><span data-stu-id="cfd03-133">-Scope</span></span>
<span data-ttu-id="cfd03-134">Escopo do webhook.</span><span class="sxs-lookup"><span data-stu-id="cfd03-134">Webhook scope.</span></span>

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

### <span data-ttu-id="cfd03-135">-Status</span><span class="sxs-lookup"><span data-stu-id="cfd03-135">-Status</span></span>
<span data-ttu-id="cfd03-136">Status do webhook, o valor padrão é habilitado</span><span class="sxs-lookup"><span data-stu-id="cfd03-136">Webhook status, default value is enabled</span></span>

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

### <span data-ttu-id="cfd03-137">-Marca</span><span class="sxs-lookup"><span data-stu-id="cfd03-137">-Tag</span></span>
<span data-ttu-id="cfd03-138">Marcas webhook.</span><span class="sxs-lookup"><span data-stu-id="cfd03-138">Webhook tags.</span></span>

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

### <span data-ttu-id="cfd03-139">-URI</span><span class="sxs-lookup"><span data-stu-id="cfd03-139">-Uri</span></span>
<span data-ttu-id="cfd03-140">O URI do serviço para o webhook para postar notificações.</span><span class="sxs-lookup"><span data-stu-id="cfd03-140">The service URI for the webhook to post notifications.</span></span>

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

### <span data-ttu-id="cfd03-141">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cfd03-141">-Confirm</span></span>
<span data-ttu-id="cfd03-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cfd03-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfd03-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfd03-143">-WhatIf</span></span>
<span data-ttu-id="cfd03-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cfd03-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cfd03-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cfd03-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cfd03-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfd03-146">CommonParameters</span></span>
<span data-ttu-id="cfd03-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfd03-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfd03-148">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfd03-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfd03-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cfd03-149">INPUTS</span></span>

### <span data-ttu-id="cfd03-150">System. String</span><span class="sxs-lookup"><span data-stu-id="cfd03-150">System.String</span></span>

## <span data-ttu-id="cfd03-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cfd03-151">OUTPUTS</span></span>

### <span data-ttu-id="cfd03-152">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="cfd03-152">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="cfd03-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cfd03-153">NOTES</span></span>

## <span data-ttu-id="cfd03-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cfd03-154">RELATED LINKS</span></span>

[<span data-ttu-id="cfd03-155">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="cfd03-155">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="cfd03-156">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="cfd03-156">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="cfd03-157">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="cfd03-157">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)

[<span data-ttu-id="cfd03-158">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="cfd03-158">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)