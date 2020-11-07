---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermpolicyassignment
schema: 2.0.0
ms.openlocfilehash: dc54d84886bc9c13fa6a4ecef4e41ef80fa6d4e4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785625"
---
# <span data-ttu-id="35b86-101">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="35b86-101">Set-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="35b86-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="35b86-102">SYNOPSIS</span></span>
<span data-ttu-id="35b86-103">Modifica uma atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="35b86-103">Modifies a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35b86-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="35b86-104">SYNTAX</span></span>

### <span data-ttu-id="35b86-105">NameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="35b86-105">NameParameterSet (Default)</span></span>
```
Set-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="35b86-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="35b86-106">IdParameterSet</span></span>
```
Set-AzureRmPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="35b86-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="35b86-107">DESCRIPTION</span></span>
<span data-ttu-id="35b86-108">O cmdlet **set-AzureRmPolicyAssignment** modifica uma atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="35b86-108">The **Set-AzureRmPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="35b86-109">Especifique uma atribuição por ID ou por nome e escopo.</span><span class="sxs-lookup"><span data-stu-id="35b86-109">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="35b86-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="35b86-110">EXAMPLES</span></span>

### <span data-ttu-id="35b86-111">Exemplo 1: atualizar o nome para exibição</span><span class="sxs-lookup"><span data-stu-id="35b86-111">Example 1: Update the display name</span></span>
```
PS C:\> $ResourceGroup = Get-AzureRmResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzureRmPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzureRmPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName 'Do not allow VM creation'
```

<span data-ttu-id="35b86-112">O primeiro comando obtém um grupo de recursos chamado ResourceGroup11 usando o cmdlet Get-AzureRMResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="35b86-112">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="35b86-113">O comando armazena esse objeto na variável $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="35b86-113">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="35b86-114">O segundo comando obtém a atribuição de política chamada PolicyAssignment usando o cmdlet Get-AzureRmPolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="35b86-114">The second command gets the policy assignment named PolicyAssignment by using the Get-AzureRmPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="35b86-115">O comando armazena esse objeto na variável $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="35b86-115">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="35b86-116">O comando final atualiza o nome de exibição na atribuição de política no grupo de recursos identificado pela propriedade **ResourceId** de $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="35b86-116">The final command updates the display name on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="35b86-117">Exemplo 2: adicionar uma identidade gerenciada à atribuição de política</span><span class="sxs-lookup"><span data-stu-id="35b86-117">Example 2: Add a managed identity to the policy assignment</span></span>
```
PS C:\> $PolicyAssignment = Get-AzureRmPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzureRmPolicyAssignment -Id $PolicyAssignment.ResourceId -AssignIdentity -Location 'westus'
```

<span data-ttu-id="35b86-118">O primeiro comando obtém a atribuição de política chamada PolicyAssignment da assinatura atual usando o cmdlet Get-AzureRmPolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="35b86-118">The first command gets the policy assignment named PolicyAssignment from the current subscription by using the Get-AzureRmPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="35b86-119">O comando armazena esse objeto na variável $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="35b86-119">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="35b86-120">O comando final atribui uma identidade gerenciada à atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="35b86-120">The final command assigns a managed identity to the policy assignment.</span></span>

## <span data-ttu-id="35b86-121">OS</span><span class="sxs-lookup"><span data-stu-id="35b86-121">PARAMETERS</span></span>

### <span data-ttu-id="35b86-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="35b86-122">-ApiVersion</span></span>
<span data-ttu-id="35b86-123">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="35b86-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="35b86-124">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="35b86-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="35b86-125">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="35b86-125">-AssignIdentity</span></span>
<span data-ttu-id="35b86-126">Gerar e atribuir uma identidade do Azure Active Directory para esta atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="35b86-126">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="35b86-127">A identidade será usada ao executar implantações para políticas de "deployIfNotExists".</span><span class="sxs-lookup"><span data-stu-id="35b86-127">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="35b86-128">A localização é necessária ao atribuir uma identidade.</span><span class="sxs-lookup"><span data-stu-id="35b86-128">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="35b86-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35b86-129">-DefaultProfile</span></span>
<span data-ttu-id="35b86-130">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="35b86-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="35b86-131">-Descrição</span><span class="sxs-lookup"><span data-stu-id="35b86-131">-Description</span></span>
<span data-ttu-id="35b86-132">A descrição da atribuição de política</span><span class="sxs-lookup"><span data-stu-id="35b86-132">The description for policy assignment</span></span>

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

### <span data-ttu-id="35b86-133">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="35b86-133">-DisplayName</span></span>
<span data-ttu-id="35b86-134">Especifica um novo nome de exibição para a atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="35b86-134">Specifies a new display name for the policy assignment.</span></span>

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

