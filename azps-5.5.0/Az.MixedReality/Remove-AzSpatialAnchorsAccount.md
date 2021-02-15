---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/remove-azspatialanchorsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzSpatialAnchorsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzSpatialAnchorsAccount.md
ms.openlocfilehash: 5ba079a17dcfb0a263766237adbbec9beb4cc64c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117548"
---
# <span data-ttu-id="b3eeb-101">Remove-AzSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="b3eeb-101">Remove-AzSpatialAnchorsAccount</span></span>

## <span data-ttu-id="b3eeb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b3eeb-102">SYNOPSIS</span></span>
<span data-ttu-id="b3eeb-103">Excluir Conta de Âncoras Descontinuar</span><span class="sxs-lookup"><span data-stu-id="b3eeb-103">Delete Spatial Anchors Account</span></span>

## <span data-ttu-id="b3eeb-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b3eeb-104">SYNTAX</span></span>

### <span data-ttu-id="b3eeb-105">DefaultParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b3eeb-105">DefaultParameterSet (Default)</span></span>
```
Remove-AzSpatialAnchorsAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3eeb-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3eeb-106">ResourceIdParameterSet</span></span>
```
Remove-AzSpatialAnchorsAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3eeb-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3eeb-107">PipelineParameterSet</span></span>
```
Remove-AzSpatialAnchorsAccount -InputObject <PSSpatialAnchorsAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3eeb-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="b3eeb-108">DESCRIPTION</span></span>
<span data-ttu-id="b3eeb-109">Exclua a Conta de Âncoras Desaportivas especificada de determinado Grupo de Recursos e Assinaturas.</span><span class="sxs-lookup"><span data-stu-id="b3eeb-109">Delete specified Spatial Anchors Account from certain Subscription and Resource Group.</span></span>

## <span data-ttu-id="b3eeb-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b3eeb-110">EXAMPLES</span></span>

### <span data-ttu-id="b3eeb-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b3eeb-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example
```

<span data-ttu-id="b3eeb-112">Exclua a Conta de Âncoras Desaportivas "exemplo" da assinatura atual e grupo de recursos "rg1".</span><span class="sxs-lookup"><span data-stu-id="b3eeb-112">Delete Spatial Anchors Account "example" from current Subscription and Resource Group "rg1".</span></span>

## <span data-ttu-id="b3eeb-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b3eeb-113">PARAMETERS</span></span>

### <span data-ttu-id="b3eeb-114">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="b3eeb-114">-Confirm</span></span>
<span data-ttu-id="b3eeb-115">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3eeb-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3eeb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3eeb-116">-DefaultProfile</span></span>
<span data-ttu-id="b3eeb-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b3eeb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3eeb-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3eeb-118">-InputObject</span></span>
<span data-ttu-id="b3eeb-119">O objeto de domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="b3eeb-119">The custom domain object.</span></span>

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

### <span data-ttu-id="b3eeb-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="b3eeb-120">-Name</span></span>
<span data-ttu-id="b3eeb-121">Nome da conta De âncoras de espaço.</span><span class="sxs-lookup"><span data-stu-id="b3eeb-121">Spatial Anchors Account Name.</span></span>

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

### <span data-ttu-id="b3eeb-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b3eeb-122">-PassThru</span></span>
<span data-ttu-id="b3eeb-123">Retornar objeto, se especificado.</span><span class="sxs-lookup"><span data-stu-id="b3eeb-123">Return object if specified.</span></span>

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

### <span data-ttu-id="b3eeb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3eeb-124">-ResourceGroupName</span></span>
<span data-ttu-id="b3eeb-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b3eeb-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="b3eeb-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b3eeb-126">-ResourceId</span></span>
<span data-ttu-id="b3eeb-127">ID do Recurso da Conta de Âncoras Desarmada.</span><span class="sxs-lookup"><span data-stu-id="b3eeb-127">Resource ID of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="b3eeb-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3eeb-128">-WhatIf</span></span>
<span data-ttu-id="b3eeb-129">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="b3eeb-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3eeb-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b3eeb-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3eeb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3eeb-131">CommonParameters</span></span>
<span data-ttu-id="b3eeb-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3eeb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b3eeb-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3eeb-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3eeb-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="b3eeb-134">INPUTS</span></span>

### <span data-ttu-id="b3eeb-135">System.String</span><span class="sxs-lookup"><span data-stu-id="b3eeb-135">System.String</span></span>

### <span data-ttu-id="b3eeb-136">Microsoft.Azure.Commands.MixedReality.GeoespaciaisAccount.PSSárialEstaresAccount</span><span class="sxs-lookup"><span data-stu-id="b3eeb-136">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

### <span data-ttu-id="b3eeb-137">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b3eeb-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b3eeb-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="b3eeb-138">OUTPUTS</span></span>

### <span data-ttu-id="b3eeb-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b3eeb-139">System.Boolean</span></span>

## <span data-ttu-id="b3eeb-140">Notas</span><span class="sxs-lookup"><span data-stu-id="b3eeb-140">NOTES</span></span>

## <span data-ttu-id="b3eeb-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b3eeb-141">RELATED LINKS</span></span>
