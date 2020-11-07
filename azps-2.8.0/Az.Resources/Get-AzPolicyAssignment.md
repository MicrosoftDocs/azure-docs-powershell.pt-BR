---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2DBAF415-A039-479E-B3CA-E00FD5E476C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyAssignment.md
ms.openlocfilehash: e2cce15271b1289a2d6bfe5f8874f004ba95a04b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773364"
---
# <span data-ttu-id="61fcf-101">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="61fcf-101">Get-AzPolicyAssignment</span></span>

## <span data-ttu-id="61fcf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="61fcf-102">SYNOPSIS</span></span>
<span data-ttu-id="61fcf-103">Obtém atribuições de política.</span><span class="sxs-lookup"><span data-stu-id="61fcf-103">Gets policy assignments.</span></span>

## <span data-ttu-id="61fcf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="61fcf-104">SYNTAX</span></span>

### <span data-ttu-id="61fcf-105">DefaultParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="61fcf-105">DefaultParameterSet (Default)</span></span>
```
Get-AzPolicyAssignment [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="61fcf-106">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="61fcf-106">NameParameterSet</span></span>
```
Get-AzPolicyAssignment [-Name <String>] [-Scope <String>] [-PolicyDefinitionId <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61fcf-107">IncludeDescendentParameterSet</span><span class="sxs-lookup"><span data-stu-id="61fcf-107">IncludeDescendentParameterSet</span></span>
```
Get-AzPolicyAssignment [-Scope <String>] [-IncludeDescendent] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61fcf-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="61fcf-108">IdParameterSet</span></span>
```
Get-AzPolicyAssignment -Id <String> [-PolicyDefinitionId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61fcf-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="61fcf-109">DESCRIPTION</span></span>
<span data-ttu-id="61fcf-110">O cmdlet **Get-AzPolicyAssignment** obtém todas as atribuições de política ou atribuições específicas.</span><span class="sxs-lookup"><span data-stu-id="61fcf-110">The **Get-AzPolicyAssignment** cmdlet gets all policy assignments or particular assignments.</span></span>
<span data-ttu-id="61fcf-111">Identifique uma atribuição de política para obter por nome e escopo ou por ID.</span><span class="sxs-lookup"><span data-stu-id="61fcf-111">Identify a policy assignment to get by name and scope or by ID.</span></span>

## <span data-ttu-id="61fcf-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="61fcf-112">EXAMPLES</span></span>

### <span data-ttu-id="61fcf-113">Exemplo 1: obter todas as atribuições de política</span><span class="sxs-lookup"><span data-stu-id="61fcf-113">Example 1: Get all policy assignments</span></span>
```
PS C:\> Get-AzPolicyAssignment
```

<span data-ttu-id="61fcf-114">Este comando obtém todas as atribuições de política.</span><span class="sxs-lookup"><span data-stu-id="61fcf-114">This command gets all the policy assignments.</span></span>

### <span data-ttu-id="61fcf-115">Exemplo 2: obter uma atribuição de política específica</span><span class="sxs-lookup"><span data-stu-id="61fcf-115">Example 2: Get a specific policy assignment</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> Get-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="61fcf-116">O primeiro comando obtém um grupo de recursos chamado ResourceGroup11 usando o cmdlet Get-AzResourceGroup e o armazena na variável $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="61fcf-116">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="61fcf-117">O segundo comando obtém a atribuição de política chamada PolicyAssignment07 para o escopo que a propriedade **ResourceId** de $ResourceGroup identifica.</span><span class="sxs-lookup"><span data-stu-id="61fcf-117">The second command gets the policy assignment named PolicyAssignment07 for the scope that the **ResourceId** property of $ResourceGroup identifies.</span></span>

### <span data-ttu-id="61fcf-118">Exemplo 3: obter todas as atribuições de política atribuídas a um grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="61fcf-118">Example 3: Get all policy assignments assigned to a management group</span></span>
```
PS C:\> $mgId = 'myManagementGroup'
PS C:\> Get-AzPolicyAssignment -Scope '/providers/Microsoft.Management/managementgroups/$mgId'
```

<span data-ttu-id="61fcf-119">O primeiro comando especifica a ID do grupo de gerenciamento a ser consultado.</span><span class="sxs-lookup"><span data-stu-id="61fcf-119">The first command specifies the ID of the management group to query.</span></span>
<span data-ttu-id="61fcf-120">O segundo comando obtém todas as atribuições de política atribuídas ao grupo de gerenciamento com ID ' mymanagement Group '.</span><span class="sxs-lookup"><span data-stu-id="61fcf-120">The second command gets all of the policy assignments that are assigned to the management group with ID 'myManagementGroup'.</span></span>

## <span data-ttu-id="61fcf-121">OS</span><span class="sxs-lookup"><span data-stu-id="61fcf-121">PARAMETERS</span></span>

### <span data-ttu-id="61fcf-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="61fcf-122">-ApiVersion</span></span>
<span data-ttu-id="61fcf-123">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="61fcf-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="61fcf-124">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="61fcf-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="61fcf-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61fcf-125">-DefaultProfile</span></span>
<span data-ttu-id="61fcf-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="61fcf-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="61fcf-127">-ID</span><span class="sxs-lookup"><span data-stu-id="61fcf-127">-Id</span></span>
<span data-ttu-id="61fcf-128">Especifica a ID de recurso totalmente qualificado para a atribuição de política que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="61fcf-128">Specifies the fully qualified resource ID for the policy assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="61fcf-129">-IncludeDescendent</span><span class="sxs-lookup"><span data-stu-id="61fcf-129">-IncludeDescendent</span></span>
<span data-ttu-id="61fcf-130">Faz com que a lista de atribuições de política retornadas inclua todas as atribuições relacionadas ao escopo fornecido, incluindo as de escopos ancestrais e as de escopos descendentes.</span><span class="sxs-lookup"><span data-stu-id="61fcf-130">Causes the list of returned policy assignments to include all assignments related to the given scope, including those from ancestor scopes and those from descendent scopes.</span></span>

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

### <span data-ttu-id="61fcf-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="61fcf-131">-Name</span></span>
<span data-ttu-id="61fcf-132">Especifica o nome da atribuição de política que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="61fcf-132">Specifies the name of the policy assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="61fcf-133">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="61fcf-133">-PolicyDefinitionId</span></span>
<span data-ttu-id="61fcf-134">Especifica a ID da definição de política das atribuições de política que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="61fcf-134">Specifies the ID of the policy definition of the policy assignments that this cmdlet gets.</span></span>

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

### <span data-ttu-id="61fcf-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="61fcf-135">-Pre</span></span>
<span data-ttu-id="61fcf-136">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="61fcf-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="61fcf-137">-Escopo</span><span class="sxs-lookup"><span data-stu-id="61fcf-137">-Scope</span></span>
<span data-ttu-id="61fcf-138">Especifica o escopo no qual a política é aplicada para a atribuição que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="61fcf-138">Specifies the scope at which the policy is applied for the assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="61fcf-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61fcf-139">CommonParameters</span></span>
<span data-ttu-id="61fcf-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61fcf-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61fcf-141">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="61fcf-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61fcf-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="61fcf-142">INPUTS</span></span>

### <span data-ttu-id="61fcf-143">System. String</span><span class="sxs-lookup"><span data-stu-id="61fcf-143">System.String</span></span>

### <span data-ttu-id="61fcf-144">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="61fcf-144">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="61fcf-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="61fcf-145">OUTPUTS</span></span>

### <span data-ttu-id="61fcf-146">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="61fcf-146">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="61fcf-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="61fcf-147">NOTES</span></span>

## <span data-ttu-id="61fcf-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="61fcf-148">RELATED LINKS</span></span>

[<span data-ttu-id="61fcf-149">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="61fcf-149">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="61fcf-150">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="61fcf-150">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)

[<span data-ttu-id="61fcf-151">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="61fcf-151">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)

