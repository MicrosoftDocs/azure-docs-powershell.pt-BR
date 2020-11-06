---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyAssignment.md
ms.openlocfilehash: 97be8f9eef611a87dae045df680d2823dc2f7acb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433429"
---
# <span data-ttu-id="6f7e8-101">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="6f7e8-101">Set-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="6f7e8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6f7e8-102">SYNOPSIS</span></span>
<span data-ttu-id="6f7e8-103">Modifica uma atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="6f7e8-103">Modifies a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f7e8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6f7e8-104">SYNTAX</span></span>

### <span data-ttu-id="6f7e8-105">SetByPolicyAssignmentName (padrão)</span><span class="sxs-lookup"><span data-stu-id="6f7e8-105">SetByPolicyAssignmentName (Default)</span></span>
```
Set-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="6f7e8-106">SetByPolicyAssignmentId</span><span class="sxs-lookup"><span data-stu-id="6f7e8-106">SetByPolicyAssignmentId</span></span>
```
Set-AzureRmPolicyAssignment -Id <String> [-DisplayName <String>] [-Description <String>] [-Sku <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="6f7e8-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6f7e8-107">DESCRIPTION</span></span>
<span data-ttu-id="6f7e8-108">O cmdlet **set-AzureRmPolicyAssignment** modifica uma atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="6f7e8-108">The **Set-AzureRmPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="6f7e8-109">Especifique uma atribuição por ID ou por nome e escopo.</span><span class="sxs-lookup"><span data-stu-id="6f7e8-109">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="6f7e8-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6f7e8-110">EXAMPLES</span></span>

### <span data-ttu-id="6f7e8-111">Exemplo 1: atualizar o nome para exibição</span><span class="sxs-lookup"><span data-stu-id="6f7e8-111">Example 1: Update the display name</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> $PolicyAssignment = Get-AzureRmPolicyAssignment -Name "PolicyAssignment" -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzureRmPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName "Do not allow VM creation"
```

<span data-ttu-id="6f7e8-112">O primeiro comando obtém um grupo de recursos chamado ResourceGroup11 usando o cmdlet Get-AzureRMResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="6f7e8-112">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="6f7e8-113">O comando armazena esse objeto na variável $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="6f7e8-113">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="6f7e8-114">O segundo comando obtém a atribuição de política chamada PolicyAssignment usando o cmdlet Get-AzureRmPolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="6f7e8-114">The second command gets the policy assignment named PolicyAssignment by using the Get-AzureRmPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="6f7e8-115">O comando armazena esse objeto na variável $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="6f7e8-115">The command stores that object in the $PolicyAssignment variable.</span></span>

<span data-ttu-id="6f7e8-116">O comando final atualiza o nome de exibição na atribuição de política identificada pela propriedade **ResourceId** de $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="6f7e8-116">The final command updates the display name on the policy assignment identified by the **ResourceId** property of $PolicyAssignment.</span></span>

## <span data-ttu-id="6f7e8-117">OS</span><span class="sxs-lookup"><span data-stu-id="6f7e8-117">PARAMETERS</span></span>

### <span data-ttu-id="6f7e8-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6f7e8-118">-ApiVersion</span></span>
<span data-ttu-id="6f7e8-119">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="6f7e8-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="6f7e8-120">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="6f7e8-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="6f7e8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f7e8-121">-DefaultProfile</span></span>
<span data-ttu-id="6f7e8-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="6f7e8-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6f7e8-123">-Descrição</span><span class="sxs-lookup"><span data-stu-id="6f7e8-123">-Description</span></span>
<span data-ttu-id="6f7e8-124">A descrição da atribuição de política</span><span class="sxs-lookup"><span data-stu-id="6f7e8-124">The description for policy assignment</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f7e8-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="6f7e8-125">-DisplayName</span></span>
<span data-ttu-id="6f7e8-126">Especifica um novo nome de exibição para a atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="6f7e8-126">Specifies a new display name for the policy assignment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f7e8-127">-ID</span><span class="sxs-lookup"><span data-stu-id="6f7e8-127">-Id</span></span>
<span data-ttu-id="6f7e8-128">Especifica a ID de recurso totalmente qualificado para a atribuição de política que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="6f7e8-128">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: SetByPolicyAssignmentId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f7e8-129">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="6f7e8-129">-InformationAction</span></span>
<span data-ttu-id="6f7e8-130">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="6f7e8-130">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6f7e8-131">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="6f7e8-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6f7e8-132">Contínuo</span><span class="sxs-lookup"><span data-stu-id="6f7e8-132">Continue</span></span>
- <span data-ttu-id="6f7e8-133">Ignorar</span><span class="sxs-lookup"><span data-stu-id="6f7e8-133">Ignore</span></span>
- <span data-ttu-id="6f7e8-134">Inquire</span><span class="sxs-lookup"><span data-stu-id="6f7e8-134">Inquire</span></span>
- <span data-ttu-id="6f7e8-135">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6f7e8-135">SilentlyContinue</span></span>
- <span data-ttu-id="6f7e8-136">Finaliza</span><span class="sxs-lookup"><span data-stu-id="6f7e8-136">Stop</span></span>
- <span data-ttu-id="6f7e8-137">Suspensão</span><span class="sxs-lookup"><span data-stu-id="6f7e8-137">Suspend</span></span>

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

### <span data-ttu-id="6f7e8-138">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6f7e8-138">-InformationVariable</span></span>
<span data-ttu-id="6f7e8-139">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="6f7e8-139">Specifies an information variable.</span></span>

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

### <span data-ttu-id="6f7e8-140">-Nome</span><span class="sxs-lookup"><span data-stu-id="6f7e8-140">-Name</span></span>
<span data-ttu-id="6f7e8-141">Especifica o nome da atribuição de política que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="6f7e8-141">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: SetByPolicyAssignmentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f7e8-142">-Não-escopo</span><span class="sxs-lookup"><span data-stu-id="6f7e8-142">-NotScope</span></span>
<span data-ttu-id="6f7e8-143">A atribuição de política não é de escopos.</span><span class="sxs-lookup"><span data-stu-id="6f7e8-143">The policy assignment not scopes.</span></span>

```yaml
Type: String[]
Parameter Sets: SetByPolicyAssignmentName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f7e8-144">-Pre</span><span class="sxs-lookup"><span data-stu-id="6f7e8-144">-Pre</span></span>
<span data-ttu-id="6f7e8-145">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="6f7e8-145">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="6f7e8-146">-Escopo</span><span class="sxs-lookup"><span data-stu-id="6f7e8-146">-Scope</span></span>
<span data-ttu-id="6f7e8-147">Especifica o escopo no qual a política é aplicada.</span><span class="sxs-lookup"><span data-stu-id="6f7e8-147">Specifies the scope at which the policy is applied.</span></span>

```yaml
Type: String
Parameter Sets: SetByPolicyAssignmentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f7e8-148">-SKU</span><span class="sxs-lookup"><span data-stu-id="6f7e8-148">-Sku</span></span>
<span data-ttu-id="6f7e8-149">Uma tabela de hash que representa as propriedades de SKU.</span><span class="sxs-lookup"><span data-stu-id="6f7e8-149">A hash table which represents sku properties.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f7e8-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f7e8-150">CommonParameters</span></span>
<span data-ttu-id="6f7e8-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f7e8-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f7e8-152">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f7e8-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f7e8-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6f7e8-153">INPUTS</span></span>

### <span data-ttu-id="6f7e8-154">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="6f7e8-154">None</span></span>
<span data-ttu-id="6f7e8-155">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="6f7e8-155">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6f7e8-156">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6f7e8-156">OUTPUTS</span></span>

### <span data-ttu-id="6f7e8-157">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="6f7e8-157">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="6f7e8-158">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6f7e8-158">NOTES</span></span>

## <span data-ttu-id="6f7e8-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6f7e8-159">RELATED LINKS</span></span>

[<span data-ttu-id="6f7e8-160">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="6f7e8-160">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="6f7e8-161">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="6f7e8-161">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="6f7e8-162">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="6f7e8-162">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)


