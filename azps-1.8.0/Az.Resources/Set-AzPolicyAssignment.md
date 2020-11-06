---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
ms.openlocfilehash: 2b699219281d64e50694f7e7dd70a965626f7132
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599316"
---
# <span data-ttu-id="4af83-101">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="4af83-101">Set-AzPolicyAssignment</span></span>

## <span data-ttu-id="4af83-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4af83-102">SYNOPSIS</span></span>
<span data-ttu-id="4af83-103">Modifica uma atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="4af83-103">Modifies a policy assignment.</span></span>

## <span data-ttu-id="4af83-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4af83-104">SYNTAX</span></span>

### <span data-ttu-id="4af83-105">NameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="4af83-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4af83-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4af83-106">IdParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4af83-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4af83-107">DESCRIPTION</span></span>
<span data-ttu-id="4af83-108">O cmdlet **set-AzPolicyAssignment** modifica uma atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="4af83-108">The **Set-AzPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="4af83-109">Especifique uma atribuição por ID ou por nome e escopo.</span><span class="sxs-lookup"><span data-stu-id="4af83-109">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="4af83-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4af83-110">EXAMPLES</span></span>

### <span data-ttu-id="4af83-111">Exemplo 1: atualizar o nome para exibição</span><span class="sxs-lookup"><span data-stu-id="4af83-111">Example 1: Update the display name</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName 'Do not allow VM creation'
```

<span data-ttu-id="4af83-112">O primeiro comando obtém um grupo de recursos chamado ResourceGroup11 usando o cmdlet Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="4af83-112">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="4af83-113">O comando armazena esse objeto na variável $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="4af83-113">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="4af83-114">O segundo comando obtém a atribuição de política chamada PolicyAssignment usando o cmdlet Get-AzPolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="4af83-114">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="4af83-115">O comando armazena esse objeto na variável $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="4af83-115">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="4af83-116">O comando final atualiza o nome de exibição na atribuição de política no grupo de recursos identificado pela propriedade **ResourceId** de $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="4af83-116">The final command updates the display name on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="4af83-117">Exemplo 2: adicionar uma identidade gerenciada à atribuição de política</span><span class="sxs-lookup"><span data-stu-id="4af83-117">Example 2: Add a managed identity to the policy assignment</span></span>
```
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -AssignIdentity -Location 'westus'
```

<span data-ttu-id="4af83-118">O primeiro comando obtém a atribuição de política chamada PolicyAssignment da assinatura atual usando o cmdlet Get-AzPolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="4af83-118">The first command gets the policy assignment named PolicyAssignment from the current subscription by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="4af83-119">O comando armazena esse objeto na variável $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="4af83-119">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="4af83-120">O comando final atribui uma identidade gerenciada à atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="4af83-120">The final command assigns a managed identity to the policy assignment.</span></span>

## <span data-ttu-id="4af83-121">OS</span><span class="sxs-lookup"><span data-stu-id="4af83-121">PARAMETERS</span></span>

### <span data-ttu-id="4af83-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4af83-122">-ApiVersion</span></span>
<span data-ttu-id="4af83-123">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="4af83-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="4af83-124">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="4af83-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="4af83-125">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="4af83-125">-AssignIdentity</span></span>
<span data-ttu-id="4af83-126">Gerar e atribuir uma identidade do Azure Active Directory para esta atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="4af83-126">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="4af83-127">A identidade será usada ao executar implantações para políticas de "deployIfNotExists".</span><span class="sxs-lookup"><span data-stu-id="4af83-127">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="4af83-128">A localização é necessária ao atribuir uma identidade.</span><span class="sxs-lookup"><span data-stu-id="4af83-128">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="4af83-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4af83-129">-DefaultProfile</span></span>
<span data-ttu-id="4af83-130">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="4af83-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4af83-131">-Descrição</span><span class="sxs-lookup"><span data-stu-id="4af83-131">-Description</span></span>
<span data-ttu-id="4af83-132">A descrição da atribuição de política</span><span class="sxs-lookup"><span data-stu-id="4af83-132">The description for policy assignment</span></span>

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

### <span data-ttu-id="4af83-133">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="4af83-133">-DisplayName</span></span>
<span data-ttu-id="4af83-134">Especifica um novo nome de exibição para a atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="4af83-134">Specifies a new display name for the policy assignment.</span></span>

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

### <span data-ttu-id="4af83-135">-ID</span><span class="sxs-lookup"><span data-stu-id="4af83-135">-Id</span></span>
<span data-ttu-id="4af83-136">Especifica a ID de recurso totalmente qualificado para a atribuição de política que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="4af83-136">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="4af83-137">-Local</span><span class="sxs-lookup"><span data-stu-id="4af83-137">-Location</span></span>
<span data-ttu-id="4af83-138">O local da identidade do recurso da atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="4af83-138">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="4af83-139">Isso é necessário quando a opção-AssignIdentity é usada.</span><span class="sxs-lookup"><span data-stu-id="4af83-139">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="4af83-140">-Metadados</span><span class="sxs-lookup"><span data-stu-id="4af83-140">-Metadata</span></span>
<span data-ttu-id="4af83-141">Os metadados atualizados para a atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="4af83-141">The updated metadata for the policy assignment.</span></span> <span data-ttu-id="4af83-142">Isso pode ser um caminho para um nome de arquivo que contém os metadados ou os metadados como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="4af83-142">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="4af83-143">-Nome</span><span class="sxs-lookup"><span data-stu-id="4af83-143">-Name</span></span>
<span data-ttu-id="4af83-144">Especifica o nome da atribuição de política que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="4af83-144">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="4af83-145">-Não-escopo</span><span class="sxs-lookup"><span data-stu-id="4af83-145">-NotScope</span></span>
<span data-ttu-id="4af83-146">A atribuição de política não é de escopos.</span><span class="sxs-lookup"><span data-stu-id="4af83-146">The policy assignment not scopes.</span></span>

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

### <span data-ttu-id="4af83-147">-Pre</span><span class="sxs-lookup"><span data-stu-id="4af83-147">-Pre</span></span>
<span data-ttu-id="4af83-148">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="4af83-148">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="4af83-149">-Escopo</span><span class="sxs-lookup"><span data-stu-id="4af83-149">-Scope</span></span>
<span data-ttu-id="4af83-150">Especifica o escopo no qual a política é aplicada.</span><span class="sxs-lookup"><span data-stu-id="4af83-150">Specifies the scope at which the policy is applied.</span></span>

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

### <span data-ttu-id="4af83-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4af83-151">CommonParameters</span></span>
<span data-ttu-id="4af83-152">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4af83-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4af83-153">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4af83-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4af83-154">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4af83-154">INPUTS</span></span>

### <span data-ttu-id="4af83-155">System. String</span><span class="sxs-lookup"><span data-stu-id="4af83-155">System.String</span></span>

### <span data-ttu-id="4af83-156">System. String []</span><span class="sxs-lookup"><span data-stu-id="4af83-156">System.String[]</span></span>

## <span data-ttu-id="4af83-157">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4af83-157">OUTPUTS</span></span>

### <span data-ttu-id="4af83-158">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="4af83-158">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="4af83-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4af83-159">NOTES</span></span>

## <span data-ttu-id="4af83-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4af83-160">RELATED LINKS</span></span>

[<span data-ttu-id="4af83-161">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="4af83-161">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="4af83-162">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="4af83-162">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="4af83-163">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="4af83-163">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)


