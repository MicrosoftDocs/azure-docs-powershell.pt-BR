---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteportloa
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortLOA.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortLOA.md
ms.openlocfilehash: 22f5023aa294dde734157439d8b355916adfb03f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271738"
---
# <span data-ttu-id="b6a50-101">New-AzExpressRoutePortLOA</span><span class="sxs-lookup"><span data-stu-id="b6a50-101">New-AzExpressRoutePortLOA</span></span>

## <span data-ttu-id="b6a50-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b6a50-102">SYNOPSIS</span></span>
<span data-ttu-id="b6a50-103">Baixar a carta de autorização do documento para uma porta expressa de rota.</span><span class="sxs-lookup"><span data-stu-id="b6a50-103">Download letter of authorization document for an express route port.</span></span>

## <span data-ttu-id="b6a50-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b6a50-104">SYNTAX</span></span>

### <span data-ttu-id="b6a50-105">ResourceNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="b6a50-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzExpressRoutePortLOA -PortName <String> -ResourceGroupName <String> -CustomerName <String>
 [-Destination <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6a50-106">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6a50-106">ResourceObjectParameterSet</span></span>
```
New-AzExpressRoutePortLOA -ExpressRoutePort <PSExpressRoutePort> -CustomerName <String> [-Destination <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6a50-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6a50-107">ResourceIdParameterSet</span></span>
```
New-AzExpressRoutePortLOA -Id <String> -CustomerName <String> [-Destination <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6a50-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b6a50-108">DESCRIPTION</span></span>
<span data-ttu-id="b6a50-109">New-AzExpressRoutePortLOA cmdlet baixa um documento da carta de autorização no formato PDF para uma porta expressa de rota.</span><span class="sxs-lookup"><span data-stu-id="b6a50-109">New-AzExpressRoutePortLOA cmdlet downloads a letter of authorization document in PDF format for an express route port.</span></span>


## <span data-ttu-id="b6a50-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b6a50-110">EXAMPLES</span></span>

### <span data-ttu-id="b6a50-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b6a50-111">Example 1</span></span>
```powershell
PS C:\> New-AzExpressRoutePortLOA -ResourceGroupName myRg -PortName myPort -CustomerName Contoso -Destination loa.pdf
```

<span data-ttu-id="b6a50-112">Baixe o documento da carta de autorização para porta de rota expressa ' MyPort ' e armazene-o no arquivo ' loa.pdf '.</span><span class="sxs-lookup"><span data-stu-id="b6a50-112">Download the letter of authorization document for express route port 'myPort' and store it in file 'loa.pdf'.</span></span>

## <span data-ttu-id="b6a50-113">OS</span><span class="sxs-lookup"><span data-stu-id="b6a50-113">PARAMETERS</span></span>

### <span data-ttu-id="b6a50-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b6a50-114">-AsJob</span></span>
<span data-ttu-id="b6a50-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="b6a50-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6a50-116">-O CustomerName</span><span class="sxs-lookup"><span data-stu-id="b6a50-116">-CustomerName</span></span>
<span data-ttu-id="b6a50-117">O nome do cliente ao qual esta porta expressa expressa está atribuída.</span><span class="sxs-lookup"><span data-stu-id="b6a50-117">The customer name to whom this Express Route Port is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6a50-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6a50-118">-DefaultProfile</span></span>
<span data-ttu-id="b6a50-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b6a50-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6a50-120">-Destino</span><span class="sxs-lookup"><span data-stu-id="b6a50-120">-Destination</span></span>
<span data-ttu-id="b6a50-121">O FilePath de saída para armazenar a carta de autorização.</span><span class="sxs-lookup"><span data-stu-id="b6a50-121">The output filepath to store the Letter of Authorization to.</span></span>

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

### <span data-ttu-id="b6a50-122">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="b6a50-122">-ExpressRoutePort</span></span>
<span data-ttu-id="b6a50-123">O recurso de porta de rota expressa.</span><span class="sxs-lookup"><span data-stu-id="b6a50-123">The express route port resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: ResourceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6a50-124">-ID</span><span class="sxs-lookup"><span data-stu-id="b6a50-124">-Id</span></span>
<span data-ttu-id="b6a50-125">ResourceId da porta de rota expressa.</span><span class="sxs-lookup"><span data-stu-id="b6a50-125">ResourceId of the express route port.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6a50-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b6a50-126">-PassThru</span></span>
<span data-ttu-id="b6a50-127">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="b6a50-127">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="b6a50-128">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="b6a50-128">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6a50-129">-PortName</span><span class="sxs-lookup"><span data-stu-id="b6a50-129">-PortName</span></span>
<span data-ttu-id="b6a50-130">O nome da porta de rota expressa.</span><span class="sxs-lookup"><span data-stu-id="b6a50-130">The express route port name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6a50-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6a50-131">-ResourceGroupName</span></span>
<span data-ttu-id="b6a50-132">O nome do grupo de recursos da porta de rota expressa.</span><span class="sxs-lookup"><span data-stu-id="b6a50-132">The resource group name of the express route port.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6a50-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6a50-133">CommonParameters</span></span>
<span data-ttu-id="b6a50-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6a50-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6a50-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b6a50-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6a50-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b6a50-136">INPUTS</span></span>

### <span data-ttu-id="b6a50-137">System. String</span><span class="sxs-lookup"><span data-stu-id="b6a50-137">System.String</span></span>

## <span data-ttu-id="b6a50-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b6a50-138">OUTPUTS</span></span>

### <span data-ttu-id="b6a50-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b6a50-139">System.Boolean</span></span>

## <span data-ttu-id="b6a50-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b6a50-140">NOTES</span></span>

## <span data-ttu-id="b6a50-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b6a50-141">RELATED LINKS</span></span>
