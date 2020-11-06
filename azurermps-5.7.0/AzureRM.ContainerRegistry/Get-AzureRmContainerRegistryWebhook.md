---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/get-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryWebhook.md
ms.openlocfilehash: 4f20f177b172ab9b5372de6b95d821202e991000
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428964"
---
# <span data-ttu-id="69f43-101">Get-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="69f43-101">Get-AzureRmContainerRegistryWebhook</span></span>

## <span data-ttu-id="69f43-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="69f43-102">SYNOPSIS</span></span>
<span data-ttu-id="69f43-103">Obtém um webhook do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="69f43-103">Gets a container registry webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69f43-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="69f43-104">SYNTAX</span></span>

### <span data-ttu-id="69f43-105">ListWebhookByNameResourceGroupParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="69f43-105">ListWebhookByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistryWebhook [-ResourceGroupName] <String> [-RegistryName] <String>
 [-IncludeConfiguration] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69f43-106">ShowWebhookByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="69f43-106">ShowWebhookByNameResourceGroupParameterSet</span></span>
```
Get-AzureRmContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-IncludeConfiguration] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69f43-107">ShowWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="69f43-107">ShowWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryWebhook [-Name] <String> -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69f43-108">ListWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="69f43-108">ListWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryWebhook -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69f43-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="69f43-109">ResourceIdParameterSet</span></span>
```
Get-AzureRmContainerRegistryWebhook [-IncludeConfiguration] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69f43-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="69f43-110">DESCRIPTION</span></span>
<span data-ttu-id="69f43-111">O cmdlet Get-AzureRmContainerRegistryWebhook Obtém um webhook do registro de contêiner especificado ou todos os WebHooks de um registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="69f43-111">The Get-AzureRmContainerRegistryWebhook cmdlet gets a specified webhook of container registry or all the webhooks of a container registry.</span></span>

## <span data-ttu-id="69f43-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="69f43-112">EXAMPLES</span></span>

### <span data-ttu-id="69f43-113">Exemplo 1: obter um webhook especificado de um registro de contêiner</span><span class="sxs-lookup"><span data-stu-id="69f43-113">Example 1: Get a specified webhook of a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded
```

<span data-ttu-id="69f43-114">Obter um webhook especificado de um registro de contêiner</span><span class="sxs-lookup"><span data-stu-id="69f43-114">Get a specified webhook of a container registry</span></span>

### <span data-ttu-id="69f43-115">Exemplo 2: obter todos os WebHooks de um registro de contêiner</span><span class="sxs-lookup"><span data-stu-id="69f43-115">Example 2: Get all the webhooks of a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook04       westus     enabled                    {push, delete}  Succeeded
webhook05       westus     disabled                   {push, delete}  Succeeded
wh003           westus     enabled                    delete          Succeeded
```

<span data-ttu-id="69f43-116">Obter todos os WebHooks de um registro de contêiner</span><span class="sxs-lookup"><span data-stu-id="69f43-116">Get all the webhooks of a container registry</span></span>

### <span data-ttu-id="69f43-117">Exemplo 3: obter um webhook especificado de um registro de contêiner com detalhes de configuração</span><span class="sxs-lookup"><span data-stu-id="69f43-117">Example 3: Get a specified webhook of a container registry with configuration details</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -IncludeConfiguration

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded  http://www.test.com/
```

<span data-ttu-id="69f43-118">Obter um webhook especificado de um registro de contêiner com detalhes de configuração</span><span class="sxs-lookup"><span data-stu-id="69f43-118">Get a specified webhook of a container registry with configuration details</span></span>

## <span data-ttu-id="69f43-119">OS</span><span class="sxs-lookup"><span data-stu-id="69f43-119">PARAMETERS</span></span>

### <span data-ttu-id="69f43-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69f43-120">-DefaultProfile</span></span>
<span data-ttu-id="69f43-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="69f43-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69f43-122">-IncludeConfiguration</span><span class="sxs-lookup"><span data-stu-id="69f43-122">-IncludeConfiguration</span></span>
<span data-ttu-id="69f43-123">Obter as informações de configuração de um webhook.</span><span class="sxs-lookup"><span data-stu-id="69f43-123">Get the configuration information for a webhook.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69f43-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="69f43-124">-Name</span></span>
<span data-ttu-id="69f43-125">Nome do webhook.</span><span class="sxs-lookup"><span data-stu-id="69f43-125">Webhook Name.</span></span>

```yaml
Type: String
Parameter Sets: ShowWebhookByNameResourceGroupParameterSet, ShowWebhookByRegistryObjectParameterSet
Aliases: WebhookName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69f43-126">-Registro</span><span class="sxs-lookup"><span data-stu-id="69f43-126">-Registry</span></span>
<span data-ttu-id="69f43-127">Objeto do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="69f43-127">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistry
Parameter Sets: ShowWebhookByRegistryObjectParameterSet, ListWebhookByRegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69f43-128">-Registryname</span><span class="sxs-lookup"><span data-stu-id="69f43-128">-RegistryName</span></span>
<span data-ttu-id="69f43-129">Nome do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="69f43-129">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: ListWebhookByNameResourceGroupParameterSet, ShowWebhookByNameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69f43-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69f43-130">-ResourceGroupName</span></span>
<span data-ttu-id="69f43-131">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="69f43-131">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ListWebhookByNameResourceGroupParameterSet, ShowWebhookByNameResourceGroupParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69f43-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="69f43-132">-ResourceId</span></span>
<span data-ttu-id="69f43-133">A ID do recurso de webhook do registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="69f43-133">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="69f43-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69f43-134">CommonParameters</span></span>
<span data-ttu-id="69f43-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69f43-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69f43-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69f43-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69f43-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="69f43-137">INPUTS</span></span>

### <span data-ttu-id="69f43-138">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="69f43-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>
<span data-ttu-id="69f43-139">System. String</span><span class="sxs-lookup"><span data-stu-id="69f43-139">System.String</span></span>

## <span data-ttu-id="69f43-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="69f43-140">OUTPUTS</span></span>

### <span data-ttu-id="69f43-141">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="69f43-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>
<span data-ttu-id="69f43-142">System. Collections. Generic. IList ' 1 [[Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook, Microsoft. Azure. Commands. ContainerRegistry, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="69f43-142">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook, Microsoft.Azure.Commands.ContainerRegistry, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="69f43-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="69f43-143">NOTES</span></span>

## <span data-ttu-id="69f43-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="69f43-144">RELATED LINKS</span></span>

[<span data-ttu-id="69f43-145">New-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="69f43-145">New-AzureRmContainerRegistryWebhook</span></span>](New-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="69f43-146">Update-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="69f43-146">Update-AzureRmContainerRegistryWebhook</span></span>](Update-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="69f43-147">Remove-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="69f43-147">Remove-AzureRmContainerRegistryWebhook</span></span>](Remove-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="69f43-148">Test-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="69f43-148">Test-AzureRmContainerRegistryWebhook</span></span>](Test-AzureRmContainerRegistryWebhook.md)
