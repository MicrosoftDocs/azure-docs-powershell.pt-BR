---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/approve-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Approve-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Approve-AzPrivateEndpointConnection.md
ms.openlocfilehash: 3768bc8769d81056dc8f2de4f42f9f1783f89728
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888841"
---
# <span data-ttu-id="e504b-101">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e504b-101">Approve-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="e504b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e504b-102">SYNOPSIS</span></span>
<span data-ttu-id="e504b-103">Aprova uma conexão de ponto de extremidade privada.</span><span class="sxs-lookup"><span data-stu-id="e504b-103">Approves a private endpoint connection.</span></span>

## <span data-ttu-id="e504b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e504b-104">SYNTAX</span></span>

### <span data-ttu-id="e504b-105">ByResourceId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e504b-105">ByResourceId (Default)</span></span>
```
Approve-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e504b-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="e504b-106">ByResource</span></span>
```
Approve-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-PrivateLinkResourceType <string>][-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e504b-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e504b-107">DESCRIPTION</span></span>
<span data-ttu-id="e504b-108">O cmdlet **Approve-AzPrivateEndpointConnection** aprova uma conexão de ponto de extremidade privada.</span><span class="sxs-lookup"><span data-stu-id="e504b-108">The **Approve-AzPrivateEndpointConnection** cmdlet approves a private endpoint connection.</span></span>

## <span data-ttu-id="e504b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e504b-109">EXAMPLES</span></span>

### <span data-ttu-id="e504b-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e504b-110">Example 1</span></span>
```
Approve-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService
```

<span data-ttu-id="e504b-111">Este exemplo aprova uma conexão de ponto de extremidade privada.</span><span class="sxs-lookup"><span data-stu-id="e504b-111">This example approves a private endpoint connection.</span></span>

## <span data-ttu-id="e504b-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e504b-112">PARAMETERS</span></span>

### <span data-ttu-id="e504b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e504b-113">-DefaultProfile</span></span>
<span data-ttu-id="e504b-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e504b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e504b-115">-Description</span><span class="sxs-lookup"><span data-stu-id="e504b-115">-Description</span></span>
<span data-ttu-id="e504b-116">O motivo da ação.</span><span class="sxs-lookup"><span data-stu-id="e504b-116">The reason of action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e504b-117">-Name</span><span class="sxs-lookup"><span data-stu-id="e504b-117">-Name</span></span>
<span data-ttu-id="e504b-118">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="e504b-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e504b-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="e504b-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="e504b-120">O tipo de recurso de link privado.</span><span class="sxs-lookup"><span data-stu-id="e504b-120">The private link resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: False
Position: Named
Default value: 'Microsoft.Network/privateLinkServices'
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e504b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e504b-121">-ResourceGroupName</span></span>
<span data-ttu-id="e504b-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e504b-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e504b-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e504b-123">-ResourceId</span></span>
<span data-ttu-id="e504b-124">A ID do gerenciador de recursos do Azure da conexão de ponto de extremidade privada.</span><span class="sxs-lookup"><span data-stu-id="e504b-124">The Azure resource manager id of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e504b-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="e504b-125">-ServiceName</span></span>
<span data-ttu-id="e504b-126">O nome do serviço de link privado.</span><span class="sxs-lookup"><span data-stu-id="e504b-126">The private link service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```


### <span data-ttu-id="e504b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e504b-127">CommonParameters</span></span>
<span data-ttu-id="e504b-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e504b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e504b-129">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e504b-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e504b-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e504b-130">INPUTS</span></span>

### <span data-ttu-id="e504b-131">System.String</span><span class="sxs-lookup"><span data-stu-id="e504b-131">System.String</span></span>

## <span data-ttu-id="e504b-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e504b-132">OUTPUTS</span></span>

### <span data-ttu-id="e504b-133">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e504b-133">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="e504b-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="e504b-134">NOTES</span></span>

## <span data-ttu-id="e504b-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e504b-135">RELATED LINKS</span></span>

[<span data-ttu-id="e504b-136">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e504b-136">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="e504b-137">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e504b-137">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="e504b-138">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e504b-138">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="e504b-139">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e504b-139">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)