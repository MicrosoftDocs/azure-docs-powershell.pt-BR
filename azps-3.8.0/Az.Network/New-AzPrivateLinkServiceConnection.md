---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatelinkserviceconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkServiceConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkServiceConnection.md
ms.openlocfilehash: 74f531e48ca873d3853aba3312d6bb10edccdfaa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943261"
---
# <span data-ttu-id="25e9a-101">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="25e9a-101">New-AzPrivateLinkServiceConnection</span></span>

## <span data-ttu-id="25e9a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="25e9a-102">SYNOPSIS</span></span>
<span data-ttu-id="25e9a-103">Cria uma configuração de conexão de serviço de link particular.</span><span class="sxs-lookup"><span data-stu-id="25e9a-103">Creates a private link service connection configuration.</span></span>

## <span data-ttu-id="25e9a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="25e9a-104">SYNTAX</span></span>

### <span data-ttu-id="25e9a-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="25e9a-105">SetByResource (Default)</span></span>
```
New-AzPrivateLinkServiceConnection -Name <String> -PrivateLinkService <PSPrivateLinkService>
 [-GroupId <String[]>] [-RequestMessage <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="25e9a-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="25e9a-106">SetByResourceId</span></span>
```
New-AzPrivateLinkServiceConnection -Name <String> -PrivateLinkServiceId <String> [-GroupId <String[]>]
 [-RequestMessage <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25e9a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="25e9a-107">DESCRIPTION</span></span>
<span data-ttu-id="25e9a-108">**O cmdlet New-AzPrivateLinkServiceConnection** cria uma configuração de conexão de serviço de link particular.</span><span class="sxs-lookup"><span data-stu-id="25e9a-108">**The New-AzPrivateLinkServiceConnection** cmdlet creates a private link service connection configuration.</span></span>

## <span data-ttu-id="25e9a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="25e9a-109">EXAMPLES</span></span>

### <span data-ttu-id="25e9a-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="25e9a-110">Example 1</span></span>
```
New-AzPrivateLinkServiceConnection -Name MyPLSConnection -PrivateLinkServiceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/privateLinkServices/privateLinkService" -RequestMessage "Please Approve my request"
```

<span data-ttu-id="25e9a-111">Este exemplo cria um objeto de conexão de serviço de link privado na memória para uso na criação de um ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="25e9a-111">This example create a private link service connection object in memory for using in creating private endpoint.</span></span>

## <span data-ttu-id="25e9a-112">OS</span><span class="sxs-lookup"><span data-stu-id="25e9a-112">PARAMETERS</span></span>

### <span data-ttu-id="25e9a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25e9a-113">-DefaultProfile</span></span>
<span data-ttu-id="25e9a-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="25e9a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25e9a-115">-GroupId</span><span class="sxs-lookup"><span data-stu-id="25e9a-115">-GroupId</span></span>
<span data-ttu-id="25e9a-116">A lista de ID do grupo.</span><span class="sxs-lookup"><span data-stu-id="25e9a-116">The list of group id.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25e9a-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="25e9a-117">-Name</span></span>
<span data-ttu-id="25e9a-118">O nome do serviço de link particular.</span><span class="sxs-lookup"><span data-stu-id="25e9a-118">The name of private link service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25e9a-119">-PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="25e9a-119">-PrivateLinkService</span></span>
<span data-ttu-id="25e9a-120">O serviço de link particular.</span><span class="sxs-lookup"><span data-stu-id="25e9a-120">The private link service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25e9a-121">-PrivateLinkServiceId</span><span class="sxs-lookup"><span data-stu-id="25e9a-121">-PrivateLinkServiceId</span></span>
<span data-ttu-id="25e9a-122">A ID do serviço de link privado.</span><span class="sxs-lookup"><span data-stu-id="25e9a-122">The id of private link service.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25e9a-123">-RequestMessage</span><span class="sxs-lookup"><span data-stu-id="25e9a-123">-RequestMessage</span></span>
<span data-ttu-id="25e9a-124">A mensagem de solicitação.</span><span class="sxs-lookup"><span data-stu-id="25e9a-124">The request message.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25e9a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25e9a-125">CommonParameters</span></span>
<span data-ttu-id="25e9a-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25e9a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25e9a-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="25e9a-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25e9a-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="25e9a-128">INPUTS</span></span>

### <span data-ttu-id="25e9a-129">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="25e9a-129">None</span></span>

## <span data-ttu-id="25e9a-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="25e9a-130">OUTPUTS</span></span>

### <span data-ttu-id="25e9a-131">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="25e9a-131">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceConnection</span></span>

## <span data-ttu-id="25e9a-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="25e9a-132">NOTES</span></span>

## <span data-ttu-id="25e9a-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="25e9a-133">RELATED LINKS</span></span>

[<span data-ttu-id="25e9a-134">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="25e9a-134">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)