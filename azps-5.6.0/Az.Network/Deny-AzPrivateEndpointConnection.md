---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/deny-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Deny-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Deny-AzPrivateEndpointConnection.md
ms.openlocfilehash: 1522e8d9c66ccd2429ab331e1f39d26c06da5930
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888687"
---
# <span data-ttu-id="6169b-101">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6169b-101">Deny-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="6169b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6169b-102">SYNOPSIS</span></span>
<span data-ttu-id="6169b-103">nega uma conexão de ponto de extremidade privada.</span><span class="sxs-lookup"><span data-stu-id="6169b-103">denies a private endpoint connection.</span></span>

## <span data-ttu-id="6169b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6169b-104">SYNTAX</span></span>

### <span data-ttu-id="6169b-105">ByResourceId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6169b-105">ByResourceId (Default)</span></span>
```
Deny-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6169b-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="6169b-106">ByResource</span></span>
```
Deny-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
[-PrivateLinkResourceType <string>] [-Description <String>]
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6169b-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6169b-107">DESCRIPTION</span></span>
<span data-ttu-id="6169b-108">O cmdlet **Deny-AzPrivateEndpointConnection** nega uma conexão de ponto de extremidade privada.</span><span class="sxs-lookup"><span data-stu-id="6169b-108">The **Deny-AzPrivateEndpointConnection** cmdlet denies a private endpoint connection.</span></span>

## <span data-ttu-id="6169b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6169b-109">EXAMPLES</span></span>

### <span data-ttu-id="6169b-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6169b-110">Example 1</span></span>
```
Deny-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService
```

<span data-ttu-id="6169b-111">Este exemplo nega uma conexão de ponto de extremidade privada.</span><span class="sxs-lookup"><span data-stu-id="6169b-111">This example denies a private endpoint connection.</span></span>

## <span data-ttu-id="6169b-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6169b-112">PARAMETERS</span></span>

### <span data-ttu-id="6169b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6169b-113">-DefaultProfile</span></span>
<span data-ttu-id="6169b-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6169b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6169b-115">-Description</span><span class="sxs-lookup"><span data-stu-id="6169b-115">-Description</span></span>
<span data-ttu-id="6169b-116">O motivo da ação.</span><span class="sxs-lookup"><span data-stu-id="6169b-116">The reason of action.</span></span>

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

### <span data-ttu-id="6169b-117">-Name</span><span class="sxs-lookup"><span data-stu-id="6169b-117">-Name</span></span>
<span data-ttu-id="6169b-118">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="6169b-118">The resource name.</span></span>

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

### <span data-ttu-id="6169b-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="6169b-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="6169b-120">O tipo de recurso de link privado.</span><span class="sxs-lookup"><span data-stu-id="6169b-120">The private link resource type.</span></span>

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

### <span data-ttu-id="6169b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6169b-121">-ResourceGroupName</span></span>
<span data-ttu-id="6169b-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6169b-122">The resource group name.</span></span>

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

### <span data-ttu-id="6169b-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6169b-123">-ResourceId</span></span>
<span data-ttu-id="6169b-124">A ID do gerenciador de recursos do Azure da conexão de ponto de extremidade privada.</span><span class="sxs-lookup"><span data-stu-id="6169b-124">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="6169b-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="6169b-125">-ServiceName</span></span>
<span data-ttu-id="6169b-126">O nome do serviço ao que a conexão de ponto de extremidade privada pertence.</span><span class="sxs-lookup"><span data-stu-id="6169b-126">The name of service that private endpoint connection belong to.</span></span>

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

### <span data-ttu-id="6169b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6169b-127">CommonParameters</span></span>
<span data-ttu-id="6169b-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6169b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6169b-129">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6169b-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6169b-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6169b-130">INPUTS</span></span>

### <span data-ttu-id="6169b-131">System.String</span><span class="sxs-lookup"><span data-stu-id="6169b-131">System.String</span></span>

## <span data-ttu-id="6169b-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6169b-132">OUTPUTS</span></span>

### <span data-ttu-id="6169b-133">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="6169b-133">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="6169b-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="6169b-134">NOTES</span></span>

## <span data-ttu-id="6169b-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6169b-135">RELATED LINKS</span></span>

[<span data-ttu-id="6169b-136">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6169b-136">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="6169b-137">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6169b-137">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="6169b-138">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6169b-138">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="6169b-139">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6169b-139">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)