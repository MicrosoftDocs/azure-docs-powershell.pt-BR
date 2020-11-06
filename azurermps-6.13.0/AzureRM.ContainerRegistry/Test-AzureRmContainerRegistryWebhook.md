---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/test-azurermcontainerregistrynameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryWebhook.md
ms.openlocfilehash: 0a5894a411f4ffb5b3bde28db68961d321584e1d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602314"
---
# <span data-ttu-id="8f903-101">Test-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="8f903-101">Test-AzureRmContainerRegistryWebhook</span></span>

## <span data-ttu-id="8f903-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8f903-102">SYNOPSIS</span></span>
<span data-ttu-id="8f903-103">Dispara um evento ping do webhook.</span><span class="sxs-lookup"><span data-stu-id="8f903-103">Triggers a webhook ping event.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f903-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8f903-104">SYNTAX</span></span>

### <span data-ttu-id="8f903-105">ResourceIdParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="8f903-105">ResourceIdParameterSet (Default)</span></span>
```
Test-AzureRmContainerRegistryWebhook -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8f903-106">NameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f903-106">NameResourceGroupParameterSet</span></span>
```
Test-AzureRmContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f903-107">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f903-107">WebhookObjectParameterSet</span></span>
```
Test-AzureRmContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f903-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8f903-108">DESCRIPTION</span></span>
<span data-ttu-id="8f903-109">O cmdlet Test-AzureRmContainerRegistryWebhook aciona um evento ping do webhook.</span><span class="sxs-lookup"><span data-stu-id="8f903-109">The Test-AzureRmContainerRegistryWebhook cmdlet triggers a webhook ping event.</span></span>

## <span data-ttu-id="8f903-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8f903-110">EXAMPLES</span></span>

### <span data-ttu-id="8f903-111">Exemplo 1: dispara um evento ping do webhook.</span><span class="sxs-lookup"><span data-stu-id="8f903-111">Example 1: Triggers a webhook ping event.</span></span>
```powershell
PS C:\> Test-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Id
--
c5950af0-c8d0-4924-9873-1ba7da5cbf83
```

<span data-ttu-id="8f903-112">Dispara um evento ping do webhook.</span><span class="sxs-lookup"><span data-stu-id="8f903-112">Triggers a webhook ping event.</span></span>

## <span data-ttu-id="8f903-113">OS</span><span class="sxs-lookup"><span data-stu-id="8f903-113">PARAMETERS</span></span>

### <span data-ttu-id="8f903-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f903-114">-DefaultProfile</span></span>
<span data-ttu-id="8f903-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8f903-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f903-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="8f903-116">-Name</span></span>
<span data-ttu-id="8f903-117">Nome do webhook.</span><span class="sxs-lookup"><span data-stu-id="8f903-117">Webhook Name.</span></span>

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

### <span data-ttu-id="8f903-118">-Registryname</span><span class="sxs-lookup"><span data-stu-id="8f903-118">-RegistryName</span></span>
<span data-ttu-id="8f903-119">Nome do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="8f903-119">Container Registry Name.</span></span>

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

### <span data-ttu-id="8f903-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f903-120">-ResourceGroupName</span></span>
<span data-ttu-id="8f903-121">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8f903-121">Resource Group Name.</span></span>

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

### <span data-ttu-id="8f903-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8f903-122">-ResourceId</span></span>
<span data-ttu-id="8f903-123">A ID do recurso de webhook do registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="8f903-123">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="8f903-124">-Webhook</span><span class="sxs-lookup"><span data-stu-id="8f903-124">-Webhook</span></span>
<span data-ttu-id="8f903-125">Objeto do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="8f903-125">Container Registry Object.</span></span>

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

### <span data-ttu-id="8f903-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f903-126">CommonParameters</span></span>
<span data-ttu-id="8f903-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f903-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f903-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f903-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f903-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8f903-129">INPUTS</span></span>

### <span data-ttu-id="8f903-130">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="8f903-130">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>
<span data-ttu-id="8f903-131">Parâmetros: webhook (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8f903-131">Parameters: Webhook (ByValue)</span></span>

### <span data-ttu-id="8f903-132">System. String</span><span class="sxs-lookup"><span data-stu-id="8f903-132">System.String</span></span>

## <span data-ttu-id="8f903-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8f903-133">OUTPUTS</span></span>

### <span data-ttu-id="8f903-134">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryEventInfo</span><span class="sxs-lookup"><span data-stu-id="8f903-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryEventInfo</span></span>

## <span data-ttu-id="8f903-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8f903-135">NOTES</span></span>

## <span data-ttu-id="8f903-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8f903-136">RELATED LINKS</span></span>

[<span data-ttu-id="8f903-137">New-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="8f903-137">New-AzureRmContainerRegistryWebhook</span></span>](New-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="8f903-138">Get-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="8f903-138">Get-AzureRmContainerRegistryWebhook</span></span>](Get-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="8f903-139">Update-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="8f903-139">Update-AzureRmContainerRegistryWebhook</span></span>](Update-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="8f903-140">Remove-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="8f903-140">Remove-AzureRmContainerRegistryWebhook</span></span>](Remove-AzureRmContainerRegistryWebhook.md)
