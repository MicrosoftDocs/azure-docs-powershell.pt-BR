---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteportloa
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortLOA.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortLOA.md
ms.openlocfilehash: 22f5023aa294dde734157439d8b355916adfb03f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113486"
---
# <span data-ttu-id="2acd9-101">New-AzExpressRoutePortLOA</span><span class="sxs-lookup"><span data-stu-id="2acd9-101">New-AzExpressRoutePortLOA</span></span>

## <span data-ttu-id="2acd9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2acd9-102">SYNOPSIS</span></span>
<span data-ttu-id="2acd9-103">Baixar carta de autorização para uma porta expressa de rota.</span><span class="sxs-lookup"><span data-stu-id="2acd9-103">Download letter of authorization document for an express route port.</span></span>

## <span data-ttu-id="2acd9-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2acd9-104">SYNTAX</span></span>

### <span data-ttu-id="2acd9-105">ResourceNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2acd9-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzExpressRoutePortLOA -PortName <String> -ResourceGroupName <String> -CustomerName <String>
 [-Destination <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2acd9-106">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2acd9-106">ResourceObjectParameterSet</span></span>
```
New-AzExpressRoutePortLOA -ExpressRoutePort <PSExpressRoutePort> -CustomerName <String> [-Destination <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2acd9-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2acd9-107">ResourceIdParameterSet</span></span>
```
New-AzExpressRoutePortLOA -Id <String> -CustomerName <String> [-Destination <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2acd9-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="2acd9-108">DESCRIPTION</span></span>
<span data-ttu-id="2acd9-109">New-AzExpressRoutePortLOA cmdlet baixa uma carta de documento de autorização no formato PDF para uma porta de rota expressa.</span><span class="sxs-lookup"><span data-stu-id="2acd9-109">New-AzExpressRoutePortLOA cmdlet downloads a letter of authorization document in PDF format for an express route port.</span></span>


## <span data-ttu-id="2acd9-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2acd9-110">EXAMPLES</span></span>

### <span data-ttu-id="2acd9-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2acd9-111">Example 1</span></span>
```powershell
PS C:\> New-AzExpressRoutePortLOA -ResourceGroupName myRg -PortName myPort -CustomerName Contoso -Destination loa.pdf
```

<span data-ttu-id="2acd9-112">Baixe a carta de documento de autorização para a porta de rota expressa 'myPort' e armazene-a no arquivo "loa.pdf".</span><span class="sxs-lookup"><span data-stu-id="2acd9-112">Download the letter of authorization document for express route port 'myPort' and store it in file 'loa.pdf'.</span></span>

## <span data-ttu-id="2acd9-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2acd9-113">PARAMETERS</span></span>

### <span data-ttu-id="2acd9-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2acd9-114">-AsJob</span></span>
<span data-ttu-id="2acd9-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="2acd9-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2acd9-116">-CustomerName</span><span class="sxs-lookup"><span data-stu-id="2acd9-116">-CustomerName</span></span>
<span data-ttu-id="2acd9-117">O nome do cliente ao qual esta Porta de Rota Expressa está atribuída.</span><span class="sxs-lookup"><span data-stu-id="2acd9-117">The customer name to whom this Express Route Port is assigned to.</span></span>

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

### <span data-ttu-id="2acd9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2acd9-118">-DefaultProfile</span></span>
<span data-ttu-id="2acd9-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2acd9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2acd9-120">-Destino</span><span class="sxs-lookup"><span data-stu-id="2acd9-120">-Destination</span></span>
<span data-ttu-id="2acd9-121">O caminho do arquivo de saída para armazenar a Carta de Autorização para.</span><span class="sxs-lookup"><span data-stu-id="2acd9-121">The output filepath to store the Letter of Authorization to.</span></span>

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

### <span data-ttu-id="2acd9-122">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="2acd9-122">-ExpressRoutePort</span></span>
<span data-ttu-id="2acd9-123">O recurso de portabilidade de rota expressa.</span><span class="sxs-lookup"><span data-stu-id="2acd9-123">The express route port resource.</span></span>

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

### <span data-ttu-id="2acd9-124">-ID</span><span class="sxs-lookup"><span data-stu-id="2acd9-124">-Id</span></span>
<span data-ttu-id="2acd9-125">ResourceId da porta de rota expressa.</span><span class="sxs-lookup"><span data-stu-id="2acd9-125">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="2acd9-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2acd9-126">-PassThru</span></span>
<span data-ttu-id="2acd9-127">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="2acd9-127">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="2acd9-128">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="2acd9-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2acd9-129">-PortName</span><span class="sxs-lookup"><span data-stu-id="2acd9-129">-PortName</span></span>
<span data-ttu-id="2acd9-130">O nome da porta de rota expressa.</span><span class="sxs-lookup"><span data-stu-id="2acd9-130">The express route port name.</span></span>

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

### <span data-ttu-id="2acd9-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2acd9-131">-ResourceGroupName</span></span>
<span data-ttu-id="2acd9-132">O nome do grupo de recursos da porta de rota expressa.</span><span class="sxs-lookup"><span data-stu-id="2acd9-132">The resource group name of the express route port.</span></span>

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

### <span data-ttu-id="2acd9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2acd9-133">CommonParameters</span></span>
<span data-ttu-id="2acd9-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2acd9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2acd9-135">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2acd9-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2acd9-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="2acd9-136">INPUTS</span></span>

### <span data-ttu-id="2acd9-137">System.String</span><span class="sxs-lookup"><span data-stu-id="2acd9-137">System.String</span></span>

## <span data-ttu-id="2acd9-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="2acd9-138">OUTPUTS</span></span>

### <span data-ttu-id="2acd9-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2acd9-139">System.Boolean</span></span>

## <span data-ttu-id="2acd9-140">Notas</span><span class="sxs-lookup"><span data-stu-id="2acd9-140">NOTES</span></span>

## <span data-ttu-id="2acd9-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2acd9-141">RELATED LINKS</span></span>
