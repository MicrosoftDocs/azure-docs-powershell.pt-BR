---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryWebhook.md
ms.openlocfilehash: b01b2e8152d74fda5faff36221ffa9b6e75ffcbb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597131"
---
# <span data-ttu-id="65a7e-101">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="65a7e-101">Get-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="65a7e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="65a7e-102">SYNOPSIS</span></span>
<span data-ttu-id="65a7e-103">Obtém um webhook do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="65a7e-103">Gets a container registry webhook.</span></span>

## <span data-ttu-id="65a7e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="65a7e-104">SYNTAX</span></span>

### <span data-ttu-id="65a7e-105">ListWebhookByNameResourceGroupParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="65a7e-105">ListWebhookByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryWebhook [-ResourceGroupName] <String> [-RegistryName] <String> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="65a7e-106">ShowWebhookByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="65a7e-106">ShowWebhookByNameResourceGroupParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-IncludeConfiguration] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="65a7e-107">ShowWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="65a7e-107">ShowWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-Name] <String> -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="65a7e-108">ListWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="65a7e-108">ListWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryWebhook -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="65a7e-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="65a7e-109">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-IncludeConfiguration] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65a7e-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="65a7e-110">DESCRIPTION</span></span>
<span data-ttu-id="65a7e-111">O cmdlet Get-AzContainerRegistryWebhook Obtém um webhook do registro de contêiner especificado ou todos os WebHooks de um registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="65a7e-111">The Get-AzContainerRegistryWebhook cmdlet gets a specified webhook of container registry or all the webhooks of a container registry.</span></span>

## <span data-ttu-id="65a7e-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="65a7e-112">EXAMPLES</span></span>

### <span data-ttu-id="65a7e-113">Exemplo 1: obter um webhook especificado de um registro de contêiner</span><span class="sxs-lookup"><span data-stu-id="65a7e-113">Example 1: Get a specified webhook of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded
```

<span data-ttu-id="65a7e-114">Obter um webhook especificado de um registro de contêiner</span><span class="sxs-lookup"><span data-stu-id="65a7e-114">Get a specified webhook of a container registry</span></span>

### <span data-ttu-id="65a7e-115">Exemplo 2: obter todos os WebHooks de um registro de contêiner</span><span class="sxs-lookup"><span data-stu-id="65a7e-115">Example 2: Get all the webhooks of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook04       westus     enabled                    {push, delete}  Succeeded
webhook05       westus     disabled                   {push, delete}  Succeeded
wh003           westus     enabled                    delete          Succeeded
```

<span data-ttu-id="65a7e-116">Obter todos os WebHooks de um registro de contêiner</span><span class="sxs-lookup"><span data-stu-id="65a7e-116">Get all the webhooks of a container registry</span></span>

### <span data-ttu-id="65a7e-117">Exemplo 3: obter um webhook especificado de um registro de contêiner com detalhes de configuração</span><span class="sxs-lookup"><span data-stu-id="65a7e-117">Example 3: Get a specified webhook of a container registry with configuration details</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -IncludeConfiguration

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded  http://www.test.com/
```

<span data-ttu-id="65a7e-118">Obter um webhook especificado de um registro de contêiner com detalhes de configuração</span><span class="sxs-lookup"><span data-stu-id="65a7e-118">Get a specified webhook of a container registry with configuration details</span></span>

## <span data-ttu-id="65a7e-119">OS</span><span class="sxs-lookup"><span data-stu-id="65a7e-119">PARAMETERS</span></span>

### <span data-ttu-id="65a7e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65a7e-120">-DefaultProfile</span></span>
<span data-ttu-id="65a7e-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="65a7e-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65a7e-122">-IncludeConfiguration</span><span class="sxs-lookup"><span data-stu-id="65a7e-122">-IncludeConfiguration</span></span>
<span data-ttu-id="65a7e-123">Obter as informações de configuração de um webhook.</span><span class="sxs-lookup"><span data-stu-id="65a7e-123">Get the configuration information for a webhook.</span></span>

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

### <span data-ttu-id="65a7e-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="65a7e-124">-Name</span></span>
<span data-ttu-id="65a7e-125">Nome do webhook.</span><span class="sxs-lookup"><span data-stu-id="65a7e-125">Webhook Name.</span></span>

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

### <span data-ttu-id="65a7e-126">-Registro</span><span class="sxs-lookup"><span data-stu-id="65a7e-126">-Registry</span></span>
<span data-ttu-id="65a7e-127">Objeto do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="65a7e-127">Container Registry Object.</span></span>

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

### <span data-ttu-id="65a7e-128">-Registryname</span><span class="sxs-lookup"><span data-stu-id="65a7e-128">-RegistryName</span></span>
<span data-ttu-id="65a7e-129">Nome do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="65a7e-129">Container Registry Name.</span></span>

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

### <span data-ttu-id="65a7e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65a7e-130">-ResourceGroupName</span></span>
<span data-ttu-id="65a7e-131">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="65a7e-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="65a7e-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="65a7e-132">-ResourceId</span></span>
<span data-ttu-id="65a7e-133">A ID do recurso de webhook do registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="65a7e-133">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="65a7e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65a7e-134">CommonParameters</span></span>
<span data-ttu-id="65a7e-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65a7e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65a7e-136">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="65a7e-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65a7e-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="65a7e-137">INPUTS</span></span>

### <span data-ttu-id="65a7e-138">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="65a7e-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="65a7e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="65a7e-139">System.String</span></span>

## <span data-ttu-id="65a7e-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="65a7e-140">OUTPUTS</span></span>

### <span data-ttu-id="65a7e-141">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="65a7e-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="65a7e-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="65a7e-142">NOTES</span></span>

## <span data-ttu-id="65a7e-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="65a7e-143">RELATED LINKS</span></span>

[<span data-ttu-id="65a7e-144">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="65a7e-144">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="65a7e-145">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="65a7e-145">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="65a7e-146">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="65a7e-146">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)

[<span data-ttu-id="65a7e-147">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="65a7e-147">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)