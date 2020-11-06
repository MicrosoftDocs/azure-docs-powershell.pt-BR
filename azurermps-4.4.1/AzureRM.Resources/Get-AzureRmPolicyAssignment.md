---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2DBAF415-A039-479E-B3CA-E00FD5E476C9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyAssignment.md
ms.openlocfilehash: 11a28cb8848c197d9d766b05833e8c0ca3106412
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429121"
---
# <span data-ttu-id="6a2da-101">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="6a2da-101">Get-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="6a2da-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6a2da-102">SYNOPSIS</span></span>
<span data-ttu-id="6a2da-103">Obtém atribuições de política.</span><span class="sxs-lookup"><span data-stu-id="6a2da-103">Gets policy assignments.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a2da-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6a2da-104">SYNTAX</span></span>

### <span data-ttu-id="6a2da-105">O conjunto de parâmetros da lista todas as atribuições de política.</span><span class="sxs-lookup"><span data-stu-id="6a2da-105">The list all policy assignments parameter set.</span></span> <span data-ttu-id="6a2da-106">Assume</span><span class="sxs-lookup"><span data-stu-id="6a2da-106">(Default)</span></span>
```
Get-AzureRmPolicyAssignment [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="6a2da-107">O conjunto de parâmetros de nome da atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="6a2da-107">The policy assignment name parameter set.</span></span>
```
Get-AzureRmPolicyAssignment [-Name <String>] -Scope <String> [-PolicyDefinitionId <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="6a2da-108">O conjunto de parâmetros de ID da atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="6a2da-108">The policy assignment Id parameter set.</span></span>
```
Get-AzureRmPolicyAssignment -Id <String> [-PolicyDefinitionId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="6a2da-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6a2da-109">DESCRIPTION</span></span>
<span data-ttu-id="6a2da-110">O cmdlet **Get-AzureRmPolicyAssignment** obtém todas as atribuições de política ou atribuições específicas.</span><span class="sxs-lookup"><span data-stu-id="6a2da-110">The **Get-AzureRmPolicyAssignment** cmdlet gets all policy assignments or particular assignments.</span></span>
<span data-ttu-id="6a2da-111">Identifique uma atribuição de política para obter por nome e escopo ou por ID.</span><span class="sxs-lookup"><span data-stu-id="6a2da-111">Identify a policy assignment to get by name and scope or by ID.</span></span>

## <span data-ttu-id="6a2da-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6a2da-112">EXAMPLES</span></span>

### <span data-ttu-id="6a2da-113">Exemplo 1: obter todas as atribuições de política</span><span class="sxs-lookup"><span data-stu-id="6a2da-113">Example 1: Get all policy assignments</span></span>
```
PS C:\>Get-AzureRmPolicyAssignment
```

<span data-ttu-id="6a2da-114">Este comando obtém todas as atribuições de política.</span><span class="sxs-lookup"><span data-stu-id="6a2da-114">This command gets all the policy assignments.</span></span>

### <span data-ttu-id="6a2da-115">Exemplo 2: obter uma atribuição de política específica</span><span class="sxs-lookup"><span data-stu-id="6a2da-115">Example 2: Get a specific policy assignment</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> Get-AzureRmPolicyAssignment -Name "PolicyAssignment07" -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="6a2da-116">O primeiro comando obtém um grupo de recursos chamado ResourceGroup11 usando o cmdlet Get-AzureRMResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="6a2da-116">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="6a2da-117">O comando armazena esse objeto na variável $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="6a2da-117">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="6a2da-118">O segundo comando obtém a atribuição de política chamada PolicyAssignment07 para o escopo que a propriedade **ResourceId** de $ResourceGroup identifica.</span><span class="sxs-lookup"><span data-stu-id="6a2da-118">The second command get the policy assignment named PolicyAssignment07 for the scope that the **ResourceId** property of $ResourceGroup identifies.</span></span>

## <span data-ttu-id="6a2da-119">OS</span><span class="sxs-lookup"><span data-stu-id="6a2da-119">PARAMETERS</span></span>

### <span data-ttu-id="6a2da-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6a2da-120">-ApiVersion</span></span>
<span data-ttu-id="6a2da-121">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="6a2da-121">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="6a2da-122">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="6a2da-122">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="6a2da-123">-ID</span><span class="sxs-lookup"><span data-stu-id="6a2da-123">-Id</span></span>
<span data-ttu-id="6a2da-124">Especifica a ID de recurso totalmente qualificado para a atribuição de política que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="6a2da-124">Specifies the fully qualified resource ID for the policy assignment that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a2da-125">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="6a2da-125">-InformationAction</span></span>
<span data-ttu-id="6a2da-126">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="6a2da-126">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6a2da-127">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="6a2da-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6a2da-128">Contínuo</span><span class="sxs-lookup"><span data-stu-id="6a2da-128">Continue</span></span>
- <span data-ttu-id="6a2da-129">Ignorar</span><span class="sxs-lookup"><span data-stu-id="6a2da-129">Ignore</span></span>
- <span data-ttu-id="6a2da-130">Inquire</span><span class="sxs-lookup"><span data-stu-id="6a2da-130">Inquire</span></span>
- <span data-ttu-id="6a2da-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6a2da-131">SilentlyContinue</span></span>
- <span data-ttu-id="6a2da-132">Finaliza</span><span class="sxs-lookup"><span data-stu-id="6a2da-132">Stop</span></span>
- <span data-ttu-id="6a2da-133">Suspensão</span><span class="sxs-lookup"><span data-stu-id="6a2da-133">Suspend</span></span>

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

### <span data-ttu-id="6a2da-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6a2da-134">-InformationVariable</span></span>
<span data-ttu-id="6a2da-135">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="6a2da-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="6a2da-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="6a2da-136">-Name</span></span>
<span data-ttu-id="6a2da-137">Especifica o nome da atribuição de política que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="6a2da-137">Specifies the name of the policy assignment that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment name parameter set.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a2da-138">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="6a2da-138">-PolicyDefinitionId</span></span>
<span data-ttu-id="6a2da-139">Especifica a ID da definição de política das atribuições de política que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="6a2da-139">Specifies the ID of the policy definition of the policy assignments that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment name parameter set., The policy assignment Id parameter set.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a2da-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="6a2da-140">-Pre</span></span>
<span data-ttu-id="6a2da-141">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="6a2da-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="6a2da-142">-Escopo</span><span class="sxs-lookup"><span data-stu-id="6a2da-142">-Scope</span></span>
<span data-ttu-id="6a2da-143">Especifica o escopo no qual a política é aplicada para a atribuição que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="6a2da-143">Specifies the scope at which the policy is applied for the assignment that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a2da-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a2da-144">-DefaultProfile</span></span>
<span data-ttu-id="6a2da-145">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6a2da-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a2da-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a2da-146">CommonParameters</span></span>
<span data-ttu-id="6a2da-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a2da-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a2da-148">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a2da-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a2da-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6a2da-149">INPUTS</span></span>

## <span data-ttu-id="6a2da-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6a2da-150">OUTPUTS</span></span>

### <span data-ttu-id="6a2da-151">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="6a2da-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="6a2da-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6a2da-152">NOTES</span></span>

## <span data-ttu-id="6a2da-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6a2da-153">RELATED LINKS</span></span>

[<span data-ttu-id="6a2da-154">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="6a2da-154">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="6a2da-155">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="6a2da-155">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)

[<span data-ttu-id="6a2da-156">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="6a2da-156">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


