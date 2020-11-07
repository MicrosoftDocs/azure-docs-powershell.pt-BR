---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2DBAF415-A039-479E-B3CA-E00FD5E476C9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermpolicyassignment
schema: 2.0.0
ms.openlocfilehash: cabd2c86ed687b90b45e60b8078d89ad0a413c87
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785866"
---
# <span data-ttu-id="e172f-101">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="e172f-101">Get-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="e172f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e172f-102">SYNOPSIS</span></span>
<span data-ttu-id="e172f-103">Obtém atribuições de política.</span><span class="sxs-lookup"><span data-stu-id="e172f-103">Gets policy assignments.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e172f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e172f-104">SYNTAX</span></span>

### <span data-ttu-id="e172f-105">DefaultParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="e172f-105">DefaultParameterSet (Default)</span></span>
```
Get-AzureRmPolicyAssignment [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="e172f-106">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e172f-106">NameParameterSet</span></span>
```
Get-AzureRmPolicyAssignment [-Name <String>] [-Scope <String>] [-PolicyDefinitionId <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="e172f-107">IncludeDescendentParameterSet</span><span class="sxs-lookup"><span data-stu-id="e172f-107">IncludeDescendentParameterSet</span></span>
```
Get-AzureRmPolicyAssignment [-Scope <String>] [-IncludeDescendent] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="e172f-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e172f-108">IdParameterSet</span></span>
```
Get-AzureRmPolicyAssignment -Id <String> [-PolicyDefinitionId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="e172f-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e172f-109">DESCRIPTION</span></span>
<span data-ttu-id="e172f-110">O cmdlet **Get-AzureRmPolicyAssignment** obtém todas as atribuições de política ou atribuições específicas.</span><span class="sxs-lookup"><span data-stu-id="e172f-110">The **Get-AzureRmPolicyAssignment** cmdlet gets all policy assignments or particular assignments.</span></span>
<span data-ttu-id="e172f-111">Identifique uma atribuição de política para obter por nome e escopo ou por ID.</span><span class="sxs-lookup"><span data-stu-id="e172f-111">Identify a policy assignment to get by name and scope or by ID.</span></span>

## <span data-ttu-id="e172f-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e172f-112">EXAMPLES</span></span>

### <span data-ttu-id="e172f-113">Exemplo 1: obter todas as atribuições de política</span><span class="sxs-lookup"><span data-stu-id="e172f-113">Example 1: Get all policy assignments</span></span>
```
PS C:\> Get-AzureRmPolicyAssignment
```

<span data-ttu-id="e172f-114">Este comando obtém todas as atribuições de política.</span><span class="sxs-lookup"><span data-stu-id="e172f-114">This command gets all the policy assignments.</span></span>

### <span data-ttu-id="e172f-115">Exemplo 2: obter uma atribuição de política específica</span><span class="sxs-lookup"><span data-stu-id="e172f-115">Example 2: Get a specific policy assignment</span></span>
```
PS C:\> $ResourceGroup = Get-AzureRmResourceGroup -Name 'ResourceGroup11'
PS C:\> Get-AzureRmPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="e172f-116">O primeiro comando obtém um grupo de recursos chamado ResourceGroup11 usando o Get-AzureRMResourceGroup cmdletand o armazena na variável $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="e172f-116">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdletand stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="e172f-117">O segundo comando obtém a atribuição de política chamada PolicyAssignment07 para o escopo que a propriedade **ResourceId** de $ResourceGroup identifica.</span><span class="sxs-lookup"><span data-stu-id="e172f-117">The second command gets the policy assignment named PolicyAssignment07 for the scope that the **ResourceId** property of $ResourceGroup identifies.</span></span>

### <span data-ttu-id="e172f-118">Exemplo 3: obter todas as atribuições de política atribuídas a um grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="e172f-118">Example 3: Get all policy assignments assigned to a management group</span></span>
```
PS C:\> $mgId = 'myManagementGroup'
PS C:\> Get-AzureRmPolicyAssignment -Scope '/providers/Microsoft.Management/managementgroups/$mgId'
```

<span data-ttu-id="e172f-119">O primeiro comando especifica a ID do grupo de gerenciamento a ser consultado.</span><span class="sxs-lookup"><span data-stu-id="e172f-119">The first command specifies the ID of the management group to query.</span></span>
<span data-ttu-id="e172f-120">O segundo comando obtém todas as atribuições de política atribuídas ao grupo de gerenciamento com ID ' mymanagement Group '.</span><span class="sxs-lookup"><span data-stu-id="e172f-120">The second command gets all of the policy assignments that are assigned to the management group with ID 'myManagementGroup'.</span></span>

## <span data-ttu-id="e172f-121">OS</span><span class="sxs-lookup"><span data-stu-id="e172f-121">PARAMETERS</span></span>

### <span data-ttu-id="e172f-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e172f-122">-ApiVersion</span></span>
<span data-ttu-id="e172f-123">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="e172f-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="e172f-124">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="e172f-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="e172f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e172f-125">-DefaultProfile</span></span>
<span data-ttu-id="e172f-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="e172f-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e172f-127">-ID</span><span class="sxs-lookup"><span data-stu-id="e172f-127">-Id</span></span>
<span data-ttu-id="e172f-128">Especifica a ID de recurso totalmente qualificado para a atribuição de política que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="e172f-128">Specifies the fully qualified resource ID for the policy assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e172f-129">-IncludeDescendent</span><span class="sxs-lookup"><span data-stu-id="e172f-129">-IncludeDescendent</span></span>
<span data-ttu-id="e172f-130">Faz com que a lista de atribuições de política retornadas inclua todas as atribuições relacionadas ao escopo fornecido, incluindo as de escopos ancestrais e as de escopos descendentes.</span><span class="sxs-lookup"><span data-stu-id="e172f-130">Causes the list of returned policy assignments to include all assignments related to the given scope, including those from ancestor scopes and those from descendent scopes.</span></span>

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

### <span data-ttu-id="e172f-131">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="e172f-131">-InformationAction</span></span>
<span data-ttu-id="e172f-132">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="e172f-132">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="e172f-133">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="e172f-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e172f-134">Contínuo</span><span class="sxs-lookup"><span data-stu-id="e172f-134">Continue</span></span>
- <span data-ttu-id="e172f-135">Ignorar</span><span class="sxs-lookup"><span data-stu-id="e172f-135">Ignore</span></span>
- <span data-ttu-id="e172f-136">Inquire</span><span class="sxs-lookup"><span data-stu-id="e172f-136">Inquire</span></span>
- <span data-ttu-id="e172f-137">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e172f-137">SilentlyContinue</span></span>
- <span data-ttu-id="e172f-138">Finaliza</span><span class="sxs-lookup"><span data-stu-id="e172f-138">Stop</span></span>
- <span data-ttu-id="e172f-139">Suspensão</span><span class="sxs-lookup"><span data-stu-id="e172f-139">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e172f-140">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e172f-140">-InformationVariable</span></span>
<span data-ttu-id="e172f-141">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="e172f-141">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e172f-142">-Nome</span><span class="sxs-lookup"><span data-stu-id="e172f-142">-Name</span></span>
<span data-ttu-id="e172f-143">Especifica o nome da atribuição de política que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="e172f-143">Specifies the name of the policy assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e172f-144">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="e172f-144">-PolicyDefinitionId</span></span>
<span data-ttu-id="e172f-145">Especifica a ID da definição de política das atribuições de política que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="e172f-145">Specifies the ID of the policy definition of the policy assignments that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e172f-146">-Pre</span><span class="sxs-lookup"><span data-stu-id="e172f-146">-Pre</span></span>
<span data-ttu-id="e172f-147">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="e172f-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e172f-148">-Escopo</span><span class="sxs-lookup"><span data-stu-id="e172f-148">-Scope</span></span>
<span data-ttu-id="e172f-149">Especifica o escopo no qual a política é aplicada para a atribuição que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="e172f-149">Specifies the scope at which the policy is applied for the assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e172f-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e172f-150">CommonParameters</span></span>
<span data-ttu-id="e172f-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e172f-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e172f-152">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e172f-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e172f-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e172f-153">INPUTS</span></span>

## <span data-ttu-id="e172f-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e172f-154">OUTPUTS</span></span>

## <span data-ttu-id="e172f-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e172f-155">NOTES</span></span>

## <span data-ttu-id="e172f-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e172f-156">RELATED LINKS</span></span>

[<span data-ttu-id="e172f-157">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="e172f-157">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="e172f-158">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="e172f-158">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)

[<span data-ttu-id="e172f-159">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="e172f-159">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


