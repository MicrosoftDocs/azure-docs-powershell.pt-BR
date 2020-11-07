---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/test-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryWebhook.md
ms.openlocfilehash: 1245c92e13af691b0b439d6745a35a917bdf4d89
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777550"
---
# <span data-ttu-id="df317-101">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="df317-101">Test-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="df317-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="df317-102">SYNOPSIS</span></span>
<span data-ttu-id="df317-103">Dispara um evento ping do webhook.</span><span class="sxs-lookup"><span data-stu-id="df317-103">Triggers a webhook ping event.</span></span>

## <span data-ttu-id="df317-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="df317-104">SYNTAX</span></span>

### <span data-ttu-id="df317-105">ResourceIdParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="df317-105">ResourceIdParameterSet (Default)</span></span>
```
Test-AzContainerRegistryWebhook -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="df317-106">NameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="df317-106">NameResourceGroupParameterSet</span></span>
```
Test-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df317-107">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="df317-107">WebhookObjectParameterSet</span></span>
```
Test-AzContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df317-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="df317-108">DESCRIPTION</span></span>
<span data-ttu-id="df317-109">O cmdlet Test-AzContainerRegistryWebhook aciona um evento ping do webhook.</span><span class="sxs-lookup"><span data-stu-id="df317-109">The Test-AzContainerRegistryWebhook cmdlet triggers a webhook ping event.</span></span>

## <span data-ttu-id="df317-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="df317-110">EXAMPLES</span></span>

### <span data-ttu-id="df317-111">Exemplo 1: dispara um evento ping do webhook.</span><span class="sxs-lookup"><span data-stu-id="df317-111">Example 1: Triggers a webhook ping event.</span></span>
```powershell
PS C:\> Test-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Id
--
c5950af0-c8d0-4924-9873-1ba7da5cbf83
```

<span data-ttu-id="df317-112">Dispara um evento ping do webhook.</span><span class="sxs-lookup"><span data-stu-id="df317-112">Triggers a webhook ping event.</span></span>

## <span data-ttu-id="df317-113">OS</span><span class="sxs-lookup"><span data-stu-id="df317-113">PARAMETERS</span></span>

### <span data-ttu-id="df317-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df317-114">-DefaultProfile</span></span>
<span data-ttu-id="df317-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="df317-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df317-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="df317-116">-Name</span></span>
<span data-ttu-id="df317-117">Nome do webhook.</span><span class="sxs-lookup"><span data-stu-id="df317-117">Webhook Name.</span></span>

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

### <span data-ttu-id="df317-118">-Registryname</span><span class="sxs-lookup"><span data-stu-id="df317-118">-RegistryName</span></span>
<span data-ttu-id="df317-119">Nome do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="df317-119">Container Registry Name.</span></span>

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

### <span data-ttu-id="df317-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df317-120">-ResourceGroupName</span></span>
<span data-ttu-id="df317-121">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="df317-121">Resource Group Name.</span></span>

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

### <span data-ttu-id="df317-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="df317-122">-ResourceId</span></span>
<span data-ttu-id="df317-123">A ID do recurso de webhook do registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="df317-123">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="df317-124">-Webhook</span><span class="sxs-lookup"><span data-stu-id="df317-124">-Webhook</span></span>
<span data-ttu-id="df317-125">Objeto do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="df317-125">Container Registry Object.</span></span>

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

### <span data-ttu-id="df317-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df317-126">CommonParameters</span></span>
<span data-ttu-id="df317-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df317-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df317-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="df317-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df317-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="df317-129">INPUTS</span></span>

### <span data-ttu-id="df317-130">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="df317-130">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

### <span data-ttu-id="df317-131">System. String</span><span class="sxs-lookup"><span data-stu-id="df317-131">System.String</span></span>

## <span data-ttu-id="df317-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="df317-132">OUTPUTS</span></span>

### <span data-ttu-id="df317-133">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryEventInfo</span><span class="sxs-lookup"><span data-stu-id="df317-133">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryEventInfo</span></span>

## <span data-ttu-id="df317-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="df317-134">NOTES</span></span>

## <span data-ttu-id="df317-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="df317-135">RELATED LINKS</span></span>

[<span data-ttu-id="df317-136">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="df317-136">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="df317-137">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="df317-137">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="df317-138">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="df317-138">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="df317-139">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="df317-139">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)