### <span data-ttu-id="35b86-135">-ID</span><span class="sxs-lookup"><span data-stu-id="35b86-135">-Id</span></span>
<span data-ttu-id="35b86-136">Especifica a ID de recurso totalmente qualificado para a atribuição de política que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="35b86-136">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="35b86-137">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="35b86-137">-InformationAction</span></span>
<span data-ttu-id="35b86-138">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="35b86-138">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="35b86-139">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="35b86-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="35b86-140">Contínuo</span><span class="sxs-lookup"><span data-stu-id="35b86-140">Continue</span></span>
- <span data-ttu-id="35b86-141">Ignorar</span><span class="sxs-lookup"><span data-stu-id="35b86-141">Ignore</span></span>
- <span data-ttu-id="35b86-142">Inquire</span><span class="sxs-lookup"><span data-stu-id="35b86-142">Inquire</span></span>
- <span data-ttu-id="35b86-143">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="35b86-143">SilentlyContinue</span></span>
- <span data-ttu-id="35b86-144">Finaliza</span><span class="sxs-lookup"><span data-stu-id="35b86-144">Stop</span></span>
- <span data-ttu-id="35b86-145">Suspensão</span><span class="sxs-lookup"><span data-stu-id="35b86-145">Suspend</span></span>

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

### <span data-ttu-id="35b86-146">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="35b86-146">-InformationVariable</span></span>
<span data-ttu-id="35b86-147">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="35b86-147">Specifies an information variable.</span></span>

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

### <span data-ttu-id="35b86-148">-Local</span><span class="sxs-lookup"><span data-stu-id="35b86-148">-Location</span></span>
<span data-ttu-id="35b86-149">O local da identidade do recurso da atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="35b86-149">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="35b86-150">Isso é necessário quando a opção-AssignIdentity é usada.</span><span class="sxs-lookup"><span data-stu-id="35b86-150">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="35b86-151">-Metadados</span><span class="sxs-lookup"><span data-stu-id="35b86-151">-Metadata</span></span>
<span data-ttu-id="35b86-152">Os metadados atualizados para a atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="35b86-152">The updated metadata for the policy assignment.</span></span> <span data-ttu-id="35b86-153">Isso pode ser um caminho para um nome de arquivo que contém os metadados ou os metadados como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="35b86-153">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="35b86-154">-Nome</span><span class="sxs-lookup"><span data-stu-id="35b86-154">-Name</span></span>
<span data-ttu-id="35b86-155">Especifica o nome da atribuição de política que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="35b86-155">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35b86-156">-Não-escopo</span><span class="sxs-lookup"><span data-stu-id="35b86-156">-NotScope</span></span>
<span data-ttu-id="35b86-157">A atribuição de política não é de escopos.</span><span class="sxs-lookup"><span data-stu-id="35b86-157">The policy assignment not scopes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35b86-158">-Pre</span><span class="sxs-lookup"><span data-stu-id="35b86-158">-Pre</span></span>
<span data-ttu-id="35b86-159">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="35b86-159">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="35b86-160">-Escopo</span><span class="sxs-lookup"><span data-stu-id="35b86-160">-Scope</span></span>
<span data-ttu-id="35b86-161">Especifica o escopo no qual a política é aplicada.</span><span class="sxs-lookup"><span data-stu-id="35b86-161">Specifies the scope at which the policy is applied.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35b86-162">-SKU</span><span class="sxs-lookup"><span data-stu-id="35b86-162">-Sku</span></span>
<span data-ttu-id="35b86-163">Uma tabela de hash que representa as propriedades de SKU.</span><span class="sxs-lookup"><span data-stu-id="35b86-163">A hash table which represents sku properties.</span></span>

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

### <span data-ttu-id="35b86-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35b86-164">CommonParameters</span></span>
<span data-ttu-id="35b86-165">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35b86-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35b86-166">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35b86-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35b86-167">SENSORES</span><span class="sxs-lookup"><span data-stu-id="35b86-167">INPUTS</span></span>

## <span data-ttu-id="35b86-168">EXIBE</span><span class="sxs-lookup"><span data-stu-id="35b86-168">OUTPUTS</span></span>

## <span data-ttu-id="35b86-169">INFORMA</span><span class="sxs-lookup"><span data-stu-id="35b86-169">NOTES</span></span>

## <span data-ttu-id="35b86-170">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="35b86-170">RELATED LINKS</span></span>

[<span data-ttu-id="35b86-171">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="35b86-171">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="35b86-172">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="35b86-172">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="35b86-173">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="35b86-173">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)


