---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePort.md
ms.openlocfilehash: f9ce00bb5efbe5182143a08f9f205101b9f85611
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888834"
---
# <span data-ttu-id="7b060-101">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="7b060-101">Get-AzExpressRoutePort</span></span>

## <span data-ttu-id="7b060-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b060-102">SYNOPSIS</span></span>
<span data-ttu-id="7b060-103">Obtém um recurso do Azure ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="7b060-103">Gets an Azure ExpressRoutePort resource.</span></span>

## <span data-ttu-id="7b060-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7b060-104">SYNTAX</span></span>

### <span data-ttu-id="7b060-105">ResourceNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7b060-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzExpressRoutePort [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b060-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b060-106">ResourceIdParameterSet</span></span>
```
Get-AzExpressRoutePort -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b060-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7b060-107">DESCRIPTION</span></span>
<span data-ttu-id="7b060-108">O cmdlet **Get-AzExpressRoutePort** é usado para recuperar um objeto ExpressRoutePort da sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="7b060-108">The **Get-AzExpressRoutePort** cmdlet is used to retrieve an ExpressRoutePort object from your subscription.</span></span> <span data-ttu-id="7b060-109">O objeto expressrouteport retornado pode ser usado como entrada para outros cmdlets que operam no ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="7b060-109">The expressrouteport object returned can be used as input to other cmdlets that operate on ExpressRoutePort.</span></span>

## <span data-ttu-id="7b060-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7b060-110">EXAMPLES</span></span>

### <span data-ttu-id="7b060-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7b060-111">Example 1</span></span>
```powershell
PS C:\> Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
```

<span data-ttu-id="7b060-112">Obtém o objeto ExpressRoutePort com nome $PortName no grupo de recursos $rg em sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="7b060-112">Gets the ExpressRoutePort object with name $PortName in resource group $rg in your subscription.</span></span>

### <span data-ttu-id="7b060-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="7b060-113">Example 2</span></span>
```powershell
PS C:\> Get-AzExpressRoutePort -Name test*
```

<span data-ttu-id="7b060-114">Obtém todos os objetos ExpressRoutePort cujo nome começa com "test".</span><span class="sxs-lookup"><span data-stu-id="7b060-114">Gets all of the ExpressRoutePort objects whose name starts with "test".</span></span>

### <span data-ttu-id="7b060-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="7b060-115">Example 3</span></span>
```powershell
PS C:\> Get-AzExpressRoutePort -ResourceId $id
```

<span data-ttu-id="7b060-116">Obtém o objeto ExpressRoutePort com ResourceId $id.</span><span class="sxs-lookup"><span data-stu-id="7b060-116">Gets the ExpressRoutePort object with ResourceId $id.</span></span> 

## <span data-ttu-id="7b060-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7b060-117">PARAMETERS</span></span>

### <span data-ttu-id="7b060-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b060-118">-DefaultProfile</span></span>
<span data-ttu-id="7b060-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7b060-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b060-120">-Name</span><span class="sxs-lookup"><span data-stu-id="7b060-120">-Name</span></span>
<span data-ttu-id="7b060-121">O nome do ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="7b060-121">The name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="7b060-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b060-122">-ResourceGroupName</span></span>
<span data-ttu-id="7b060-123">O nome do grupo de recursos do ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="7b060-123">The resource group name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="7b060-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7b060-124">-ResourceId</span></span>
<span data-ttu-id="7b060-125">ResourceId da porta de rota expressa.</span><span class="sxs-lookup"><span data-stu-id="7b060-125">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="7b060-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b060-126">CommonParameters</span></span>
<span data-ttu-id="7b060-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b060-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b060-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7b060-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b060-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7b060-129">INPUTS</span></span>

### <span data-ttu-id="7b060-130">System.String</span><span class="sxs-lookup"><span data-stu-id="7b060-130">System.String</span></span>

## <span data-ttu-id="7b060-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7b060-131">OUTPUTS</span></span>

### <span data-ttu-id="7b060-132">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="7b060-132">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="7b060-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="7b060-133">NOTES</span></span>

## <span data-ttu-id="7b060-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7b060-134">RELATED LINKS</span></span>

[<span data-ttu-id="7b060-135">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="7b060-135">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="7b060-136">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="7b060-136">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)

[<span data-ttu-id="7b060-137">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="7b060-137">Set-AzExpressRoutePort</span></span>](./Set-AzExpressRoutePort.md)
