---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2DBAF415-A039-479E-B3CA-E00FD5E476C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzPolicyAssignment.md
ms.openlocfilehash: 160cff39918691c310de6931cd57cb415774d7e6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776442"
---
# <span data-ttu-id="4f312-101">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="4f312-101">Get-AzPolicyAssignment</span></span>

## <span data-ttu-id="4f312-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4f312-102">SYNOPSIS</span></span>
<span data-ttu-id="4f312-103">Obtém atribuições de política.</span><span class="sxs-lookup"><span data-stu-id="4f312-103">Gets policy assignments.</span></span>

## <span data-ttu-id="4f312-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4f312-104">SYNTAX</span></span>

### <span data-ttu-id="4f312-105">DefaultParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="4f312-105">DefaultParameterSet (Default)</span></span>
```
Get-AzPolicyAssignment [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="4f312-106">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f312-106">NameParameterSet</span></span>
```
Get-AzPolicyAssignment [-Name <String>] [-Scope <String>] [-PolicyDefinitionId <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="4f312-107">IncludeDescendentParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f312-107">IncludeDescendentParameterSet</span></span>
```
Get-AzPolicyAssignment [-Scope <String>] [-IncludeDescendent] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="4f312-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f312-108">IdParameterSet</span></span>
```
Get-AzPolicyAssignment -Id <String> [-PolicyDefinitionId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="4f312-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4f312-109">DESCRIPTION</span></span>
<span data-ttu-id="4f312-110">O cmdlet **Get-AzPolicyAssignment** obtém todas as atribuições de política ou atribuições específicas.</span><span class="sxs-lookup"><span data-stu-id="4f312-110">The **Get-AzPolicyAssignment** cmdlet gets all policy assignments or particular assignments.</span></span>
<span data-ttu-id="4f312-111">Identifique uma atribuição de política para obter por nome e escopo ou por ID.</span><span class="sxs-lookup"><span data-stu-id="4f312-111">Identify a policy assignment to get by name and scope or by ID.</span></span>

## <span data-ttu-id="4f312-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4f312-112">EXAMPLES</span></span>

### <span data-ttu-id="4f312-113">Exemplo 1: obter todas as atribuições de política</span><span class="sxs-lookup"><span data-stu-id="4f312-113">Example 1: Get all policy assignments</span></span>
```
PS C:\> Get-AzPolicyAssignment
```

<span data-ttu-id="4f312-114">Este comando obtém todas as atribuições de política.</span><span class="sxs-lookup"><span data-stu-id="4f312-114">This command gets all the policy assignments.</span></span>

### <span data-ttu-id="4f312-115">Exemplo 2: obter uma atribuição de política específica</span><span class="sxs-lookup"><span data-stu-id="4f312-115">Example 2: Get a specific policy assignment</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> Get-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="4f312-116">O primeiro comando obtém um grupo de recursos chamado ResourceGroup11 usando o Get-AzResourceGroup cmdletand o armazena na variável $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="4f312-116">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdletand stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="4f312-117">O segundo comando obtém a atribuição de política chamada PolicyAssignment07 para o escopo que a propriedade **ResourceId** de $ResourceGroup identifica.</span><span class="sxs-lookup"><span data-stu-id="4f312-117">The second command gets the policy assignment named PolicyAssignment07 for the scope that the **ResourceId** property of $ResourceGroup identifies.</span></span>

### <span data-ttu-id="4f312-118">Exemplo 3: obter todas as atribuições de política atribuídas a um grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="4f312-118">Example 3: Get all policy assignments assigned to a management group</span></span>
```
PS C:\> $mgId = 'myManagementGroup'
PS C:\> Get-AzPolicyAssignment -Scope '/providers/Microsoft.Management/managementgroups/$mgId'
```

<span data-ttu-id="4f312-119">O primeiro comando especifica a ID do grupo de gerenciamento a ser consultado.</span><span class="sxs-lookup"><span data-stu-id="4f312-119">The first command specifies the ID of the management group to query.</span></span>
<span data-ttu-id="4f312-120">O segundo comando obtém todas as atribuições de política atribuídas ao grupo de gerenciamento com ID ' mymanagement Group '.</span><span class="sxs-lookup"><span data-stu-id="4f312-120">The second command gets all of the policy assignments that are assigned to the management group with ID 'myManagementGroup'.</span></span>

## <span data-ttu-id="4f312-121">OS</span><span class="sxs-lookup"><span data-stu-id="4f312-121">PARAMETERS</span></span>

### <span data-ttu-id="4f312-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4f312-122">-ApiVersion</span></span>
<span data-ttu-id="4f312-123">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="4f312-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="4f312-124">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="4f312-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="4f312-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f312-125">-DefaultProfile</span></span>
<span data-ttu-id="4f312-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="4f312-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f312-127">-ID</span><span class="sxs-lookup"><span data-stu-id="4f312-127">-Id</span></span>
<span data-ttu-id="4f312-128">Especifica a ID de recurso totalmente qualificado para a atribuição de política que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="4f312-128">Specifies the fully qualified resource ID for the policy assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="4f312-129">-IncludeDescendent</span><span class="sxs-lookup"><span data-stu-id="4f312-129">-IncludeDescendent</span></span>
<span data-ttu-id="4f312-130">Faz com que a lista de atribuições de política retornadas inclua todas as atribuições relacionadas ao escopo fornecido, incluindo as de escopos ancestrais e as de escopos descendentes.</span><span class="sxs-lookup"><span data-stu-id="4f312-130">Causes the list of returned policy assignments to include all assignments related to the given scope, including those from ancestor scopes and those from descendent scopes.</span></span>

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

### <span data-ttu-id="4f312-131">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="4f312-131">-InformationAction</span></span>
<span data-ttu-id="4f312-132">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="4f312-132">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="4f312-133">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="4f312-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4f312-134">Contínuo</span><span class="sxs-lookup"><span data-stu-id="4f312-134">Continue</span></span>
- <span data-ttu-id="4f312-135">Ignorar</span><span class="sxs-lookup"><span data-stu-id="4f312-135">Ignore</span></span>
- <span data-ttu-id="4f312-136">Inquire</span><span class="sxs-lookup"><span data-stu-id="4f312-136">Inquire</span></span>
- <span data-ttu-id="4f312-137">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="4f312-137">SilentlyContinue</span></span>
- <span data-ttu-id="4f312-138">Finaliza</span><span class="sxs-lookup"><span data-stu-id="4f312-138">Stop</span></span>
- <span data-ttu-id="4f312-139">Suspensão</span><span class="sxs-lookup"><span data-stu-id="4f312-139">Suspend</span></span>

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

### <span data-ttu-id="4f312-140">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="4f312-140">-InformationVariable</span></span>
<span data-ttu-id="4f312-141">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="4f312-141">Specifies an information variable.</span></span>

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

### <span data-ttu-id="4f312-142">-Nome</span><span class="sxs-lookup"><span data-stu-id="4f312-142">-Name</span></span>
<span data-ttu-id="4f312-143">Especifica o nome da atribuição de política que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="4f312-143">Specifies the name of the policy assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="4f312-144">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="4f312-144">-PolicyDefinitionId</span></span>
<span data-ttu-id="4f312-145">Especifica a ID da definição de política das atribuições de política que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="4f312-145">Specifies the ID of the policy definition of the policy assignments that this cmdlet gets.</span></span>

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

### <span data-ttu-id="4f312-146">-Pre</span><span class="sxs-lookup"><span data-stu-id="4f312-146">-Pre</span></span>
<span data-ttu-id="4f312-147">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="4f312-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="4f312-148">-Escopo</span><span class="sxs-lookup"><span data-stu-id="4f312-148">-Scope</span></span>
<span data-ttu-id="4f312-149">Especifica o escopo no qual a política é aplicada para a atribuição que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="4f312-149">Specifies the scope at which the policy is applied for the assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="4f312-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f312-150">CommonParameters</span></span>
<span data-ttu-id="4f312-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f312-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f312-152">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f312-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f312-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4f312-153">INPUTS</span></span>

## <span data-ttu-id="4f312-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4f312-154">OUTPUTS</span></span>

## <span data-ttu-id="4f312-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4f312-155">NOTES</span></span>

## <span data-ttu-id="4f312-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4f312-156">RELATED LINKS</span></span>

[<span data-ttu-id="4f312-157">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="4f312-157">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="4f312-158">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="4f312-158">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)

[<span data-ttu-id="4f312-159">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="4f312-159">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


