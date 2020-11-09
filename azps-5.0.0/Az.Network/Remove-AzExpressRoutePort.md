---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePort.md
ms.openlocfilehash: 7e6ee711de551de00a54930be2bdb285998e3ccb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94283859"
---
# <span data-ttu-id="ba638-101">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="ba638-101">Remove-AzExpressRoutePort</span></span>

## <span data-ttu-id="ba638-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ba638-102">SYNOPSIS</span></span>
<span data-ttu-id="ba638-103">Remove um ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="ba638-103">Removes an ExpressRoutePort.</span></span>

## <span data-ttu-id="ba638-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ba638-104">SYNTAX</span></span>

### <span data-ttu-id="ba638-105">ResourceNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="ba638-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzExpressRoutePort -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba638-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba638-106">InputObjectParameterSet</span></span>
```
Remove-AzExpressRoutePort -InputObject <PSExpressRoutePort> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba638-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba638-107">ResourceIdParameterSet</span></span>
```
Remove-AzExpressRoutePort -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba638-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ba638-108">DESCRIPTION</span></span>
<span data-ttu-id="ba638-109">O cmdlet **Remove-AzExpressRoutePort** remove um ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="ba638-109">The **Remove-AzExpressRoutePort** cmdlet removes an ExpressRoutePort.</span></span>

## <span data-ttu-id="ba638-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ba638-110">EXAMPLES</span></span>

### <span data-ttu-id="ba638-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ba638-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
```

<span data-ttu-id="ba638-112">Remove $PortName recurso ExpressRoutePort em $rg grupo de recursos na sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="ba638-112">Removes $PortName ExpressRoutePort resource in $rg resource group in your subscription.</span></span>

### <span data-ttu-id="ba638-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ba638-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzExpressRoutePort -InputObject $erPort
```

<span data-ttu-id="ba638-114">Remove o recurso ExpressRoutePort em InputObject.</span><span class="sxs-lookup"><span data-stu-id="ba638-114">Removes the ExpressRoutePort resource in InputObject.</span></span>

### <span data-ttu-id="ba638-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="ba638-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzExpressRoutePort -Name $ResourceId $id
```

<span data-ttu-id="ba638-116">Remove o recurso ExpressRoutePort com $id ResourceId.</span><span class="sxs-lookup"><span data-stu-id="ba638-116">Removes the ExpressRoutePort resource with ResourceId $id.</span></span>

## <span data-ttu-id="ba638-117">OS</span><span class="sxs-lookup"><span data-stu-id="ba638-117">PARAMETERS</span></span>

### <span data-ttu-id="ba638-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ba638-118">-AsJob</span></span>
<span data-ttu-id="ba638-119">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="ba638-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ba638-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba638-120">-DefaultProfile</span></span>
<span data-ttu-id="ba638-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ba638-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba638-122">-Force</span><span class="sxs-lookup"><span data-stu-id="ba638-122">-Force</span></span>
<span data-ttu-id="ba638-123">Não pedir confirmação se quiser excluir o recurso</span><span class="sxs-lookup"><span data-stu-id="ba638-123">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="ba638-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ba638-124">-InputObject</span></span>
<span data-ttu-id="ba638-125">O objeto porta de rota expressa</span><span class="sxs-lookup"><span data-stu-id="ba638-125">The express route port object</span></span>

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

### <span data-ttu-id="ba638-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="ba638-126">-Name</span></span>
<span data-ttu-id="ba638-127">O nome do ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="ba638-127">The name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="ba638-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ba638-128">-PassThru</span></span>
<span data-ttu-id="ba638-129">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="ba638-129">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="ba638-130">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="ba638-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ba638-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba638-131">-ResourceGroupName</span></span>
<span data-ttu-id="ba638-132">O nome do grupo de recursos do ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="ba638-132">The resource group name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="ba638-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ba638-133">-ResourceId</span></span>
<span data-ttu-id="ba638-134">ResourceId da porta de rota expressa.</span><span class="sxs-lookup"><span data-stu-id="ba638-134">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="ba638-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ba638-135">-Confirm</span></span>
<span data-ttu-id="ba638-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba638-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba638-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba638-137">-WhatIf</span></span>
<span data-ttu-id="ba638-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ba638-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba638-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ba638-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba638-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba638-140">CommonParameters</span></span>
<span data-ttu-id="ba638-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba638-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba638-142">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba638-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba638-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ba638-143">INPUTS</span></span>

### <span data-ttu-id="ba638-144">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="ba638-144">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

### <span data-ttu-id="ba638-145">System. String</span><span class="sxs-lookup"><span data-stu-id="ba638-145">System.String</span></span>

## <span data-ttu-id="ba638-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ba638-146">OUTPUTS</span></span>

### <span data-ttu-id="ba638-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ba638-147">System.Boolean</span></span>

## <span data-ttu-id="ba638-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ba638-148">NOTES</span></span>

## <span data-ttu-id="ba638-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ba638-149">RELATED LINKS</span></span>

[<span data-ttu-id="ba638-150">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="ba638-150">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="ba638-151">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="ba638-151">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="ba638-152">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="ba638-152">Set-AzExpressRoutePort</span></span>](./Set-AzExpressRoutePort.md)
