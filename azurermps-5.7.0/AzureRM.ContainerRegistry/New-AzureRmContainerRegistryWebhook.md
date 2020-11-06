---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/new-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistryWebhook.md
ms.openlocfilehash: 0a23cfb79c341fb4fcee5b5688b0780ba178e978
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431037"
---
# <span data-ttu-id="af4eb-101">New-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="af4eb-101">New-AzureRmContainerRegistryWebhook</span></span>

## <span data-ttu-id="af4eb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="af4eb-102">SYNOPSIS</span></span>
<span data-ttu-id="af4eb-103">Cria um webhook do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="af4eb-103">Creates a container registry webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af4eb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="af4eb-104">SYNTAX</span></span>

### <span data-ttu-id="af4eb-105">NameResourceGroupParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="af4eb-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzureRmContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>]
 [-Scope <String>] [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="af4eb-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="af4eb-106">RegistryObjectParameterSet</span></span>
```
New-AzureRmContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]>
 -Registry <PSContainerRegistry> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>] [-Scope <String>]
 [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af4eb-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="af4eb-107">ResourceIdParameterSet</span></span>
```
New-AzureRmContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>]
 [-Tag <Hashtable>] [-Status <String>] [-Scope <String>] [-Location <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af4eb-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="af4eb-108">DESCRIPTION</span></span>
<span data-ttu-id="af4eb-109">O cmdlet New-AzureRmContainerRegistryWebhook cria um webhook do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="af4eb-109">The New-AzureRmContainerRegistryWebhook cmdlet creates a container registry webhook.</span></span>

## <span data-ttu-id="af4eb-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="af4eb-110">EXAMPLES</span></span>

### <span data-ttu-id="af4eb-111">Exemplo 1: criar um webhook do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="af4eb-111">Example 1: Create a container registry webhook.</span></span>
```
PS C:\> New-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -Uri http://www.bing.com -Action Delete,Push -Header @{SpecialHeader='headerVal'} -Tag @{Key="val"} -Location "east us" -Status Enabled -Scope "foo:*"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled    foo:*           {push, delete}  Succeeded
```

<span data-ttu-id="af4eb-112">Crie um webhook do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="af4eb-112">Create a container registry webhook.</span></span>

## <span data-ttu-id="af4eb-113">OS</span><span class="sxs-lookup"><span data-stu-id="af4eb-113">PARAMETERS</span></span>

### <span data-ttu-id="af4eb-114">-Ação</span><span class="sxs-lookup"><span data-stu-id="af4eb-114">-Action</span></span>
<span data-ttu-id="af4eb-115">Lista separada por espaço de ações que disparam o webhook para postar notificações.</span><span class="sxs-lookup"><span data-stu-id="af4eb-115">Space separated list of actions that trigger the webhook to post notifications.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: WebhookActions
Accepted values: delete, push

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af4eb-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="af4eb-116">-Confirm</span></span>
<span data-ttu-id="af4eb-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af4eb-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af4eb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af4eb-118">-DefaultProfile</span></span>
<span data-ttu-id="af4eb-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="af4eb-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af4eb-120">-Header</span><span class="sxs-lookup"><span data-stu-id="af4eb-120">-Header</span></span>
<span data-ttu-id="af4eb-121">Cabeçalhos personalizados que serão adicionados às notificações do webhook.</span><span class="sxs-lookup"><span data-stu-id="af4eb-121">Custom headers that will be added to the webhook notifications.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: WebhookHeaders

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af4eb-122">-Local</span><span class="sxs-lookup"><span data-stu-id="af4eb-122">-Location</span></span>
<span data-ttu-id="af4eb-123">Local do webhook.</span><span class="sxs-lookup"><span data-stu-id="af4eb-123">Webhook Location.</span></span>
<span data-ttu-id="af4eb-124">Padrão para o local do registro.</span><span class="sxs-lookup"><span data-stu-id="af4eb-124">Default to the location of the registry.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebhookLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af4eb-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="af4eb-125">-Name</span></span>
<span data-ttu-id="af4eb-126">Nome do webhook.</span><span class="sxs-lookup"><span data-stu-id="af4eb-126">Webhook Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebhookName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af4eb-127">-Registro</span><span class="sxs-lookup"><span data-stu-id="af4eb-127">-Registry</span></span>
<span data-ttu-id="af4eb-128">Objeto do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="af4eb-128">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af4eb-129">-Registryname</span><span class="sxs-lookup"><span data-stu-id="af4eb-129">-RegistryName</span></span>
<span data-ttu-id="af4eb-130">Nome do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="af4eb-130">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af4eb-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af4eb-131">-ResourceGroupName</span></span>
<span data-ttu-id="af4eb-132">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="af4eb-132">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af4eb-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="af4eb-133">-ResourceId</span></span>
<span data-ttu-id="af4eb-134">A ID do recurso do registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="af4eb-134">The container registry resource id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af4eb-135">-Escopo</span><span class="sxs-lookup"><span data-stu-id="af4eb-135">-Scope</span></span>
<span data-ttu-id="af4eb-136">Escopo do webhook.</span><span class="sxs-lookup"><span data-stu-id="af4eb-136">Webhook scope.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebhookScope

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af4eb-137">-Status</span><span class="sxs-lookup"><span data-stu-id="af4eb-137">-Status</span></span>
<span data-ttu-id="af4eb-138">Status do webhook, o valor padrão é habilitado</span><span class="sxs-lookup"><span data-stu-id="af4eb-138">Webhook status, default value is enabled</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebhookStatus
Accepted values: enabled, disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af4eb-139">-Marca</span><span class="sxs-lookup"><span data-stu-id="af4eb-139">-Tag</span></span>
<span data-ttu-id="af4eb-140">Marcas webhook.</span><span class="sxs-lookup"><span data-stu-id="af4eb-140">Webhook tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af4eb-141">-URI</span><span class="sxs-lookup"><span data-stu-id="af4eb-141">-Uri</span></span>
<span data-ttu-id="af4eb-142">O URI do serviço para o webhook para postar notificações.</span><span class="sxs-lookup"><span data-stu-id="af4eb-142">The service URI for the webhook to post notifications.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: WebhookUri

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af4eb-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af4eb-143">-WhatIf</span></span>
<span data-ttu-id="af4eb-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="af4eb-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af4eb-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="af4eb-145">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af4eb-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af4eb-146">CommonParameters</span></span>
<span data-ttu-id="af4eb-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af4eb-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af4eb-148">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af4eb-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af4eb-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="af4eb-149">INPUTS</span></span>

### <span data-ttu-id="af4eb-150">System. String</span><span class="sxs-lookup"><span data-stu-id="af4eb-150">System.String</span></span>

## <span data-ttu-id="af4eb-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="af4eb-151">OUTPUTS</span></span>

### <span data-ttu-id="af4eb-152">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="af4eb-152">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="af4eb-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="af4eb-153">NOTES</span></span>

## <span data-ttu-id="af4eb-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="af4eb-154">RELATED LINKS</span></span>

[<span data-ttu-id="af4eb-155">Get-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="af4eb-155">Get-AzureRmContainerRegistryWebhook</span></span>](Get-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="af4eb-156">Update-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="af4eb-156">Update-AzureRmContainerRegistryWebhook</span></span>](Update-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="af4eb-157">Remove-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="af4eb-157">Remove-AzureRmContainerRegistryWebhook</span></span>](Remove-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="af4eb-158">Test-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="af4eb-158">Test-AzureRmContainerRegistryWebhook</span></span>](Test-AzureRmContainerRegistryWebhook.md)
