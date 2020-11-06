---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2DBAF415-A039-479E-B3CA-E00FD5E476C9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyAssignment.md
ms.openlocfilehash: 0604c7bd8f4f016f908eb7e9c93ff6b9d95db979
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609494"
---
# <span data-ttu-id="76a0e-101">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="76a0e-101">Get-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="76a0e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="76a0e-102">SYNOPSIS</span></span>
<span data-ttu-id="76a0e-103">Obtém atribuições de política.</span><span class="sxs-lookup"><span data-stu-id="76a0e-103">Gets policy assignments.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76a0e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="76a0e-104">SYNTAX</span></span>

### <span data-ttu-id="76a0e-105">GetAllPolicyAssignments (padrão)</span><span class="sxs-lookup"><span data-stu-id="76a0e-105">GetAllPolicyAssignments (Default)</span></span>
```
Get-AzureRmPolicyAssignment [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="76a0e-106">GetPolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="76a0e-106">GetPolicyAssignmentName</span></span>
```
Get-AzureRmPolicyAssignment [-Name <String>] -Scope <String> [-PolicyDefinitionId <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="76a0e-107">GetPolicyAssignmentId</span><span class="sxs-lookup"><span data-stu-id="76a0e-107">GetPolicyAssignmentId</span></span>
```
Get-AzureRmPolicyAssignment -Id <String> [-PolicyDefinitionId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="76a0e-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="76a0e-108">DESCRIPTION</span></span>
<span data-ttu-id="76a0e-109">O cmdlet **Get-AzureRmPolicyAssignment** obtém todas as atribuições de política ou atribuições específicas.</span><span class="sxs-lookup"><span data-stu-id="76a0e-109">The **Get-AzureRmPolicyAssignment** cmdlet gets all policy assignments or particular assignments.</span></span>
<span data-ttu-id="76a0e-110">Identifique uma atribuição de política para obter por nome e escopo ou por ID.</span><span class="sxs-lookup"><span data-stu-id="76a0e-110">Identify a policy assignment to get by name and scope or by ID.</span></span>

## <span data-ttu-id="76a0e-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="76a0e-111">EXAMPLES</span></span>

### <span data-ttu-id="76a0e-112">Exemplo 1: obter todas as atribuições de política</span><span class="sxs-lookup"><span data-stu-id="76a0e-112">Example 1: Get all policy assignments</span></span>
```
PS C:\>Get-AzureRmPolicyAssignment
```

<span data-ttu-id="76a0e-113">Este comando obtém todas as atribuições de política.</span><span class="sxs-lookup"><span data-stu-id="76a0e-113">This command gets all the policy assignments.</span></span>

### <span data-ttu-id="76a0e-114">Exemplo 2: obter uma atribuição de política específica</span><span class="sxs-lookup"><span data-stu-id="76a0e-114">Example 2: Get a specific policy assignment</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> Get-AzureRmPolicyAssignment -Name "PolicyAssignment07" -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="76a0e-115">O primeiro comando obtém um grupo de recursos chamado ResourceGroup11 usando o cmdlet Get-AzureRMResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="76a0e-115">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="76a0e-116">O comando armazena esse objeto na variável $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="76a0e-116">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="76a0e-117">O segundo comando obtém a atribuição de política chamada PolicyAssignment07 para o escopo que a propriedade **ResourceId** de $ResourceGroup identifica.</span><span class="sxs-lookup"><span data-stu-id="76a0e-117">The second command get the policy assignment named PolicyAssignment07 for the scope that the **ResourceId** property of $ResourceGroup identifies.</span></span>

## <span data-ttu-id="76a0e-118">OS</span><span class="sxs-lookup"><span data-stu-id="76a0e-118">PARAMETERS</span></span>

### <span data-ttu-id="76a0e-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="76a0e-119">-ApiVersion</span></span>
<span data-ttu-id="76a0e-120">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="76a0e-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="76a0e-121">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="76a0e-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76a0e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76a0e-122">-DefaultProfile</span></span>
<span data-ttu-id="76a0e-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="76a0e-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76a0e-124">-ID</span><span class="sxs-lookup"><span data-stu-id="76a0e-124">-Id</span></span>
<span data-ttu-id="76a0e-125">Especifica a ID de recurso totalmente qualificado para a atribuição de política que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="76a0e-125">Specifies the fully qualified resource ID for the policy assignment that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: GetPolicyAssignmentId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76a0e-126">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="76a0e-126">-InformationAction</span></span>
<span data-ttu-id="76a0e-127">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="76a0e-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="76a0e-128">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="76a0e-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="76a0e-129">Contínuo</span><span class="sxs-lookup"><span data-stu-id="76a0e-129">Continue</span></span>
- <span data-ttu-id="76a0e-130">Ignorar</span><span class="sxs-lookup"><span data-stu-id="76a0e-130">Ignore</span></span>
- <span data-ttu-id="76a0e-131">Inquire</span><span class="sxs-lookup"><span data-stu-id="76a0e-131">Inquire</span></span>
- <span data-ttu-id="76a0e-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="76a0e-132">SilentlyContinue</span></span>
- <span data-ttu-id="76a0e-133">Finaliza</span><span class="sxs-lookup"><span data-stu-id="76a0e-133">Stop</span></span>
- <span data-ttu-id="76a0e-134">Suspensão</span><span class="sxs-lookup"><span data-stu-id="76a0e-134">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76a0e-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="76a0e-135">-InformationVariable</span></span>
<span data-ttu-id="76a0e-136">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="76a0e-136">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76a0e-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="76a0e-137">-Name</span></span>
<span data-ttu-id="76a0e-138">Especifica o nome da atribuição de política que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="76a0e-138">Specifies the name of the policy assignment that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: GetPolicyAssignmentName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76a0e-139">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="76a0e-139">-PolicyDefinitionId</span></span>
<span data-ttu-id="76a0e-140">Especifica a ID da definição de política das atribuições de política que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="76a0e-140">Specifies the ID of the policy definition of the policy assignments that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: GetPolicyAssignmentName, GetPolicyAssignmentId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76a0e-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="76a0e-141">-Pre</span></span>
<span data-ttu-id="76a0e-142">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="76a0e-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76a0e-143">-Escopo</span><span class="sxs-lookup"><span data-stu-id="76a0e-143">-Scope</span></span>
<span data-ttu-id="76a0e-144">Especifica o escopo no qual a política é aplicada para a atribuição que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="76a0e-144">Specifies the scope at which the policy is applied for the assignment that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: GetPolicyAssignmentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76a0e-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76a0e-145">CommonParameters</span></span>
<span data-ttu-id="76a0e-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76a0e-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76a0e-147">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76a0e-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76a0e-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="76a0e-148">INPUTS</span></span>

### <span data-ttu-id="76a0e-149">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="76a0e-149">None</span></span>
<span data-ttu-id="76a0e-150">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="76a0e-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="76a0e-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="76a0e-151">OUTPUTS</span></span>

### <span data-ttu-id="76a0e-152">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="76a0e-152">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="76a0e-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="76a0e-153">NOTES</span></span>

## <span data-ttu-id="76a0e-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="76a0e-154">RELATED LINKS</span></span>

[<span data-ttu-id="76a0e-155">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="76a0e-155">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="76a0e-156">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="76a0e-156">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)

[<span data-ttu-id="76a0e-157">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="76a0e-157">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


