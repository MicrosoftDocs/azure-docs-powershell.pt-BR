---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/approve-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Approve-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Approve-AzPrivateEndpointConnection.md
ms.openlocfilehash: 9b47fb1954b13e28268f6b7aad66fa8190e20584
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771821"
---
# <span data-ttu-id="ce152-101">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ce152-101">Approve-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="ce152-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ce152-102">SYNOPSIS</span></span>
<span data-ttu-id="ce152-103">Aprova uma conexão de ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="ce152-103">Approves a private endpoint connection.</span></span>

## <span data-ttu-id="ce152-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ce152-104">SYNTAX</span></span>

### <span data-ttu-id="ce152-105">ByResourceId (padrão)</span><span class="sxs-lookup"><span data-stu-id="ce152-105">ByResourceId (Default)</span></span>
```
Approve-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce152-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="ce152-106">ByResource</span></span>
```
Approve-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce152-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ce152-107">DESCRIPTION</span></span>
<span data-ttu-id="ce152-108">O cmdlet **Approve-AzPrivateEndpointConnection** aprova uma conexão de ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="ce152-108">The **Approve-AzPrivateEndpointConnection** cmdlet approves a private endpoint connection.</span></span>

## <span data-ttu-id="ce152-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ce152-109">EXAMPLES</span></span>

### <span data-ttu-id="ce152-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ce152-110">Example 1</span></span>
```
Approve-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService
```

<span data-ttu-id="ce152-111">Este exemplo aprova uma conexão de ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="ce152-111">This example approves a private endpoint connection.</span></span>

## <span data-ttu-id="ce152-112">OS</span><span class="sxs-lookup"><span data-stu-id="ce152-112">PARAMETERS</span></span>

### <span data-ttu-id="ce152-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce152-113">-DefaultProfile</span></span>
<span data-ttu-id="ce152-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ce152-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce152-115">-Descrição</span><span class="sxs-lookup"><span data-stu-id="ce152-115">-Description</span></span>
<span data-ttu-id="ce152-116">O motivo da ação.</span><span class="sxs-lookup"><span data-stu-id="ce152-116">The reason of action.</span></span>

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

### <span data-ttu-id="ce152-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="ce152-117">-Name</span></span>
<span data-ttu-id="ce152-118">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="ce152-118">The resource name.</span></span>

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

### <span data-ttu-id="ce152-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce152-119">-ResourceGroupName</span></span>
<span data-ttu-id="ce152-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ce152-120">The resource group name.</span></span>

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

### <span data-ttu-id="ce152-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ce152-121">-ResourceId</span></span>
<span data-ttu-id="ce152-122">A ID do Gerenciador de recursos do Azure da conexão de ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="ce152-122">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="ce152-123">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="ce152-123">-ServiceName</span></span>
<span data-ttu-id="ce152-124">O nome do serviço de link privado.</span><span class="sxs-lookup"><span data-stu-id="ce152-124">The private link service name.</span></span>

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

### <span data-ttu-id="ce152-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce152-125">CommonParameters</span></span>
<span data-ttu-id="ce152-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce152-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce152-127">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ce152-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce152-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ce152-128">INPUTS</span></span>

### <span data-ttu-id="ce152-129">System. String</span><span class="sxs-lookup"><span data-stu-id="ce152-129">System.String</span></span>

## <span data-ttu-id="ce152-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ce152-130">OUTPUTS</span></span>

### <span data-ttu-id="ce152-131">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ce152-131">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="ce152-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ce152-132">NOTES</span></span>

## <span data-ttu-id="ce152-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ce152-133">RELATED LINKS</span></span>

[<span data-ttu-id="ce152-134">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ce152-134">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="ce152-135">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ce152-135">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="ce152-136">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ce152-136">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)