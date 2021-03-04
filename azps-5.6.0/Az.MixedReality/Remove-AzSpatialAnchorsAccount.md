---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/powershell/module/az.mixedreality/remove-azspatialanchorsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzSpatialAnchorsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzSpatialAnchorsAccount.md
ms.openlocfilehash: 502b7b7c97752758003c1a7f0ad007e3e6cf67e1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888932"
---
# <span data-ttu-id="d1f70-101">Remove-AzSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="d1f70-101">Remove-AzSpatialAnchorsAccount</span></span>

## <span data-ttu-id="d1f70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1f70-102">SYNOPSIS</span></span>
<span data-ttu-id="d1f70-103">Excluir Conta de Âncoras Espaciais</span><span class="sxs-lookup"><span data-stu-id="d1f70-103">Delete Spatial Anchors Account</span></span>

## <span data-ttu-id="d1f70-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d1f70-104">SYNTAX</span></span>

### <span data-ttu-id="d1f70-105">DefaultParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d1f70-105">DefaultParameterSet (Default)</span></span>
```
Remove-AzSpatialAnchorsAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1f70-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1f70-106">ResourceIdParameterSet</span></span>
```
Remove-AzSpatialAnchorsAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1f70-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1f70-107">PipelineParameterSet</span></span>
```
Remove-AzSpatialAnchorsAccount -InputObject <PSSpatialAnchorsAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1f70-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d1f70-108">DESCRIPTION</span></span>
<span data-ttu-id="d1f70-109">Exclua a Conta de Âncoras Espaciais especificada de determinado Grupo de Recursos e Assinaturas.</span><span class="sxs-lookup"><span data-stu-id="d1f70-109">Delete specified Spatial Anchors Account from certain Subscription and Resource Group.</span></span>

## <span data-ttu-id="d1f70-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d1f70-110">EXAMPLES</span></span>

### <span data-ttu-id="d1f70-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d1f70-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example
```

<span data-ttu-id="d1f70-112">Excluir a Conta de Âncoras Espaciais "example" do grupo de recursos e assinatura atual "rg1".</span><span class="sxs-lookup"><span data-stu-id="d1f70-112">Delete Spatial Anchors Account "example" from current Subscription and Resource Group "rg1".</span></span>

## <span data-ttu-id="d1f70-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d1f70-113">PARAMETERS</span></span>

### <span data-ttu-id="d1f70-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d1f70-114">-Confirm</span></span>
<span data-ttu-id="d1f70-115">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1f70-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1f70-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1f70-116">-DefaultProfile</span></span>
<span data-ttu-id="d1f70-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d1f70-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1f70-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d1f70-118">-InputObject</span></span>
<span data-ttu-id="d1f70-119">O objeto de domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="d1f70-119">The custom domain object.</span></span>

```yaml
Type: PSSpatialAnchorsAccount
Parameter Sets: PipelineParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1f70-120">-Name</span><span class="sxs-lookup"><span data-stu-id="d1f70-120">-Name</span></span>
<span data-ttu-id="d1f70-121">Nome da conta de Âncoras Espaciais.</span><span class="sxs-lookup"><span data-stu-id="d1f70-121">Spatial Anchors Account Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: SpatialAnchorsAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1f70-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d1f70-122">-PassThru</span></span>
<span data-ttu-id="d1f70-123">Retornar objeto, se especificado.</span><span class="sxs-lookup"><span data-stu-id="d1f70-123">Return object if specified.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1f70-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1f70-124">-ResourceGroupName</span></span>
<span data-ttu-id="d1f70-125">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="d1f70-125">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1f70-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d1f70-126">-ResourceId</span></span>
<span data-ttu-id="d1f70-127">ID de Recurso da Conta de Âncoras Espaciais.</span><span class="sxs-lookup"><span data-stu-id="d1f70-127">Resource ID of Spatial Anchors Account.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1f70-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1f70-128">-WhatIf</span></span>
<span data-ttu-id="d1f70-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d1f70-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1f70-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d1f70-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1f70-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1f70-131">CommonParameters</span></span>
<span data-ttu-id="d1f70-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1f70-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d1f70-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1f70-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1f70-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d1f70-134">INPUTS</span></span>

### <span data-ttu-id="d1f70-135">System.String</span><span class="sxs-lookup"><span data-stu-id="d1f70-135">System.String</span></span>

### <span data-ttu-id="d1f70-136">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="d1f70-136">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

### <span data-ttu-id="d1f70-137">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d1f70-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d1f70-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d1f70-138">OUTPUTS</span></span>

### <span data-ttu-id="d1f70-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d1f70-139">System.Boolean</span></span>

## <span data-ttu-id="d1f70-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="d1f70-140">NOTES</span></span>

## <span data-ttu-id="d1f70-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d1f70-141">RELATED LINKS</span></span>
