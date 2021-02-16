---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/test-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryWebhook.md
ms.openlocfilehash: 1245c92e13af691b0b439d6745a35a917bdf4d89
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127050"
---
# <span data-ttu-id="66831-101">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="66831-101">Test-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="66831-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="66831-102">SYNOPSIS</span></span>
<span data-ttu-id="66831-103">Aciona um evento de ping web browser.</span><span class="sxs-lookup"><span data-stu-id="66831-103">Triggers a webhook ping event.</span></span>

## <span data-ttu-id="66831-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="66831-104">SYNTAX</span></span>

### <span data-ttu-id="66831-105">ResourceIdParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="66831-105">ResourceIdParameterSet (Default)</span></span>
```
Test-AzContainerRegistryWebhook -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="66831-106">NameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="66831-106">NameResourceGroupParameterSet</span></span>
```
Test-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66831-107">WebbjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="66831-107">WebhookObjectParameterSet</span></span>
```
Test-AzContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66831-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="66831-108">DESCRIPTION</span></span>
<span data-ttu-id="66831-109">O Test-AzContainerRegistryWebhook cmdlet aciona um evento de ping web ressíntegro.</span><span class="sxs-lookup"><span data-stu-id="66831-109">The Test-AzContainerRegistryWebhook cmdlet triggers a webhook ping event.</span></span>

## <span data-ttu-id="66831-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="66831-110">EXAMPLES</span></span>

### <span data-ttu-id="66831-111">Exemplo 1: dispara um evento de ping web rede.</span><span class="sxs-lookup"><span data-stu-id="66831-111">Example 1: Triggers a webhook ping event.</span></span>
```powershell
PS C:\> Test-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Id
--
c5950af0-c8d0-4924-9873-1ba7da5cbf83
```

<span data-ttu-id="66831-112">Aciona um evento de ping web browser.</span><span class="sxs-lookup"><span data-stu-id="66831-112">Triggers a webhook ping event.</span></span>

## <span data-ttu-id="66831-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="66831-113">PARAMETERS</span></span>

### <span data-ttu-id="66831-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66831-114">-DefaultProfile</span></span>
<span data-ttu-id="66831-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="66831-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66831-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="66831-116">-Name</span></span>
<span data-ttu-id="66831-117">Nome Web browser.</span><span class="sxs-lookup"><span data-stu-id="66831-117">Webhook Name.</span></span>

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

### <span data-ttu-id="66831-118">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="66831-118">-RegistryName</span></span>
<span data-ttu-id="66831-119">Nome do Registro do Contêiner.</span><span class="sxs-lookup"><span data-stu-id="66831-119">Container Registry Name.</span></span>

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

### <span data-ttu-id="66831-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66831-120">-ResourceGroupName</span></span>
<span data-ttu-id="66831-121">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="66831-121">Resource Group Name.</span></span>

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

### <span data-ttu-id="66831-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="66831-122">-ResourceId</span></span>
<span data-ttu-id="66831-123">A ID de recurso Web browser do registro de contêineres</span><span class="sxs-lookup"><span data-stu-id="66831-123">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="66831-124">-Web browser</span><span class="sxs-lookup"><span data-stu-id="66831-124">-Webhook</span></span>
<span data-ttu-id="66831-125">Objeto do Registro de Contêineres.</span><span class="sxs-lookup"><span data-stu-id="66831-125">Container Registry Object.</span></span>

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

### <span data-ttu-id="66831-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66831-126">CommonParameters</span></span>
<span data-ttu-id="66831-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66831-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66831-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="66831-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66831-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="66831-129">INPUTS</span></span>

### <span data-ttu-id="66831-130">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebweb</span><span class="sxs-lookup"><span data-stu-id="66831-130">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

### <span data-ttu-id="66831-131">System.String</span><span class="sxs-lookup"><span data-stu-id="66831-131">System.String</span></span>

## <span data-ttu-id="66831-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="66831-132">OUTPUTS</span></span>

### <span data-ttu-id="66831-133">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryEventInfo</span><span class="sxs-lookup"><span data-stu-id="66831-133">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryEventInfo</span></span>

## <span data-ttu-id="66831-134">Notas</span><span class="sxs-lookup"><span data-stu-id="66831-134">NOTES</span></span>

## <span data-ttu-id="66831-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="66831-135">RELATED LINKS</span></span>

[<span data-ttu-id="66831-136">New-AzContainerRegistryWebweb</span><span class="sxs-lookup"><span data-stu-id="66831-136">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="66831-137">Get-AzContainerRegistryWebweb</span><span class="sxs-lookup"><span data-stu-id="66831-137">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="66831-138">Update-AzContainerRegistryWebweb</span><span class="sxs-lookup"><span data-stu-id="66831-138">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="66831-139">Remove-AzContainerRegistryWebweb</span><span class="sxs-lookup"><span data-stu-id="66831-139">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)