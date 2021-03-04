---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2DBAF415-A039-479E-B3CA-E00FD5E476C9
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyAssignment.md
ms.openlocfilehash: 010f8be0a96499415ac78c584ebad1c10acf4523
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885846"
---
# <span data-ttu-id="15295-101">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="15295-101">Get-AzPolicyAssignment</span></span>

## <span data-ttu-id="15295-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15295-102">SYNOPSIS</span></span>
<span data-ttu-id="15295-103">Obtém atribuições de política.</span><span class="sxs-lookup"><span data-stu-id="15295-103">Gets policy assignments.</span></span>

## <span data-ttu-id="15295-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="15295-104">SYNTAX</span></span>

### <span data-ttu-id="15295-105">DefaultParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="15295-105">DefaultParameterSet (Default)</span></span>
```
Get-AzPolicyAssignment [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="15295-106">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="15295-106">NameParameterSet</span></span>
```
Get-AzPolicyAssignment [-Name <String>] [-Scope <String>] [-PolicyDefinitionId <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15295-107">IncludeDescendentParameterSet</span><span class="sxs-lookup"><span data-stu-id="15295-107">IncludeDescendentParameterSet</span></span>
```
Get-AzPolicyAssignment [-Scope <String>] [-IncludeDescendent] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15295-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="15295-108">IdParameterSet</span></span>
```
Get-AzPolicyAssignment -Id <String> [-PolicyDefinitionId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15295-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="15295-109">DESCRIPTION</span></span>
<span data-ttu-id="15295-110">O cmdlet **Get-AzPolicyAssignment** obtém todas as atribuições de política ou atribuições específicas.</span><span class="sxs-lookup"><span data-stu-id="15295-110">The **Get-AzPolicyAssignment** cmdlet gets all policy assignments or particular assignments.</span></span>
<span data-ttu-id="15295-111">Identifique uma atribuição de política para obter por nome e escopo ou por ID.</span><span class="sxs-lookup"><span data-stu-id="15295-111">Identify a policy assignment to get by name and scope or by ID.</span></span>

## <span data-ttu-id="15295-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="15295-112">EXAMPLES</span></span>

### <span data-ttu-id="15295-113">Exemplo 1: Obter todas as atribuições de política</span><span class="sxs-lookup"><span data-stu-id="15295-113">Example 1: Get all policy assignments</span></span>
```
PS C:\> Get-AzPolicyAssignment
```

<span data-ttu-id="15295-114">Este comando obtém todas as atribuições de política.</span><span class="sxs-lookup"><span data-stu-id="15295-114">This command gets all the policy assignments.</span></span>

### <span data-ttu-id="15295-115">Exemplo 2: Obter uma atribuição de política específica</span><span class="sxs-lookup"><span data-stu-id="15295-115">Example 2: Get a specific policy assignment</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> Get-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="15295-116">O primeiro comando obtém um grupo de recursos chamado ResourceGroup11 usando o cmdlet Get-AzResourceGroup e o armazena na variável $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="15295-116">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="15295-117">O segundo comando obtém a atribuição de política chamada PolicyAssignment07 para o escopo que a **propriedade ResourceId** do $ResourceGroup identifica.</span><span class="sxs-lookup"><span data-stu-id="15295-117">The second command gets the policy assignment named PolicyAssignment07 for the scope that the **ResourceId** property of $ResourceGroup identifies.</span></span>

### <span data-ttu-id="15295-118">Exemplo 3: Obter todas as atribuições de política atribuídas a um grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="15295-118">Example 3: Get all policy assignments assigned to a management group</span></span>
```
PS C:\> $mgId = 'myManagementGroup'
PS C:\> Get-AzPolicyAssignment -Scope '/providers/Microsoft.Management/managementgroups/$mgId'
```

<span data-ttu-id="15295-119">O primeiro comando especifica a ID do grupo de gerenciamento a ser consultado.</span><span class="sxs-lookup"><span data-stu-id="15295-119">The first command specifies the ID of the management group to query.</span></span>
<span data-ttu-id="15295-120">O segundo comando obtém todas as atribuições de política atribuídas ao grupo de gerenciamento com iD 'myManagementGroup'.</span><span class="sxs-lookup"><span data-stu-id="15295-120">The second command gets all of the policy assignments that are assigned to the management group with ID 'myManagementGroup'.</span></span>

## <span data-ttu-id="15295-121">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="15295-121">PARAMETERS</span></span>

### <span data-ttu-id="15295-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="15295-122">-ApiVersion</span></span>
<span data-ttu-id="15295-123">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="15295-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="15295-124">Se você não especificar uma versão, este cmdlet usará a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="15295-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="15295-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15295-125">-DefaultProfile</span></span>
<span data-ttu-id="15295-126">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="15295-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="15295-127">-Id</span><span class="sxs-lookup"><span data-stu-id="15295-127">-Id</span></span>
<span data-ttu-id="15295-128">Especifica a ID de recurso totalmente qualificada para a atribuição de política que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="15295-128">Specifies the fully qualified resource ID for the policy assignment that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15295-129">-IncludeDescendent</span><span class="sxs-lookup"><span data-stu-id="15295-129">-IncludeDescendent</span></span>
<span data-ttu-id="15295-130">Faz com que a lista de atribuições de política retornadas inclua todas as atribuições relacionadas ao escopo determinado, incluindo as de escopos ancestrais e aquelas de escopos descendentes.</span><span class="sxs-lookup"><span data-stu-id="15295-130">Causes the list of returned policy assignments to include all assignments related to the given scope, including those from ancestor scopes and those from descendent scopes.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: IncludeDescendentParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15295-131">-Name</span><span class="sxs-lookup"><span data-stu-id="15295-131">-Name</span></span>
<span data-ttu-id="15295-132">Especifica o nome da atribuição de política que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="15295-132">Specifies the name of the policy assignment that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15295-133">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="15295-133">-PolicyDefinitionId</span></span>
<span data-ttu-id="15295-134">Especifica a ID da definição de política das atribuições de política que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="15295-134">Specifies the ID of the policy definition of the policy assignments that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, IdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15295-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="15295-135">-Pre</span></span>
<span data-ttu-id="15295-136">Indica que esse cmdlet considera versões da API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="15295-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="15295-137">-Scope</span><span class="sxs-lookup"><span data-stu-id="15295-137">-Scope</span></span>
<span data-ttu-id="15295-138">Especifica o escopo no qual a política é aplicada para a atribuição que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="15295-138">Specifies the scope at which the policy is applied for the assignment that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, IncludeDescendentParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15295-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15295-139">CommonParameters</span></span>
<span data-ttu-id="15295-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15295-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15295-141">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="15295-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15295-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="15295-142">INPUTS</span></span>

### <span data-ttu-id="15295-143">System.String</span><span class="sxs-lookup"><span data-stu-id="15295-143">System.String</span></span>

### <span data-ttu-id="15295-144">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="15295-144">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="15295-145">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="15295-145">OUTPUTS</span></span>

### <span data-ttu-id="15295-146">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="15295-146">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="15295-147">NOTES</span><span class="sxs-lookup"><span data-stu-id="15295-147">NOTES</span></span>

## <span data-ttu-id="15295-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="15295-148">RELATED LINKS</span></span>

[<span data-ttu-id="15295-149">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="15295-149">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="15295-150">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="15295-150">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)

[<span data-ttu-id="15295-151">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="15295-151">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


