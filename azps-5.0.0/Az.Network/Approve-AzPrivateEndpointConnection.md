---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/approve-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Approve-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Approve-AzPrivateEndpointConnection.md
ms.openlocfilehash: 8fe3058b122c88448403293ad4f109aa5d62b23f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94124790"
---
# <span data-ttu-id="b9ced-101">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b9ced-101">Approve-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="b9ced-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b9ced-102">SYNOPSIS</span></span>
<span data-ttu-id="b9ced-103">Aprova uma conexão de ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="b9ced-103">Approves a private endpoint connection.</span></span>

## <span data-ttu-id="b9ced-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b9ced-104">SYNTAX</span></span>

### <span data-ttu-id="b9ced-105">ByResourceId (padrão)</span><span class="sxs-lookup"><span data-stu-id="b9ced-105">ByResourceId (Default)</span></span>
```
Approve-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9ced-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="b9ced-106">ByResource</span></span>
```
Approve-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-PrivateLinkResourceType <string>][-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9ced-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b9ced-107">DESCRIPTION</span></span>
<span data-ttu-id="b9ced-108">O cmdlet **Approve-AzPrivateEndpointConnection** aprova uma conexão de ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="b9ced-108">The **Approve-AzPrivateEndpointConnection** cmdlet approves a private endpoint connection.</span></span>

## <span data-ttu-id="b9ced-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b9ced-109">EXAMPLES</span></span>

### <span data-ttu-id="b9ced-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b9ced-110">Example 1</span></span>
```
Approve-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService
```

<span data-ttu-id="b9ced-111">Este exemplo aprova uma conexão de ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="b9ced-111">This example approves a private endpoint connection.</span></span>

## <span data-ttu-id="b9ced-112">OS</span><span class="sxs-lookup"><span data-stu-id="b9ced-112">PARAMETERS</span></span>

### <span data-ttu-id="b9ced-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9ced-113">-DefaultProfile</span></span>
<span data-ttu-id="b9ced-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b9ced-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9ced-115">-Descrição</span><span class="sxs-lookup"><span data-stu-id="b9ced-115">-Description</span></span>
<span data-ttu-id="b9ced-116">O motivo da ação.</span><span class="sxs-lookup"><span data-stu-id="b9ced-116">The reason of action.</span></span>

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

### <span data-ttu-id="b9ced-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="b9ced-117">-Name</span></span>
<span data-ttu-id="b9ced-118">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="b9ced-118">The resource name.</span></span>

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

### <span data-ttu-id="b9ced-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="b9ced-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="b9ced-120">O tipo de recurso de link particular.</span><span class="sxs-lookup"><span data-stu-id="b9ced-120">The private link resource type.</span></span>

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

### <span data-ttu-id="b9ced-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9ced-121">-ResourceGroupName</span></span>
<span data-ttu-id="b9ced-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b9ced-122">The resource group name.</span></span>

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

### <span data-ttu-id="b9ced-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b9ced-123">-ResourceId</span></span>
<span data-ttu-id="b9ced-124">A ID do Gerenciador de recursos do Azure da conexão de ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="b9ced-124">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="b9ced-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="b9ced-125">-ServiceName</span></span>
<span data-ttu-id="b9ced-126">O nome do serviço de link privado.</span><span class="sxs-lookup"><span data-stu-id="b9ced-126">The private link service name.</span></span>

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


### <span data-ttu-id="b9ced-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9ced-127">CommonParameters</span></span>
<span data-ttu-id="b9ced-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9ced-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9ced-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b9ced-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9ced-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b9ced-130">INPUTS</span></span>

### <span data-ttu-id="b9ced-131">System. String</span><span class="sxs-lookup"><span data-stu-id="b9ced-131">System.String</span></span>

## <span data-ttu-id="b9ced-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b9ced-132">OUTPUTS</span></span>

### <span data-ttu-id="b9ced-133">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="b9ced-133">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="b9ced-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b9ced-134">NOTES</span></span>

## <span data-ttu-id="b9ced-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b9ced-135">RELATED LINKS</span></span>

[<span data-ttu-id="b9ced-136">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b9ced-136">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="b9ced-137">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b9ced-137">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="b9ced-138">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b9ced-138">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="b9ced-139">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b9ced-139">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)