---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyAssignment.md
ms.openlocfilehash: fcb1283531b35365cc8c07016c839a1152011160
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429119"
---
# <span data-ttu-id="8c65e-101">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="8c65e-101">Set-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="8c65e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8c65e-102">SYNOPSIS</span></span>
<span data-ttu-id="8c65e-103">Modifica uma atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="8c65e-103">Modifies a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c65e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8c65e-104">SYNTAX</span></span>

### <span data-ttu-id="8c65e-105">O conjunto de parâmetros de nome da atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="8c65e-105">The policy assignment name parameter set.</span></span> <span data-ttu-id="8c65e-106">Assume</span><span class="sxs-lookup"><span data-stu-id="8c65e-106">(Default)</span></span>
```
Set-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="8c65e-107">O conjunto de parâmetros de ID da atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="8c65e-107">The policy assignment Id parameter set.</span></span>
```
Set-AzureRmPolicyAssignment -Id <String> [-DisplayName <String>] [-Description <String>] [-Sku <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="8c65e-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8c65e-108">DESCRIPTION</span></span>
<span data-ttu-id="8c65e-109">O cmdlet **set-AzureRmPolicyAssignment** modifica uma atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="8c65e-109">The **Set-AzureRmPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="8c65e-110">Especifique uma atribuição por ID ou por nome e escopo.</span><span class="sxs-lookup"><span data-stu-id="8c65e-110">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="8c65e-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8c65e-111">EXAMPLES</span></span>

### <span data-ttu-id="8c65e-112">Exemplo 1: atualizar o nome para exibição</span><span class="sxs-lookup"><span data-stu-id="8c65e-112">Example 1: Update the display name</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> $PolicyAssignment = Get-AzureRmPolicyAssignment -Name "PolicyAssignment" -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzureRmPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName "Do not allow VM creation"
```

<span data-ttu-id="8c65e-113">O primeiro comando obtém um grupo de recursos chamado ResourceGroup11 usando o cmdlet Get-AzureRMResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8c65e-113">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="8c65e-114">O comando armazena esse objeto na variável $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8c65e-114">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="8c65e-115">O segundo comando obtém a atribuição de política chamada PolicyAssignment usando o cmdlet Get-AzureRmPolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="8c65e-115">The second command gets the policy assignment named PolicyAssignment by using the Get-AzureRmPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="8c65e-116">O comando armazena esse objeto na variável $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="8c65e-116">The command stores that object in the $PolicyAssignment variable.</span></span>

<span data-ttu-id="8c65e-117">O comando final atualiza o nome de exibição na atribuição de política identificada pela propriedade **ResourceId** de $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="8c65e-117">The final command updates the display name on the policy assignment identified by the **ResourceId** property of $PolicyAssignment.</span></span>

## <span data-ttu-id="8c65e-118">OS</span><span class="sxs-lookup"><span data-stu-id="8c65e-118">PARAMETERS</span></span>

### <span data-ttu-id="8c65e-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8c65e-119">-ApiVersion</span></span>
<span data-ttu-id="8c65e-120">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="8c65e-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="8c65e-121">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="8c65e-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="8c65e-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8c65e-122">-DisplayName</span></span>
<span data-ttu-id="8c65e-123">Especifica um novo nome de exibição para a atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="8c65e-123">Specifies a new display name for the policy assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c65e-124">-ID</span><span class="sxs-lookup"><span data-stu-id="8c65e-124">-Id</span></span>
<span data-ttu-id="8c65e-125">Especifica a ID de recurso totalmente qualificado para a atribuição de política que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="8c65e-125">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="8c65e-126">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="8c65e-126">-InformationAction</span></span>
<span data-ttu-id="8c65e-127">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="8c65e-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="8c65e-128">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="8c65e-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8c65e-129">Contínuo</span><span class="sxs-lookup"><span data-stu-id="8c65e-129">Continue</span></span>
- <span data-ttu-id="8c65e-130">Ignorar</span><span class="sxs-lookup"><span data-stu-id="8c65e-130">Ignore</span></span>
- <span data-ttu-id="8c65e-131">Inquire</span><span class="sxs-lookup"><span data-stu-id="8c65e-131">Inquire</span></span>
- <span data-ttu-id="8c65e-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8c65e-132">SilentlyContinue</span></span>
- <span data-ttu-id="8c65e-133">Finaliza</span><span class="sxs-lookup"><span data-stu-id="8c65e-133">Stop</span></span>
- <span data-ttu-id="8c65e-134">Suspensão</span><span class="sxs-lookup"><span data-stu-id="8c65e-134">Suspend</span></span>

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

### <span data-ttu-id="8c65e-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8c65e-135">-InformationVariable</span></span>
<span data-ttu-id="8c65e-136">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="8c65e-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="8c65e-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="8c65e-137">-Name</span></span>
<span data-ttu-id="8c65e-138">Especifica o nome da atribuição de política que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="8c65e-138">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="8c65e-139">-Não-escopo</span><span class="sxs-lookup"><span data-stu-id="8c65e-139">-NotScope</span></span>
<span data-ttu-id="8c65e-140">A atribuição de política não é de escopos.</span><span class="sxs-lookup"><span data-stu-id="8c65e-140">The policy assignment not scopes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: The policy assignment name parameter set.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c65e-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="8c65e-141">-Pre</span></span>
<span data-ttu-id="8c65e-142">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="8c65e-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="8c65e-143">-Escopo</span><span class="sxs-lookup"><span data-stu-id="8c65e-143">-Scope</span></span>
<span data-ttu-id="8c65e-144">Especifica o escopo no qual a política é aplicada.</span><span class="sxs-lookup"><span data-stu-id="8c65e-144">Specifies the scope at which the policy is applied.</span></span>

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

### <span data-ttu-id="8c65e-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c65e-145">-DefaultProfile</span></span>
<span data-ttu-id="8c65e-146">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8c65e-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c65e-147">-Descrição</span><span class="sxs-lookup"><span data-stu-id="8c65e-147">-Description</span></span>
<span data-ttu-id="8c65e-148">A descrição da atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="8c65e-148">The description for policy assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c65e-149">-SKU</span><span class="sxs-lookup"><span data-stu-id="8c65e-149">-Sku</span></span>
<span data-ttu-id="8c65e-150">Uma tabela de hash que representa as propriedades de SKU.</span><span class="sxs-lookup"><span data-stu-id="8c65e-150">A hash table which represents sku properties.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c65e-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c65e-151">CommonParameters</span></span>
<span data-ttu-id="8c65e-152">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c65e-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c65e-153">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c65e-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c65e-154">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8c65e-154">INPUTS</span></span>

## <span data-ttu-id="8c65e-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8c65e-155">OUTPUTS</span></span>

### <span data-ttu-id="8c65e-156">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="8c65e-156">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="8c65e-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8c65e-157">NOTES</span></span>

## <span data-ttu-id="8c65e-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8c65e-158">RELATED LINKS</span></span>

[<span data-ttu-id="8c65e-159">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="8c65e-159">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="8c65e-160">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="8c65e-160">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="8c65e-161">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="8c65e-161">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)


