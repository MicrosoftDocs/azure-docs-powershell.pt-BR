---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistrywebhookevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryWebhookEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryWebhookEvent.md
ms.openlocfilehash: b30df9c2cce1c4284085b683a06327e4c0ac3ab0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601182"
---
# <span data-ttu-id="a1593-101">Get-AzContainerRegistryWebhookEvent</span><span class="sxs-lookup"><span data-stu-id="a1593-101">Get-AzContainerRegistryWebhookEvent</span></span>

## <span data-ttu-id="a1593-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a1593-102">SYNOPSIS</span></span>
<span data-ttu-id="a1593-103">Obtém eventos de um webhook do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="a1593-103">Gets events of a container registry webhook.</span></span>

## <span data-ttu-id="a1593-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a1593-104">SYNTAX</span></span>

### <span data-ttu-id="a1593-105">ListWebhookEventsByNameResourceGroupParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="a1593-105">ListWebhookEventsByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryWebhookEvent [-WebhookName] <String> [-ResourceGroupName] <String>
 [-RegistryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1593-106">ListWebhookEventsByWebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1593-106">ListWebhookEventsByWebhookObjectParameterSet</span></span>
```
Get-AzContainerRegistryWebhookEvent -Webhook <PSContainerRegistryWebhook>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1593-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1593-107">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryWebhookEvent -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a1593-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a1593-108">DESCRIPTION</span></span>
<span data-ttu-id="a1593-109">O cmdlet Get-AzContainerRegistryWebhookEvent lista todos os eventos de um webhook.</span><span class="sxs-lookup"><span data-stu-id="a1593-109">The Get-AzContainerRegistryWebhookEvent cmdlet lists all the events of a webhook.</span></span>

## <span data-ttu-id="a1593-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a1593-110">EXAMPLES</span></span>

### <span data-ttu-id="a1593-111">Exemplo 1: Obtém todos os eventos de um webhook.</span><span class="sxs-lookup"><span data-stu-id="a1593-111">Example 1: Gets all the events of a webhook.</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhookEvent -ResourceGroupName mattacrtest001 -RegistryName premium001 -Name webhook001

   Webhook service Uri: http://www.bing.com/

ID                                       Action   Timestamp                      Response
                                                                                 StatusCode
--                                       ------   ---------                      ----------
3c6281b6-47cd-4129-948b-4036780236f0     ping     11/17/2017 5:10:09 PM          200
70f1d41d-15fe-4251-87b6-43c32a91eae7     ping     11/17/2017 6:56:23 AM          200
5d25556b-32d0-4377-8031-d8ba7a263d6a     ping     11/17/2017 6:27:41 AM          200
c1e7d8aa-9f1b-447c-9583-2a58b7f81026     ping     11/17/2017 12:09:41 AM         200
eb4aa503-0d14-4f25-8ae5-33cce9a8fd50     ping     11/16/2017 11:35:03 PM         200
85a93d7f-3923-4ec5-bb8e-9ded5b6549c1     ping     11/17/2017 5:10:09 PM          200
9e3c8b5f-e0ee-47cf-9727-df1c8d45a497     ping     11/17/2017 6:56:23 AM          200
2d0ce294-9b59-4f5c-953a-47f2b270526f     ping     11/17/2017 6:27:41 AM          200
```

<span data-ttu-id="a1593-112">Obtém todos os eventos de um webhook.</span><span class="sxs-lookup"><span data-stu-id="a1593-112">Gets all the events of a webhook.</span></span>

## <span data-ttu-id="a1593-113">OS</span><span class="sxs-lookup"><span data-stu-id="a1593-113">PARAMETERS</span></span>

### <span data-ttu-id="a1593-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1593-114">-DefaultProfile</span></span>
<span data-ttu-id="a1593-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a1593-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1593-116">-Registryname</span><span class="sxs-lookup"><span data-stu-id="a1593-116">-RegistryName</span></span>
<span data-ttu-id="a1593-117">Nome do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="a1593-117">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListWebhookEventsByNameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1593-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1593-118">-ResourceGroupName</span></span>
<span data-ttu-id="a1593-119">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a1593-119">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListWebhookEventsByNameResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1593-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1593-120">-ResourceId</span></span>
<span data-ttu-id="a1593-121">A ID do recurso de webhook do registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="a1593-121">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="a1593-122">-Webhook</span><span class="sxs-lookup"><span data-stu-id="a1593-122">-Webhook</span></span>
<span data-ttu-id="a1593-123">Objeto do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="a1593-123">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook
Parameter Sets: ListWebhookEventsByWebhookObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1593-124">-Webhookname</span><span class="sxs-lookup"><span data-stu-id="a1593-124">-WebhookName</span></span>
<span data-ttu-id="a1593-125">Nome do webhook.</span><span class="sxs-lookup"><span data-stu-id="a1593-125">Webhook Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListWebhookEventsByNameResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1593-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1593-126">CommonParameters</span></span>
<span data-ttu-id="a1593-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1593-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1593-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1593-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1593-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a1593-129">INPUTS</span></span>

### <span data-ttu-id="a1593-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a1593-130">System.String</span></span>

## <span data-ttu-id="a1593-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a1593-131">OUTPUTS</span></span>

### <span data-ttu-id="a1593-132">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhookEvent</span><span class="sxs-lookup"><span data-stu-id="a1593-132">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhookEvent</span></span>

## <span data-ttu-id="a1593-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a1593-133">NOTES</span></span>

## <span data-ttu-id="a1593-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a1593-134">RELATED LINKS</span></span>

[<span data-ttu-id="a1593-135">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="a1593-135">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="a1593-136">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="a1593-136">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="a1593-137">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="a1593-137">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="a1593-138">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="a1593-138">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)

[<span data-ttu-id="a1593-139">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="a1593-139">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)

