---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRoutePort.md
ms.openlocfilehash: 5a9e4f7a4a3d7b8173cf7ef797edfc354d655cc3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429441"
---
# <span data-ttu-id="f4b9f-101">Remove-AzureRmExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="f4b9f-101">Remove-AzureRmExpressRoutePort</span></span>

## <span data-ttu-id="f4b9f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f4b9f-102">SYNOPSIS</span></span>
<span data-ttu-id="f4b9f-103">Remove um ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="f4b9f-103">Removes an ExpressRoutePort.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4b9f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f4b9f-104">SYNTAX</span></span>

### <span data-ttu-id="f4b9f-105">ResourceNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="f4b9f-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzureRmExpressRoutePort -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4b9f-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4b9f-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmExpressRoutePort -InputObject <PSExpressRoutePort> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4b9f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4b9f-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmExpressRoutePort -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4b9f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f4b9f-108">DESCRIPTION</span></span>
<span data-ttu-id="f4b9f-109">O cmdlet **Remove-AzureRmExpressRoutePort** remove um ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="f4b9f-109">The **Remove-AzureRmExpressRoutePort** cmdlet removes an ExpressRoutePort.</span></span>

## <span data-ttu-id="f4b9f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f4b9f-110">EXAMPLES</span></span>

### <span data-ttu-id="f4b9f-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f4b9f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmExpressRoutePort -Name $PortName -ResourceGroupName $rg
```

<span data-ttu-id="f4b9f-112">Remove $PortName recurso ExpressRoutePort em $rg grupo de recursos na sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="f4b9f-112">Removes $PortName ExpressRoutePort resource in $rg resource group in your subscription.</span></span>

### <span data-ttu-id="f4b9f-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="f4b9f-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzureRmExpressRoutePort -InputObject $erPort
```
<span data-ttu-id="f4b9f-114">Remove o recurso ExpressRoutePort em InputObject.</span><span class="sxs-lookup"><span data-stu-id="f4b9f-114">Removes the ExpressRoutePort resource in InputObject.</span></span>

### <span data-ttu-id="f4b9f-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="f4b9f-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzureRmExpressRoutePort -Name $ResourceId $id
```

<span data-ttu-id="f4b9f-116">Remove o recurso ExpressRoutePort com $id ResourceId.</span><span class="sxs-lookup"><span data-stu-id="f4b9f-116">Removes the ExpressRoutePort resource with ResourceId $id.</span></span>

## <span data-ttu-id="f4b9f-117">OS</span><span class="sxs-lookup"><span data-stu-id="f4b9f-117">PARAMETERS</span></span>

### <span data-ttu-id="f4b9f-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f4b9f-118">-AsJob</span></span>
<span data-ttu-id="f4b9f-119">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="f4b9f-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f4b9f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4b9f-120">-DefaultProfile</span></span>
<span data-ttu-id="f4b9f-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f4b9f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4b9f-122">-Force</span><span class="sxs-lookup"><span data-stu-id="f4b9f-122">-Force</span></span>
<span data-ttu-id="f4b9f-123">Não pedir confirmação se quiser excluir o recurso</span><span class="sxs-lookup"><span data-stu-id="f4b9f-123">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="f4b9f-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4b9f-124">-InputObject</span></span>
<span data-ttu-id="f4b9f-125">O objeto porta de rota expressa</span><span class="sxs-lookup"><span data-stu-id="f4b9f-125">The express route port object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4b9f-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="f4b9f-126">-Name</span></span>
<span data-ttu-id="f4b9f-127">O nome do ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="f4b9f-127">The name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4b9f-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f4b9f-128">-PassThru</span></span>
<span data-ttu-id="f4b9f-129">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="f4b9f-129">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="f4b9f-130">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="f4b9f-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f4b9f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4b9f-131">-ResourceGroupName</span></span>
<span data-ttu-id="f4b9f-132">O nome do grupo de recursos do ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="f4b9f-132">The resource group name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4b9f-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4b9f-133">-ResourceId</span></span>
<span data-ttu-id="f4b9f-134">ResourceId da porta de rota expressa.</span><span class="sxs-lookup"><span data-stu-id="f4b9f-134">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="f4b9f-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f4b9f-135">-Confirm</span></span>
<span data-ttu-id="f4b9f-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4b9f-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4b9f-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4b9f-137">-WhatIf</span></span>
<span data-ttu-id="f4b9f-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f4b9f-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4b9f-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f4b9f-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4b9f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4b9f-140">CommonParameters</span></span>
<span data-ttu-id="f4b9f-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4b9f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4b9f-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4b9f-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4b9f-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f4b9f-143">INPUTS</span></span>

### <span data-ttu-id="f4b9f-144">System. String</span><span class="sxs-lookup"><span data-stu-id="f4b9f-144">System.String</span></span>

### <span data-ttu-id="f4b9f-145">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="f4b9f-145">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="f4b9f-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f4b9f-146">OUTPUTS</span></span>

### <span data-ttu-id="f4b9f-147">System. Object</span><span class="sxs-lookup"><span data-stu-id="f4b9f-147">System.Object</span></span>
## <span data-ttu-id="f4b9f-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f4b9f-148">NOTES</span></span>

## <span data-ttu-id="f4b9f-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f4b9f-149">RELATED LINKS</span></span>
