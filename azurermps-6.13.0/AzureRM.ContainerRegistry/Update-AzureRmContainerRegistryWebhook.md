---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/update-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryWebhook.md
ms.openlocfilehash: b7f10fd96d8f746db1ff37b1461cdd8394bdf75d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610096"
---
# <span data-ttu-id="a4121-101">Update-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="a4121-101">Update-AzureRmContainerRegistryWebhook</span></span>

## <span data-ttu-id="a4121-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a4121-102">SYNOPSIS</span></span>
<span data-ttu-id="a4121-103">Atualiza um webhook do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="a4121-103">Updates a container registry webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4121-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a4121-104">SYNTAX</span></span>

### <span data-ttu-id="a4121-105">ResourceIdParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="a4121-105">ResourceIdParameterSet (Default)</span></span>
```
Update-AzureRmContainerRegistryWebhook [-Uri <Uri>] [-Action <String[]>] [-Header <Hashtable>]
 [-Tag <Hashtable>] [-Status <String>] [-Scope <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4121-106">NameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4121-106">NameResourceGroupParameterSet</span></span>
```
Update-AzureRmContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-Uri <Uri>] [-Action <String[]>] [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>]
 [-Scope <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4121-107">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4121-107">WebhookObjectParameterSet</span></span>
```
Update-AzureRmContainerRegistryWebhook [-Uri <Uri>] [-Action <String[]>] -Webhook <PSContainerRegistryWebhook>
 [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>] [-Scope <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4121-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a4121-108">DESCRIPTION</span></span>
<span data-ttu-id="a4121-109">O cmdlet Update-AzureRmContainerRegistryWebhook atualiza um webhook do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="a4121-109">The Update-AzureRmContainerRegistryWebhook cmdlet updates a container registry webhook.</span></span>

## <span data-ttu-id="a4121-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a4121-110">EXAMPLES</span></span>

### <span data-ttu-id="a4121-111">Exemplo 1: atualizar um webhook existente do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="a4121-111">Example 1: Update an existing container registry webhook.</span></span>
```powershell
PS C:\>Update-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -Uri http://www.bing.com -Action Delete,Push -Header @{SpecialHeader='headerVal'} -Tag @{Key='val'} -Status Enabled -Scope 'foo:*'

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled    foo:*           {push, delete}  Succeeded
```

<span data-ttu-id="a4121-112">Atualizar um webhook existente do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="a4121-112">Update an existing container registry webhook.</span></span>

## <span data-ttu-id="a4121-113">OS</span><span class="sxs-lookup"><span data-stu-id="a4121-113">PARAMETERS</span></span>

### <span data-ttu-id="a4121-114">-Ação</span><span class="sxs-lookup"><span data-stu-id="a4121-114">-Action</span></span>
<span data-ttu-id="a4121-115">Lista separada por espaço de ações que disparam o webhook para postar notificações.</span><span class="sxs-lookup"><span data-stu-id="a4121-115">Space separated list of actions that trigger the webhook to post notifications.</span></span>

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

### <span data-ttu-id="a4121-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4121-116">-DefaultProfile</span></span>
<span data-ttu-id="a4121-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a4121-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4121-118">-Header</span><span class="sxs-lookup"><span data-stu-id="a4121-118">-Header</span></span>
<span data-ttu-id="a4121-119">Cabeçalhos personalizados separados por espaço no formato ' chave \[ = valor \] ' que serão adicionados às notificações do webhook.</span><span class="sxs-lookup"><span data-stu-id="a4121-119">Space separated custom headers in 'key\[=value\]' format that will be added to the webhook notifications.</span></span>

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

### <span data-ttu-id="a4121-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="a4121-120">-Name</span></span>
<span data-ttu-id="a4121-121">Nome do webhook.</span><span class="sxs-lookup"><span data-stu-id="a4121-121">Webhook Name.</span></span>

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

### <span data-ttu-id="a4121-122">-Registryname</span><span class="sxs-lookup"><span data-stu-id="a4121-122">-RegistryName</span></span>
<span data-ttu-id="a4121-123">Nome do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="a4121-123">Container Registry Name.</span></span>

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

### <span data-ttu-id="a4121-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4121-124">-ResourceGroupName</span></span>
<span data-ttu-id="a4121-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a4121-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="a4121-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4121-126">-ResourceId</span></span>
<span data-ttu-id="a4121-127">A ID do recurso de webhook do registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="a4121-127">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="a4121-128">-Escopo</span><span class="sxs-lookup"><span data-stu-id="a4121-128">-Scope</span></span>
<span data-ttu-id="a4121-129">Escopo do webhook.</span><span class="sxs-lookup"><span data-stu-id="a4121-129">Webhook scope.</span></span>

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

### <span data-ttu-id="a4121-130">-Status</span><span class="sxs-lookup"><span data-stu-id="a4121-130">-Status</span></span>
<span data-ttu-id="a4121-131">Status do webhook</span><span class="sxs-lookup"><span data-stu-id="a4121-131">Webhook status</span></span>

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

### <span data-ttu-id="a4121-132">-Marca</span><span class="sxs-lookup"><span data-stu-id="a4121-132">-Tag</span></span>
<span data-ttu-id="a4121-133">Marcas separadas por espaço no formato ' chave \[ = valor \] '.</span><span class="sxs-lookup"><span data-stu-id="a4121-133">Space separated tags in 'key\[=value\]' format.</span></span>

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

### <span data-ttu-id="a4121-134">-URI</span><span class="sxs-lookup"><span data-stu-id="a4121-134">-Uri</span></span>
<span data-ttu-id="a4121-135">O URI do serviço para o webhook para postar notificações.</span><span class="sxs-lookup"><span data-stu-id="a4121-135">The service URI for the webhook to post notifications.</span></span>

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

### <span data-ttu-id="a4121-136">-Webhook</span><span class="sxs-lookup"><span data-stu-id="a4121-136">-Webhook</span></span>
<span data-ttu-id="a4121-137">Objeto webhook do registro contêiner.</span><span class="sxs-lookup"><span data-stu-id="a4121-137">Container Registry Webhook Object.</span></span>

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

### <span data-ttu-id="a4121-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a4121-138">-Confirm</span></span>
<span data-ttu-id="a4121-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4121-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4121-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4121-140">-WhatIf</span></span>
<span data-ttu-id="a4121-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a4121-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a4121-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a4121-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4121-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4121-143">CommonParameters</span></span>
<span data-ttu-id="a4121-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4121-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4121-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4121-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4121-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a4121-146">INPUTS</span></span>

### <span data-ttu-id="a4121-147">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="a4121-147">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>
<span data-ttu-id="a4121-148">Parâmetros: webhook (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a4121-148">Parameters: Webhook (ByValue)</span></span>

### <span data-ttu-id="a4121-149">System. String</span><span class="sxs-lookup"><span data-stu-id="a4121-149">System.String</span></span>

## <span data-ttu-id="a4121-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a4121-150">OUTPUTS</span></span>

### <span data-ttu-id="a4121-151">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="a4121-151">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="a4121-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a4121-152">NOTES</span></span>

## <span data-ttu-id="a4121-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a4121-153">RELATED LINKS</span></span>

[<span data-ttu-id="a4121-154">New-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="a4121-154">New-AzureRmContainerRegistryWebhook</span></span>](New-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="a4121-155">Get-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="a4121-155">Get-AzureRmContainerRegistryWebhook</span></span>](Get-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="a4121-156">Test-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="a4121-156">Test-AzureRmContainerRegistryWebhook</span></span>](Test-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="a4121-157">Remove-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="a4121-157">Remove-AzureRmContainerRegistryWebhook</span></span>](Remove-AzureRmContainerRegistryWebhook.md)
