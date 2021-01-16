---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/deny-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Deny-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Deny-AzPrivateEndpointConnection.md
ms.openlocfilehash: 159b320b24ff1e9ab1b4c71e6c374931ecfeffdd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259376"
---
# <span data-ttu-id="f1ec0-101">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f1ec0-101">Deny-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="f1ec0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f1ec0-102">SYNOPSIS</span></span>
<span data-ttu-id="f1ec0-103">nega uma conexão de ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="f1ec0-103">denies a private endpoint connection.</span></span>

## <span data-ttu-id="f1ec0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f1ec0-104">SYNTAX</span></span>

### <span data-ttu-id="f1ec0-105">ByResourceId (padrão)</span><span class="sxs-lookup"><span data-stu-id="f1ec0-105">ByResourceId (Default)</span></span>
```
Deny-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1ec0-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="f1ec0-106">ByResource</span></span>
```
Deny-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
[-PrivateLinkResourceType <string>] [-Description <String>]
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1ec0-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f1ec0-107">DESCRIPTION</span></span>
<span data-ttu-id="f1ec0-108">O cmdlet **Deny-AzPrivateEndpointConnection** nega uma conexão de ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="f1ec0-108">The **Deny-AzPrivateEndpointConnection** cmdlet denies a private endpoint connection.</span></span>

## <span data-ttu-id="f1ec0-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f1ec0-109">EXAMPLES</span></span>

### <span data-ttu-id="f1ec0-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f1ec0-110">Example 1</span></span>
```
Deny-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService
```

<span data-ttu-id="f1ec0-111">Este exemplo nega uma conexão de ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="f1ec0-111">This example denies a private endpoint connection.</span></span>

## <span data-ttu-id="f1ec0-112">OS</span><span class="sxs-lookup"><span data-stu-id="f1ec0-112">PARAMETERS</span></span>

### <span data-ttu-id="f1ec0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1ec0-113">-DefaultProfile</span></span>
<span data-ttu-id="f1ec0-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f1ec0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1ec0-115">-Descrição</span><span class="sxs-lookup"><span data-stu-id="f1ec0-115">-Description</span></span>
<span data-ttu-id="f1ec0-116">O motivo da ação.</span><span class="sxs-lookup"><span data-stu-id="f1ec0-116">The reason of action.</span></span>

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

### <span data-ttu-id="f1ec0-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="f1ec0-117">-Name</span></span>
<span data-ttu-id="f1ec0-118">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="f1ec0-118">The resource name.</span></span>

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

### <span data-ttu-id="f1ec0-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="f1ec0-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="f1ec0-120">O tipo de recurso de link particular.</span><span class="sxs-lookup"><span data-stu-id="f1ec0-120">The private link resource type.</span></span>

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

### <span data-ttu-id="f1ec0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1ec0-121">-ResourceGroupName</span></span>
<span data-ttu-id="f1ec0-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f1ec0-122">The resource group name.</span></span>

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

### <span data-ttu-id="f1ec0-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f1ec0-123">-ResourceId</span></span>
<span data-ttu-id="f1ec0-124">A ID do Gerenciador de recursos do Azure da conexão de ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="f1ec0-124">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="f1ec0-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="f1ec0-125">-ServiceName</span></span>
<span data-ttu-id="f1ec0-126">O nome do serviço ao qual a conexão de ponto de extremidade privada pertence.</span><span class="sxs-lookup"><span data-stu-id="f1ec0-126">The name of service that private endpoint connection belong to.</span></span>

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

### <span data-ttu-id="f1ec0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1ec0-127">CommonParameters</span></span>
<span data-ttu-id="f1ec0-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1ec0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1ec0-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f1ec0-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1ec0-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f1ec0-130">INPUTS</span></span>

### <span data-ttu-id="f1ec0-131">System. String</span><span class="sxs-lookup"><span data-stu-id="f1ec0-131">System.String</span></span>

## <span data-ttu-id="f1ec0-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f1ec0-132">OUTPUTS</span></span>

### <span data-ttu-id="f1ec0-133">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f1ec0-133">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="f1ec0-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f1ec0-134">NOTES</span></span>

## <span data-ttu-id="f1ec0-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f1ec0-135">RELATED LINKS</span></span>

[<span data-ttu-id="f1ec0-136">Aprovar-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f1ec0-136">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="f1ec0-137">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f1ec0-137">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="f1ec0-138">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f1ec0-138">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="f1ec0-139">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f1ec0-139">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)