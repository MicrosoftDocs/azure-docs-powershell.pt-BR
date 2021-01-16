---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePort.md
ms.openlocfilehash: 670880a9fa82e4845f37cdb5f0d108533a2b72c5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260484"
---
# <span data-ttu-id="a0fb7-101">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="a0fb7-101">Get-AzExpressRoutePort</span></span>

## <span data-ttu-id="a0fb7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a0fb7-102">SYNOPSIS</span></span>
<span data-ttu-id="a0fb7-103">Obtém um recurso do Azure ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="a0fb7-103">Gets an Azure ExpressRoutePort resource.</span></span>

## <span data-ttu-id="a0fb7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a0fb7-104">SYNTAX</span></span>

### <span data-ttu-id="a0fb7-105">ResourceNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="a0fb7-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzExpressRoutePort [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a0fb7-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0fb7-106">ResourceIdParameterSet</span></span>
```
Get-AzExpressRoutePort -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0fb7-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a0fb7-107">DESCRIPTION</span></span>
<span data-ttu-id="a0fb7-108">O cmdlet **Get-AzExpressRoutePort** é usado para recuperar um objeto ExpressRoutePort da sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="a0fb7-108">The **Get-AzExpressRoutePort** cmdlet is used to retrieve an ExpressRoutePort object from your subscription.</span></span> <span data-ttu-id="a0fb7-109">O objeto expressrouteport retornado pode ser usado como entrada para outros cmdlets que operam em ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="a0fb7-109">The expressrouteport object returned can be used as input to other cmdlets that operate on ExpressRoutePort.</span></span>

## <span data-ttu-id="a0fb7-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a0fb7-110">EXAMPLES</span></span>

### <span data-ttu-id="a0fb7-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a0fb7-111">Example 1</span></span>
```powershell
PS C:\> Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
```

<span data-ttu-id="a0fb7-112">Obtém o objeto ExpressRoutePort com o nome $PortName no grupo de recursos $rg na sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="a0fb7-112">Gets the ExpressRoutePort object with name $PortName in resource group $rg in your subscription.</span></span>

### <span data-ttu-id="a0fb7-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a0fb7-113">Example 2</span></span>
```powershell
PS C:\> Get-AzExpressRoutePort -Name test*
```

<span data-ttu-id="a0fb7-114">Obtém todos os objetos ExpressRoutePort cujo nome começa com "Test".</span><span class="sxs-lookup"><span data-stu-id="a0fb7-114">Gets all of the ExpressRoutePort objects whose name starts with "test".</span></span>

### <span data-ttu-id="a0fb7-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="a0fb7-115">Example 3</span></span>
```powershell
PS C:\> Get-AzExpressRoutePort -ResourceId $id
```

<span data-ttu-id="a0fb7-116">Obtém o objeto ExpressRoutePort com $id ResourceId.</span><span class="sxs-lookup"><span data-stu-id="a0fb7-116">Gets the ExpressRoutePort object with ResourceId $id.</span></span> 

## <span data-ttu-id="a0fb7-117">OS</span><span class="sxs-lookup"><span data-stu-id="a0fb7-117">PARAMETERS</span></span>

### <span data-ttu-id="a0fb7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0fb7-118">-DefaultProfile</span></span>
<span data-ttu-id="a0fb7-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a0fb7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0fb7-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="a0fb7-120">-Name</span></span>
<span data-ttu-id="a0fb7-121">O nome do ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="a0fb7-121">The name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="a0fb7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0fb7-122">-ResourceGroupName</span></span>
<span data-ttu-id="a0fb7-123">O nome do grupo de recursos do ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="a0fb7-123">The resource group name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="a0fb7-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a0fb7-124">-ResourceId</span></span>
<span data-ttu-id="a0fb7-125">ResourceId da porta de rota expressa.</span><span class="sxs-lookup"><span data-stu-id="a0fb7-125">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="a0fb7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0fb7-126">CommonParameters</span></span>
<span data-ttu-id="a0fb7-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0fb7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0fb7-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a0fb7-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0fb7-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a0fb7-129">INPUTS</span></span>

### <span data-ttu-id="a0fb7-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a0fb7-130">System.String</span></span>

## <span data-ttu-id="a0fb7-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a0fb7-131">OUTPUTS</span></span>

### <span data-ttu-id="a0fb7-132">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="a0fb7-132">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="a0fb7-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a0fb7-133">NOTES</span></span>

## <span data-ttu-id="a0fb7-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a0fb7-134">RELATED LINKS</span></span>

[<span data-ttu-id="a0fb7-135">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="a0fb7-135">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="a0fb7-136">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="a0fb7-136">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)

[<span data-ttu-id="a0fb7-137">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="a0fb7-137">Set-AzExpressRoutePort</span></span>](./Set-AzExpressRoutePort.md)
