---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualApplianceSite.md
ms.openlocfilehash: 0b29719dee8a1e69d27dd36cee2888df4575eefc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429527"
---
# <span data-ttu-id="d1d8b-101">Remove-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="d1d8b-101">Remove-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="d1d8b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d1d8b-102">SYNOPSIS</span></span>
<span data-ttu-id="d1d8b-103">Remova um site de dispositivo virtual de um recurso de dispositivo virtual de rede.</span><span class="sxs-lookup"><span data-stu-id="d1d8b-103">Remove a virtual appliance site from a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="d1d8b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d1d8b-104">SYNTAX</span></span>

### <span data-ttu-id="d1d8b-105">ResourceNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="d1d8b-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzVirtualApplianceSite -Name <String> -NetworkVirtualApplianceId <String> -ResourceGroupName <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d1d8b-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1d8b-106">ResourceIdParameterSet</span></span>
```
Remove-AzVirtualApplianceSite -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1d8b-107">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1d8b-107">ResourceObjectParameterSet</span></span>
```
Remove-AzVirtualApplianceSite -VirtualApplianceSite <PSVirtualApplianceSite> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1d8b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d1d8b-108">DESCRIPTION</span></span>
<span data-ttu-id="d1d8b-109">O comando Remove-AzVirtualApplianceSite remove um site de dispositivo virtual de um recurso de aplicativo virtual de rede.</span><span class="sxs-lookup"><span data-stu-id="d1d8b-109">The Remove-AzVirtualApplianceSite command removes a Virtual Appliance site from a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="d1d8b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d1d8b-110">EXAMPLES</span></span>

### <span data-ttu-id="d1d8b-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d1d8b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzVirtualApplianceSite -Name testsite -ResourceGroupName testrg -NetworkVirtualApplianceId $nva.Id
```

<span data-ttu-id="d1d8b-112">Exclua um recurso de site de dispositivo virtual.</span><span class="sxs-lookup"><span data-stu-id="d1d8b-112">Delete a Virtual Appliance site resource.</span></span> 

## <span data-ttu-id="d1d8b-113">OS</span><span class="sxs-lookup"><span data-stu-id="d1d8b-113">PARAMETERS</span></span>

### <span data-ttu-id="d1d8b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d1d8b-114">-AsJob</span></span>
<span data-ttu-id="d1d8b-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="d1d8b-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d1d8b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1d8b-116">-DefaultProfile</span></span>
<span data-ttu-id="d1d8b-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d1d8b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1d8b-118">-Force</span><span class="sxs-lookup"><span data-stu-id="d1d8b-118">-Force</span></span>
<span data-ttu-id="d1d8b-119">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="d1d8b-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="d1d8b-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="d1d8b-120">-Name</span></span>
<span data-ttu-id="d1d8b-121">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="d1d8b-121">The resource name.</span></span>

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

### <span data-ttu-id="d1d8b-122">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="d1d8b-122">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="d1d8b-123">A ID do recurso do aplicativo virtual de rede associado a este site.</span><span class="sxs-lookup"><span data-stu-id="d1d8b-123">The resource ID of the Network Virtual Appliance associated with this site.</span></span>

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

### <span data-ttu-id="d1d8b-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d1d8b-124">-PassThru</span></span>
<span data-ttu-id="d1d8b-125">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="d1d8b-125">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="d1d8b-126">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="d1d8b-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d1d8b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1d8b-127">-ResourceGroupName</span></span>
<span data-ttu-id="d1d8b-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d1d8b-128">The resource group name.</span></span>

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

### <span data-ttu-id="d1d8b-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d1d8b-129">-ResourceId</span></span>
<span data-ttu-id="d1d8b-130">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="d1d8b-130">The resource id.</span></span>

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

### <span data-ttu-id="d1d8b-131">-VirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="d1d8b-131">-VirtualApplianceSite</span></span>
<span data-ttu-id="d1d8b-132">O objeto de site de dispositivo virtual.</span><span class="sxs-lookup"><span data-stu-id="d1d8b-132">The virtual appliance site object.</span></span>

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

### <span data-ttu-id="d1d8b-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d1d8b-133">-Confirm</span></span>
<span data-ttu-id="d1d8b-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1d8b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1d8b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1d8b-135">-WhatIf</span></span>
<span data-ttu-id="d1d8b-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d1d8b-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1d8b-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d1d8b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1d8b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1d8b-138">CommonParameters</span></span>
<span data-ttu-id="d1d8b-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1d8b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1d8b-140">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d1d8b-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1d8b-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d1d8b-141">INPUTS</span></span>

### <span data-ttu-id="d1d8b-142">System. String</span><span class="sxs-lookup"><span data-stu-id="d1d8b-142">System.String</span></span>

### <span data-ttu-id="d1d8b-143">Microsoft. Azure. Commands. Network. Models. PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="d1d8b-143">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="d1d8b-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d1d8b-144">OUTPUTS</span></span>

### <span data-ttu-id="d1d8b-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d1d8b-145">System.Boolean</span></span>

## <span data-ttu-id="d1d8b-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d1d8b-146">NOTES</span></span>

## <span data-ttu-id="d1d8b-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d1d8b-147">RELATED LINKS</span></span>
