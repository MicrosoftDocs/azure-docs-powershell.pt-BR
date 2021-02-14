---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualApplianceSite.md
ms.openlocfilehash: 0b29719dee8a1e69d27dd36cee2888df4575eefc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117334"
---
# <span data-ttu-id="0088b-101">Remove-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="0088b-101">Remove-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="0088b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0088b-102">SYNOPSIS</span></span>
<span data-ttu-id="0088b-103">Remova um site de dispositivo virtual de um recurso de Dispositivo Virtual de Rede.</span><span class="sxs-lookup"><span data-stu-id="0088b-103">Remove a virtual appliance site from a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="0088b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0088b-104">SYNTAX</span></span>

### <span data-ttu-id="0088b-105">ResourceNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0088b-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzVirtualApplianceSite -Name <String> -NetworkVirtualApplianceId <String> -ResourceGroupName <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0088b-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0088b-106">ResourceIdParameterSet</span></span>
```
Remove-AzVirtualApplianceSite -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0088b-107">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0088b-107">ResourceObjectParameterSet</span></span>
```
Remove-AzVirtualApplianceSite -VirtualApplianceSite <PSVirtualApplianceSite> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0088b-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="0088b-108">DESCRIPTION</span></span>
<span data-ttu-id="0088b-109">O comando Remove-AzVirtualApplianceSite remover um site de Dispositivo Virtual de um recurso de Dispositivo Virtual de Rede.</span><span class="sxs-lookup"><span data-stu-id="0088b-109">The Remove-AzVirtualApplianceSite command removes a Virtual Appliance site from a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="0088b-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0088b-110">EXAMPLES</span></span>

### <span data-ttu-id="0088b-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0088b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzVirtualApplianceSite -Name testsite -ResourceGroupName testrg -NetworkVirtualApplianceId $nva.Id
```

<span data-ttu-id="0088b-112">Excluir um recurso de site de Dispositivo Virtual.</span><span class="sxs-lookup"><span data-stu-id="0088b-112">Delete a Virtual Appliance site resource.</span></span> 

## <span data-ttu-id="0088b-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0088b-113">PARAMETERS</span></span>

### <span data-ttu-id="0088b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0088b-114">-AsJob</span></span>
<span data-ttu-id="0088b-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="0088b-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0088b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0088b-116">-DefaultProfile</span></span>
<span data-ttu-id="0088b-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0088b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0088b-118">-Forçar</span><span class="sxs-lookup"><span data-stu-id="0088b-118">-Force</span></span>
<span data-ttu-id="0088b-119">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="0088b-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="0088b-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="0088b-120">-Name</span></span>
<span data-ttu-id="0088b-121">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="0088b-121">The resource name.</span></span>

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

### <span data-ttu-id="0088b-122">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="0088b-122">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="0088b-123">A ID de recurso do Dispositivo Virtual de Rede associado a este site.</span><span class="sxs-lookup"><span data-stu-id="0088b-123">The resource ID of the Network Virtual Appliance associated with this site.</span></span>

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

### <span data-ttu-id="0088b-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0088b-124">-PassThru</span></span>
<span data-ttu-id="0088b-125">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="0088b-125">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="0088b-126">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="0088b-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0088b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0088b-127">-ResourceGroupName</span></span>
<span data-ttu-id="0088b-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0088b-128">The resource group name.</span></span>

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

### <span data-ttu-id="0088b-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0088b-129">-ResourceId</span></span>
<span data-ttu-id="0088b-130">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="0088b-130">The resource id.</span></span>

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

### <span data-ttu-id="0088b-131">-VirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="0088b-131">-VirtualApplianceSite</span></span>
<span data-ttu-id="0088b-132">O objeto do site de dispositivo virtual.</span><span class="sxs-lookup"><span data-stu-id="0088b-132">The virtual appliance site object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite
Parameter Sets: ResourceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0088b-133">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="0088b-133">-Confirm</span></span>
<span data-ttu-id="0088b-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0088b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0088b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0088b-135">-WhatIf</span></span>
<span data-ttu-id="0088b-136">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="0088b-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0088b-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0088b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0088b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0088b-138">CommonParameters</span></span>
<span data-ttu-id="0088b-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0088b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0088b-140">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0088b-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0088b-141">Entradas</span><span class="sxs-lookup"><span data-stu-id="0088b-141">INPUTS</span></span>

### <span data-ttu-id="0088b-142">System.String</span><span class="sxs-lookup"><span data-stu-id="0088b-142">System.String</span></span>

### <span data-ttu-id="0088b-143">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="0088b-143">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="0088b-144">Saídas</span><span class="sxs-lookup"><span data-stu-id="0088b-144">OUTPUTS</span></span>

### <span data-ttu-id="0088b-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0088b-145">System.Boolean</span></span>

## <span data-ttu-id="0088b-146">Notas</span><span class="sxs-lookup"><span data-stu-id="0088b-146">NOTES</span></span>

## <span data-ttu-id="0088b-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0088b-147">RELATED LINKS</span></span>
