---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BA40BD11-8167-48D7-AC71-72B2FD9924F2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyAssignment.md
ms.openlocfilehash: fa43b462cf06b9e2cd58df5d6796c098e942fafc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609573"
---
# <span data-ttu-id="25601-101">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="25601-101">New-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="25601-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="25601-102">SYNOPSIS</span></span>
<span data-ttu-id="25601-103">Cria uma atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="25601-103">Creates a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25601-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="25601-104">SYNTAX</span></span>

### <span data-ttu-id="25601-105">Atribuição de política sem parâmetros (padrão)</span><span class="sxs-lookup"><span data-stu-id="25601-105">Policy assignment without parameters (Default)</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] [-PolicySetDefinition <PSObject>] [-Sku <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="25601-106">Atribuição de política com parâmetros por objeto de parâmetro de política</span><span class="sxs-lookup"><span data-stu-id="25601-106">Policy assignment with parameters via policy parameter object</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameterObject <Hashtable> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="25601-107">Atribuição de política com parâmetros por cadeia de parâmetro de política</span><span class="sxs-lookup"><span data-stu-id="25601-107">Policy assignment with parameters via policy parameter string</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameter <String> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="25601-108">Atribuição de política com parâmetros por meio do objeto de parâmetro de conjunto de políticas</span><span class="sxs-lookup"><span data-stu-id="25601-108">Policy assignment with parameters via policy set parameter object</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameterObject <Hashtable> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="25601-109">Atribuição de política com parâmetros por cadeia de parâmetro de conjunto de políticas</span><span class="sxs-lookup"><span data-stu-id="25601-109">Policy assignment with parameters via policy set parameter string</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameter <String> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="25601-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="25601-110">DESCRIPTION</span></span>
<span data-ttu-id="25601-111">O cmdlet **New-AzureRmPolicyAssignment** cria uma atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="25601-111">The **New-AzureRmPolicyAssignment** cmdlet creates a policy assignment.</span></span>
<span data-ttu-id="25601-112">Especifique uma política e um escopo.</span><span class="sxs-lookup"><span data-stu-id="25601-112">Specify a policy and scope.</span></span>

## <span data-ttu-id="25601-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="25601-113">EXAMPLES</span></span>

### <span data-ttu-id="25601-114">Exemplo 1: atribuição de política em nível de grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="25601-114">Example 1: Policy assignment at resource group level</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> $Policy = Get-AzureRmPolicyDefinition -Name "VirtualMachinePolicy"
PS C:\> New-AzureRmPolicyAssignment -Name "VirtualMachinePolicyAssignment" -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="25601-115">O primeiro comando obtém um grupo de recursos chamado ResourceGroup11 usando o cmdlet Get-AzureRMResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="25601-115">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="25601-116">O comando armazena esse objeto na variável $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="25601-116">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="25601-117">O segundo comando obtém a definição de política chamada VirtualMachinePolicy usando o cmdlet Get-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="25601-117">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="25601-118">O comando armazena esse objeto na variável $Policy.</span><span class="sxs-lookup"><span data-stu-id="25601-118">The command stores that object in the $Policy variable.</span></span>

<span data-ttu-id="25601-119">O comando final atribui a política em $Policy no nível de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="25601-119">The final command assigns the policy in $Policy at the level of a resource group.</span></span>
<span data-ttu-id="25601-120">A propriedade **ResourceId** de $ResourceGroup identifica o grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="25601-120">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

## <span data-ttu-id="25601-121">OS</span><span class="sxs-lookup"><span data-stu-id="25601-121">PARAMETERS</span></span>

### <span data-ttu-id="25601-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="25601-122">-ApiVersion</span></span>
<span data-ttu-id="25601-123">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="25601-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="25601-124">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="25601-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="25601-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="25601-125">-DisplayName</span></span>
<span data-ttu-id="25601-126">Especifica um nome de exibição para a atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="25601-126">Specifies a display name for the policy assignment.</span></span>

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

### <span data-ttu-id="25601-127">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="25601-127">-InformationAction</span></span>
<span data-ttu-id="25601-128">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="25601-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="25601-129">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="25601-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="25601-130">Contínuo</span><span class="sxs-lookup"><span data-stu-id="25601-130">Continue</span></span>
- <span data-ttu-id="25601-131">Ignorar</span><span class="sxs-lookup"><span data-stu-id="25601-131">Ignore</span></span>
- <span data-ttu-id="25601-132">Inquire</span><span class="sxs-lookup"><span data-stu-id="25601-132">Inquire</span></span>
- <span data-ttu-id="25601-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="25601-133">SilentlyContinue</span></span>
- <span data-ttu-id="25601-134">Finaliza</span><span class="sxs-lookup"><span data-stu-id="25601-134">Stop</span></span>
- <span data-ttu-id="25601-135">Suspensão</span><span class="sxs-lookup"><span data-stu-id="25601-135">Suspend</span></span>

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

### <span data-ttu-id="25601-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="25601-136">-InformationVariable</span></span>
<span data-ttu-id="25601-137">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="25601-137">Specifies an information variable.</span></span>

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

