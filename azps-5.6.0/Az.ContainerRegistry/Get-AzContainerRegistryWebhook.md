---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/get-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryWebhook.md
ms.openlocfilehash: 36bc713561c739804b358e4b778e17740bd9fb6a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888570"
---
# <span data-ttu-id="4eb54-101">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="4eb54-101">Get-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="4eb54-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4eb54-102">SYNOPSIS</span></span>
<span data-ttu-id="4eb54-103">Obtém um webhook de registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="4eb54-103">Gets a container registry webhook.</span></span>

## <span data-ttu-id="4eb54-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4eb54-104">SYNTAX</span></span>

### <span data-ttu-id="4eb54-105">ListWebhookByNameResourceGroupParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4eb54-105">ListWebhookByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryWebhook [-ResourceGroupName] <String> [-RegistryName] <String> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4eb54-106">ShowWebhookByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="4eb54-106">ShowWebhookByNameResourceGroupParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-IncludeConfiguration] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4eb54-107">ShowWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4eb54-107">ShowWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-Name] <String> -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4eb54-108">ListWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4eb54-108">ListWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryWebhook -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4eb54-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4eb54-109">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-IncludeConfiguration] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4eb54-110">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4eb54-110">DESCRIPTION</span></span>
<span data-ttu-id="4eb54-111">O Get-AzContainerRegistryWebhook cmdlet obtém um webhook especificado do registro de contêiner ou todos os webhooks de um registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="4eb54-111">The Get-AzContainerRegistryWebhook cmdlet gets a specified webhook of container registry or all the webhooks of a container registry.</span></span>

## <span data-ttu-id="4eb54-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4eb54-112">EXAMPLES</span></span>

### <span data-ttu-id="4eb54-113">Exemplo 1: Obter um webhook especificado de um registro de contêiner</span><span class="sxs-lookup"><span data-stu-id="4eb54-113">Example 1: Get a specified webhook of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded
```

<span data-ttu-id="4eb54-114">Obter um webhook especificado de um registro de contêiner</span><span class="sxs-lookup"><span data-stu-id="4eb54-114">Get a specified webhook of a container registry</span></span>

### <span data-ttu-id="4eb54-115">Exemplo 2: Obter todos os webhooks de um registro de contêiner</span><span class="sxs-lookup"><span data-stu-id="4eb54-115">Example 2: Get all the webhooks of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook04       westus     enabled                    {push, delete}  Succeeded
webhook05       westus     disabled                   {push, delete}  Succeeded
wh003           westus     enabled                    delete          Succeeded
```

<span data-ttu-id="4eb54-116">Obter todos os webhooks de um registro de contêiner</span><span class="sxs-lookup"><span data-stu-id="4eb54-116">Get all the webhooks of a container registry</span></span>

### <span data-ttu-id="4eb54-117">Exemplo 3: Obter um webhook especificado de um registro de contêiner com detalhes de configuração</span><span class="sxs-lookup"><span data-stu-id="4eb54-117">Example 3: Get a specified webhook of a container registry with configuration details</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -IncludeConfiguration

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded  http://www.test.com/
```

<span data-ttu-id="4eb54-118">Obter um webhook especificado de um registro de contêiner com detalhes de configuração</span><span class="sxs-lookup"><span data-stu-id="4eb54-118">Get a specified webhook of a container registry with configuration details</span></span>

## <span data-ttu-id="4eb54-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4eb54-119">PARAMETERS</span></span>

### <span data-ttu-id="4eb54-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4eb54-120">-DefaultProfile</span></span>
<span data-ttu-id="4eb54-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="4eb54-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4eb54-122">-IncludeConfiguration</span><span class="sxs-lookup"><span data-stu-id="4eb54-122">-IncludeConfiguration</span></span>
<span data-ttu-id="4eb54-123">Obter as informações de configuração para um webhook.</span><span class="sxs-lookup"><span data-stu-id="4eb54-123">Get the configuration information for a webhook.</span></span>

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

### <span data-ttu-id="4eb54-124">-Name</span><span class="sxs-lookup"><span data-stu-id="4eb54-124">-Name</span></span>
<span data-ttu-id="4eb54-125">Nome do webhook.</span><span class="sxs-lookup"><span data-stu-id="4eb54-125">Webhook Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ShowWebhookByNameResourceGroupParameterSet, ShowWebhookByRegistryObjectParameterSet
Aliases: WebhookName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eb54-126">-Registry</span><span class="sxs-lookup"><span data-stu-id="4eb54-126">-Registry</span></span>
<span data-ttu-id="4eb54-127">Objeto Container Registry.</span><span class="sxs-lookup"><span data-stu-id="4eb54-127">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: ShowWebhookByRegistryObjectParameterSet, ListWebhookByRegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4eb54-128">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="4eb54-128">-RegistryName</span></span>
<span data-ttu-id="4eb54-129">Nome do Registro do Contêiner.</span><span class="sxs-lookup"><span data-stu-id="4eb54-129">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListWebhookByNameResourceGroupParameterSet, ShowWebhookByNameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eb54-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4eb54-130">-ResourceGroupName</span></span>
<span data-ttu-id="4eb54-131">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="4eb54-131">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListWebhookByNameResourceGroupParameterSet, ShowWebhookByNameResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eb54-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4eb54-132">-ResourceId</span></span>
<span data-ttu-id="4eb54-133">A ID do recurso Webhook do registro de contêiner</span><span class="sxs-lookup"><span data-stu-id="4eb54-133">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="4eb54-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4eb54-134">CommonParameters</span></span>
<span data-ttu-id="4eb54-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4eb54-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4eb54-136">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4eb54-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4eb54-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4eb54-137">INPUTS</span></span>

### <span data-ttu-id="4eb54-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="4eb54-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="4eb54-139">System.String</span><span class="sxs-lookup"><span data-stu-id="4eb54-139">System.String</span></span>

## <span data-ttu-id="4eb54-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4eb54-140">OUTPUTS</span></span>

### <span data-ttu-id="4eb54-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="4eb54-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="4eb54-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="4eb54-142">NOTES</span></span>

## <span data-ttu-id="4eb54-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4eb54-143">RELATED LINKS</span></span>

[<span data-ttu-id="4eb54-144">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="4eb54-144">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="4eb54-145">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="4eb54-145">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="4eb54-146">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="4eb54-146">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)

[<span data-ttu-id="4eb54-147">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="4eb54-147">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)