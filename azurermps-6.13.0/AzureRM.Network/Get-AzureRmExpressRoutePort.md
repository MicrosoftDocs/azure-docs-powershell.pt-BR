---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRoutePort.md
ms.openlocfilehash: 36c15c9a0bfae9bbf3a14f59877d23c1c8778163
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610566"
---
# <span data-ttu-id="b8a48-101">Get-AzureRmExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="b8a48-101">Get-AzureRmExpressRoutePort</span></span>

## <span data-ttu-id="b8a48-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b8a48-102">SYNOPSIS</span></span>
<span data-ttu-id="b8a48-103">Obtém um recurso do Azure ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="b8a48-103">Gets an Azure ExpressRoutePort resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8a48-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b8a48-104">SYNTAX</span></span>

### <span data-ttu-id="b8a48-105">ResourceNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="b8a48-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzureRmExpressRoutePort [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8a48-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8a48-106">ResourceIdParameterSet</span></span>
```
Get-AzureRmExpressRoutePort -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b8a48-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b8a48-107">DESCRIPTION</span></span>
<span data-ttu-id="b8a48-108">O cmdlet **Get-AzureRmExpressRoutePort** é usado para recuperar um objeto ExpressRoutePort da sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="b8a48-108">The **Get-AzureRmExpressRoutePort** cmdlet is used to retrieve an ExpressRoutePort object from your subscription.</span></span> <span data-ttu-id="b8a48-109">O objeto expressrouteport retornado pode ser usado como entrada para outros cmdlets que operam em ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="b8a48-109">The expressrouteport object returned can be used as input to other cmdlets that operate on ExpressRoutePort.</span></span>

## <span data-ttu-id="b8a48-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b8a48-110">EXAMPLES</span></span>

### <span data-ttu-id="b8a48-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b8a48-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmExpressRoutePort -Name $PortName -ResourceGroupName $rg
```

<span data-ttu-id="b8a48-112">Obtém o objeto ExpressRoutePort com o nome $PortName no grupo de recursos $rg na sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="b8a48-112">Gets the ExpressRoutePort object with name $PortName in resource group $rg in your subscription.</span></span>

### <span data-ttu-id="b8a48-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b8a48-113">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmExpressRoutePort -ResourceId $id
```

<span data-ttu-id="b8a48-114">Obtém o objeto ExpressRoutePort com $id ResourceId.</span><span class="sxs-lookup"><span data-stu-id="b8a48-114">Gets the ExpressRoutePort object with ResourceId $id.</span></span> 

## <span data-ttu-id="b8a48-115">OS</span><span class="sxs-lookup"><span data-stu-id="b8a48-115">PARAMETERS</span></span>

### <span data-ttu-id="b8a48-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8a48-116">-DefaultProfile</span></span>
<span data-ttu-id="b8a48-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b8a48-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8a48-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="b8a48-118">-Name</span></span>
<span data-ttu-id="b8a48-119">O nome do ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="b8a48-119">The name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8a48-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8a48-120">-ResourceGroupName</span></span>
<span data-ttu-id="b8a48-121">O nome do grupo de recursos do ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="b8a48-121">The resource group name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8a48-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8a48-122">-ResourceId</span></span>
<span data-ttu-id="b8a48-123">ResourceId da porta de rota expressa.</span><span class="sxs-lookup"><span data-stu-id="b8a48-123">ResourceId of the express route port.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8a48-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8a48-124">CommonParameters</span></span>
<span data-ttu-id="b8a48-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8a48-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8a48-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8a48-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8a48-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b8a48-127">INPUTS</span></span>

### <span data-ttu-id="b8a48-128">System. String</span><span class="sxs-lookup"><span data-stu-id="b8a48-128">System.String</span></span>

## <span data-ttu-id="b8a48-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b8a48-129">OUTPUTS</span></span>

### <span data-ttu-id="b8a48-130">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="b8a48-130">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="b8a48-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b8a48-131">NOTES</span></span>

## <span data-ttu-id="b8a48-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b8a48-132">RELATED LINKS</span></span>
