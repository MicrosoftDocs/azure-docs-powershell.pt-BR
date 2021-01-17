---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/deny-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Deny-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Deny-AzPrivateEndpointConnection.md
ms.openlocfilehash: 159b320b24ff1e9ab1b4c71e6c374931ecfeffdd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427044"
---
# <span data-ttu-id="d9bd2-101">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d9bd2-101">Deny-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="d9bd2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d9bd2-102">SYNOPSIS</span></span>
<span data-ttu-id="d9bd2-103">nega uma conexão de ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="d9bd2-103">denies a private endpoint connection.</span></span>

## <span data-ttu-id="d9bd2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d9bd2-104">SYNTAX</span></span>

### <span data-ttu-id="d9bd2-105">ByResourceId (padrão)</span><span class="sxs-lookup"><span data-stu-id="d9bd2-105">ByResourceId (Default)</span></span>
```
Deny-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9bd2-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="d9bd2-106">ByResource</span></span>
```
Deny-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
[-PrivateLinkResourceType <string>] [-Description <String>]
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9bd2-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d9bd2-107">DESCRIPTION</span></span>
<span data-ttu-id="d9bd2-108">O cmdlet **Deny-AzPrivateEndpointConnection** nega uma conexão de ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="d9bd2-108">The **Deny-AzPrivateEndpointConnection** cmdlet denies a private endpoint connection.</span></span>

## <span data-ttu-id="d9bd2-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d9bd2-109">EXAMPLES</span></span>

### <span data-ttu-id="d9bd2-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d9bd2-110">Example 1</span></span>
```
Deny-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService
```

<span data-ttu-id="d9bd2-111">Este exemplo nega uma conexão de ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="d9bd2-111">This example denies a private endpoint connection.</span></span>

## <span data-ttu-id="d9bd2-112">OS</span><span class="sxs-lookup"><span data-stu-id="d9bd2-112">PARAMETERS</span></span>

### <span data-ttu-id="d9bd2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9bd2-113">-DefaultProfile</span></span>
<span data-ttu-id="d9bd2-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d9bd2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9bd2-115">-Descrição</span><span class="sxs-lookup"><span data-stu-id="d9bd2-115">-Description</span></span>
<span data-ttu-id="d9bd2-116">O motivo da ação.</span><span class="sxs-lookup"><span data-stu-id="d9bd2-116">The reason of action.</span></span>

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

### <span data-ttu-id="d9bd2-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="d9bd2-117">-Name</span></span>
<span data-ttu-id="d9bd2-118">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="d9bd2-118">The resource name.</span></span>

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

### <span data-ttu-id="d9bd2-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="d9bd2-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="d9bd2-120">O tipo de recurso de link particular.</span><span class="sxs-lookup"><span data-stu-id="d9bd2-120">The private link resource type.</span></span>

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

### <span data-ttu-id="d9bd2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9bd2-121">-ResourceGroupName</span></span>
<span data-ttu-id="d9bd2-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d9bd2-122">The resource group name.</span></span>

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

### <span data-ttu-id="d9bd2-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d9bd2-123">-ResourceId</span></span>
<span data-ttu-id="d9bd2-124">A ID do Gerenciador de recursos do Azure da conexão de ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="d9bd2-124">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="d9bd2-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="d9bd2-125">-ServiceName</span></span>
<span data-ttu-id="d9bd2-126">O nome do serviço ao qual a conexão de ponto de extremidade privada pertence.</span><span class="sxs-lookup"><span data-stu-id="d9bd2-126">The name of service that private endpoint connection belong to.</span></span>

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

### <span data-ttu-id="d9bd2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9bd2-127">CommonParameters</span></span>
<span data-ttu-id="d9bd2-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9bd2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9bd2-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d9bd2-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9bd2-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d9bd2-130">INPUTS</span></span>

### <span data-ttu-id="d9bd2-131">System. String</span><span class="sxs-lookup"><span data-stu-id="d9bd2-131">System.String</span></span>

## <span data-ttu-id="d9bd2-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d9bd2-132">OUTPUTS</span></span>

### <span data-ttu-id="d9bd2-133">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d9bd2-133">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="d9bd2-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d9bd2-134">NOTES</span></span>

## <span data-ttu-id="d9bd2-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d9bd2-135">RELATED LINKS</span></span>

[<span data-ttu-id="d9bd2-136">Aprovar-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d9bd2-136">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="d9bd2-137">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d9bd2-137">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="d9bd2-138">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d9bd2-138">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="d9bd2-139">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d9bd2-139">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)