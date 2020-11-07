---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
ms.openlocfilehash: 7504da022a5cf1310a375bed40370d71d60f205a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771720"
---
# <span data-ttu-id="ab1c4-101">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ab1c4-101">Get-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="ab1c4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ab1c4-102">SYNOPSIS</span></span>
<span data-ttu-id="ab1c4-103">Obtém um recurso de conexão de ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="ab1c4-103">Gets a private endpoint connection resource.</span></span>

## <span data-ttu-id="ab1c4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ab1c4-104">SYNTAX</span></span>

### <span data-ttu-id="ab1c4-105">ByResourceId (padrão)</span><span class="sxs-lookup"><span data-stu-id="ab1c4-105">ByResourceId (Default)</span></span>
```
Get-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab1c4-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="ab1c4-106">ByResource</span></span>
```
Get-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab1c4-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ab1c4-107">DESCRIPTION</span></span>
<span data-ttu-id="ab1c4-108">O cmdlet **Get-AzPrivateEndpointConnection** recupera um recurso de conexão de ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="ab1c4-108">The **Get-AzPrivateEndpointConnection** cmdlet retrieves a private endpoint connection resource.</span></span>

## <span data-ttu-id="ab1c4-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ab1c4-109">EXAMPLES</span></span>

### <span data-ttu-id="ab1c4-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ab1c4-110">Example 1</span></span>
```
Get-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkServiceName
```

<span data-ttu-id="ab1c4-111">Este exemplo obtém uma conexão de ponto de extremidade privada chamada MyPrivateEndpointConnection1</span><span class="sxs-lookup"><span data-stu-id="ab1c4-111">This example get a private endpoint connection named MyPrivateEndpointConnection1</span></span>

## <span data-ttu-id="ab1c4-112">OS</span><span class="sxs-lookup"><span data-stu-id="ab1c4-112">PARAMETERS</span></span>

### <span data-ttu-id="ab1c4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab1c4-113">-DefaultProfile</span></span>
<span data-ttu-id="ab1c4-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ab1c4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab1c4-115">-Descrição</span><span class="sxs-lookup"><span data-stu-id="ab1c4-115">-Description</span></span>
<span data-ttu-id="ab1c4-116">O motivo da ação.</span><span class="sxs-lookup"><span data-stu-id="ab1c4-116">The reason of action.</span></span>

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

### <span data-ttu-id="ab1c4-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="ab1c4-117">-Name</span></span>
<span data-ttu-id="ab1c4-118">O nome da conexão de ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="ab1c4-118">The name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="ab1c4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab1c4-119">-ResourceGroupName</span></span>
<span data-ttu-id="ab1c4-120">O nome do grupo de recursos da conexão de ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="ab1c4-120">The resource group name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="ab1c4-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ab1c4-121">-ResourceId</span></span>
<span data-ttu-id="ab1c4-122">A ID do Gerenciador de recursos do Azure da conexão de ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="ab1c4-122">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="ab1c4-123">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="ab1c4-123">-ServiceName</span></span>
<span data-ttu-id="ab1c4-124">O nome do serviço de vínculo privado que tem a conexão de ponto de extremidade privada.</span><span class="sxs-lookup"><span data-stu-id="ab1c4-124">The name of the private link service that has the private endpoint connection.</span></span>

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

### <span data-ttu-id="ab1c4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab1c4-125">CommonParameters</span></span>
<span data-ttu-id="ab1c4-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab1c4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab1c4-127">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ab1c4-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab1c4-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ab1c4-128">INPUTS</span></span>

### <span data-ttu-id="ab1c4-129">System. String</span><span class="sxs-lookup"><span data-stu-id="ab1c4-129">System.String</span></span>

## <span data-ttu-id="ab1c4-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ab1c4-130">OUTPUTS</span></span>

### <span data-ttu-id="ab1c4-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ab1c4-131">System.Boolean</span></span>

## <span data-ttu-id="ab1c4-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ab1c4-132">NOTES</span></span>

## <span data-ttu-id="ab1c4-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ab1c4-133">RELATED LINKS</span></span>

[<span data-ttu-id="ab1c4-134">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ab1c4-134">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
