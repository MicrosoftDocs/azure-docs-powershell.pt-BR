---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryWebhook.md
ms.openlocfilehash: 231ff710e2c8c2945947ecf2d09845e635ee6244
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112084"
---
# <span data-ttu-id="e992c-101">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="e992c-101">Get-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="e992c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e992c-102">SYNOPSIS</span></span>
<span data-ttu-id="e992c-103">Obtém um contêiner da Web de registro.</span><span class="sxs-lookup"><span data-stu-id="e992c-103">Gets a container registry webhook.</span></span>

## <span data-ttu-id="e992c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e992c-104">SYNTAX</span></span>

### <span data-ttu-id="e992c-105">ListWebwebwebbyNameResourceGroupParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e992c-105">ListWebhookByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryWebhook [-ResourceGroupName] <String> [-RegistryName] <String> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e992c-106">ShowWebwebbyNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="e992c-106">ShowWebhookByNameResourceGroupParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-IncludeConfiguration] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e992c-107">MostrarWebwebwebbyRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e992c-107">ShowWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-Name] <String> -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e992c-108">ListWebwebwebbyRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e992c-108">ListWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryWebhook -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e992c-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e992c-109">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-IncludeConfiguration] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e992c-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="e992c-110">DESCRIPTION</span></span>
<span data-ttu-id="e992c-111">O Get-AzContainerRegistryWebhook cmdlet obtém uma web seta especificada de registro de contêiner ou todas as webções de um registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="e992c-111">The Get-AzContainerRegistryWebhook cmdlet gets a specified webhook of container registry or all the webhooks of a container registry.</span></span>

## <span data-ttu-id="e992c-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e992c-112">EXAMPLES</span></span>

### <span data-ttu-id="e992c-113">Exemplo 1: Obter uma web primeira página especificada de um registro de contêineres</span><span class="sxs-lookup"><span data-stu-id="e992c-113">Example 1: Get a specified webhook of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded
```

<span data-ttu-id="e992c-114">Obter uma web seções especificadas de um registro de contêineres</span><span class="sxs-lookup"><span data-stu-id="e992c-114">Get a specified webhook of a container registry</span></span>

### <span data-ttu-id="e992c-115">Exemplo 2: Obter todas as webções de um registro de contêineres</span><span class="sxs-lookup"><span data-stu-id="e992c-115">Example 2: Get all the webhooks of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook04       westus     enabled                    {push, delete}  Succeeded
webhook05       westus     disabled                   {push, delete}  Succeeded
wh003           westus     enabled                    delete          Succeeded
```

<span data-ttu-id="e992c-116">Obter todas as webções de um registro de contêiner</span><span class="sxs-lookup"><span data-stu-id="e992c-116">Get all the webhooks of a container registry</span></span>

### <span data-ttu-id="e992c-117">Exemplo 3: Obter uma web primeira página especificada de um registro de contêiner com detalhes de configuração</span><span class="sxs-lookup"><span data-stu-id="e992c-117">Example 3: Get a specified webhook of a container registry with configuration details</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -IncludeConfiguration

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded  http://www.test.com/
```

<span data-ttu-id="e992c-118">Obter uma webiáo especificada de um registro de contêiner com detalhes de configuração</span><span class="sxs-lookup"><span data-stu-id="e992c-118">Get a specified webhook of a container registry with configuration details</span></span>

## <span data-ttu-id="e992c-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e992c-119">PARAMETERS</span></span>

### <span data-ttu-id="e992c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e992c-120">-DefaultProfile</span></span>
<span data-ttu-id="e992c-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="e992c-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e992c-122">-IncludeConfiguration</span><span class="sxs-lookup"><span data-stu-id="e992c-122">-IncludeConfiguration</span></span>
<span data-ttu-id="e992c-123">Obter as informações de configuração de um web browser.</span><span class="sxs-lookup"><span data-stu-id="e992c-123">Get the configuration information for a webhook.</span></span>

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

### <span data-ttu-id="e992c-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="e992c-124">-Name</span></span>
<span data-ttu-id="e992c-125">Nome Web browser.</span><span class="sxs-lookup"><span data-stu-id="e992c-125">Webhook Name.</span></span>

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

### <span data-ttu-id="e992c-126">-Registro</span><span class="sxs-lookup"><span data-stu-id="e992c-126">-Registry</span></span>
<span data-ttu-id="e992c-127">Objeto do Registro de Contêineres.</span><span class="sxs-lookup"><span data-stu-id="e992c-127">Container Registry Object.</span></span>

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

### <span data-ttu-id="e992c-128">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="e992c-128">-RegistryName</span></span>
<span data-ttu-id="e992c-129">Nome do Registro do Contêiner.</span><span class="sxs-lookup"><span data-stu-id="e992c-129">Container Registry Name.</span></span>

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

### <span data-ttu-id="e992c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e992c-130">-ResourceGroupName</span></span>
<span data-ttu-id="e992c-131">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e992c-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="e992c-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e992c-132">-ResourceId</span></span>
<span data-ttu-id="e992c-133">A ID de recurso Web browser do registro de contêineres</span><span class="sxs-lookup"><span data-stu-id="e992c-133">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="e992c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e992c-134">CommonParameters</span></span>
<span data-ttu-id="e992c-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e992c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e992c-136">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e992c-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e992c-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="e992c-137">INPUTS</span></span>

### <span data-ttu-id="e992c-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e992c-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="e992c-139">System.String</span><span class="sxs-lookup"><span data-stu-id="e992c-139">System.String</span></span>

## <span data-ttu-id="e992c-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="e992c-140">OUTPUTS</span></span>

### <span data-ttu-id="e992c-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebweb</span><span class="sxs-lookup"><span data-stu-id="e992c-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="e992c-142">Notas</span><span class="sxs-lookup"><span data-stu-id="e992c-142">NOTES</span></span>

## <span data-ttu-id="e992c-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e992c-143">RELATED LINKS</span></span>

[<span data-ttu-id="e992c-144">New-AzContainerRegistryWebweb</span><span class="sxs-lookup"><span data-stu-id="e992c-144">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="e992c-145">Update-AzContainerRegistryWebweb</span><span class="sxs-lookup"><span data-stu-id="e992c-145">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="e992c-146">Remove-AzContainerRegistryWebweb</span><span class="sxs-lookup"><span data-stu-id="e992c-146">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)

[<span data-ttu-id="e992c-147">Test-AzContainerRegistryWebweb</span><span class="sxs-lookup"><span data-stu-id="e992c-147">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)