### <span data-ttu-id="25601-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="25601-138">-Name</span></span>
<span data-ttu-id="25601-139">Especifica um nome para a atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="25601-139">Specifies a name for the policy assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25601-140">-Não-escopo</span><span class="sxs-lookup"><span data-stu-id="25601-140">-NotScope</span></span>
<span data-ttu-id="25601-141">Os não escopos para atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="25601-141">The not scopes for policy assignment.</span></span>

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

### <span data-ttu-id="25601-142">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="25601-142">-PolicyDefinition</span></span>
<span data-ttu-id="25601-143">Especifica uma política, como um objeto **PSObject** que contém a regra de política.</span><span class="sxs-lookup"><span data-stu-id="25601-143">Specifies a policy, as a **PSObject** object that contains the policy rule.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Policy assignment without parameters, Policy assignment with parameters via policy set parameter object, Policy assignment with parameters via policy set parameter string
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Policy assignment with parameters via policy parameter object, Policy assignment with parameters via policy parameter string
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25601-144">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="25601-144">-PolicyParameter</span></span>
<span data-ttu-id="25601-145">O caminho do arquivo de parâmetro da política ou a cadeia de caracteres de parâmetro da política.</span><span class="sxs-lookup"><span data-stu-id="25601-145">The policy parameter file path or policy parameter string.</span></span>

```yaml
Type: System.String
Parameter Sets: Policy assignment with parameters via policy parameter string, Policy assignment with parameters via policy set parameter string
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25601-146">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="25601-146">-PolicyParameterObject</span></span>
<span data-ttu-id="25601-147">O objeto de parâmetro de política.</span><span class="sxs-lookup"><span data-stu-id="25601-147">The policy parameter object.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Policy assignment with parameters via policy parameter object, Policy assignment with parameters via policy set parameter object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25601-148">-PolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="25601-148">-PolicySetDefinition</span></span>
<span data-ttu-id="25601-149">O objeto de definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="25601-149">The policy set definition object.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Policy assignment without parameters, Policy assignment with parameters via policy parameter object, Policy assignment with parameters via policy parameter string
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Policy assignment with parameters via policy set parameter object, Policy assignment with parameters via policy set parameter string
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25601-150">-Pre</span><span class="sxs-lookup"><span data-stu-id="25601-150">-Pre</span></span>
<span data-ttu-id="25601-151">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="25601-151">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="25601-152">-Escopo</span><span class="sxs-lookup"><span data-stu-id="25601-152">-Scope</span></span>
<span data-ttu-id="25601-153">Especifica o escopo no qual atribuir a política.</span><span class="sxs-lookup"><span data-stu-id="25601-153">Specifies the scope at which to assign the policy.</span></span>
<span data-ttu-id="25601-154">Por exemplo, para atribuir uma política a um grupo de recursos, especifique o seguinte:</span><span class="sxs-lookup"><span data-stu-id="25601-154">For instance, to assign a policy to a resource group, specify the following:</span></span>

<span data-ttu-id="25601-155">`/subscriptions/`ID da assinatura `/resourcegroups/` nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="25601-155">`/subscriptions/`subscription ID`/resourcegroups/`resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25601-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25601-156">-DefaultProfile</span></span>
<span data-ttu-id="25601-157">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="25601-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25601-158">-Descrição</span><span class="sxs-lookup"><span data-stu-id="25601-158">-Description</span></span>
<span data-ttu-id="25601-159">A descrição da atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="25601-159">The description for policy assignment.</span></span>

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

### <span data-ttu-id="25601-160">-SKU</span><span class="sxs-lookup"><span data-stu-id="25601-160">-Sku</span></span>
<span data-ttu-id="25601-161">Uma tabela de hash que representa as propriedades de SKU.</span><span class="sxs-lookup"><span data-stu-id="25601-161">A hash table which represents sku properties.</span></span> <span data-ttu-id="25601-162">Padrões para SKU grátis: nome = a0, nível = grátis</span><span class="sxs-lookup"><span data-stu-id="25601-162">Defaults to Free Sku: Name = A0, Tier = Free</span></span>

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

### <span data-ttu-id="25601-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25601-163">CommonParameters</span></span>
<span data-ttu-id="25601-164">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25601-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25601-165">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25601-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25601-166">SENSORES</span><span class="sxs-lookup"><span data-stu-id="25601-166">INPUTS</span></span>

## <span data-ttu-id="25601-167">EXIBE</span><span class="sxs-lookup"><span data-stu-id="25601-167">OUTPUTS</span></span>

### <span data-ttu-id="25601-168">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="25601-168">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="25601-169">INFORMA</span><span class="sxs-lookup"><span data-stu-id="25601-169">NOTES</span></span>

## <span data-ttu-id="25601-170">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="25601-170">RELATED LINKS</span></span>

[<span data-ttu-id="25601-171">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="25601-171">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="25601-172">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="25601-172">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="25601-173">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="25601-173">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)

[<span data-ttu-id="25601-174">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="25601-174">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


