---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6396AEC3-DFE6-45DA-BCF4-69C55C5D051B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzPolicyDefinition.md
ms.openlocfilehash: 66901872a6a7c3e871ce95287b45966aee974b52
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776440"
---
# <span data-ttu-id="b40b2-101">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b40b2-101">Get-AzPolicyDefinition</span></span>

## <span data-ttu-id="b40b2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b40b2-102">SYNOPSIS</span></span>
<span data-ttu-id="b40b2-103">Obtém definições de política.</span><span class="sxs-lookup"><span data-stu-id="b40b2-103">Gets policy definitions.</span></span>

## <span data-ttu-id="b40b2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b40b2-104">SYNTAX</span></span>

### <span data-ttu-id="b40b2-105">NameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="b40b2-105">NameParameterSet (Default)</span></span>
```
Get-AzPolicyDefinition [-Name <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b40b2-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b40b2-106">ManagementGroupNameParameterSet</span></span>
```
Get-AzPolicyDefinition [-Name <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b40b2-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b40b2-107">SubscriptionIdParameterSet</span></span>
```
Get-AzPolicyDefinition [-Name <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b40b2-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b40b2-108">IdParameterSet</span></span>
```
Get-AzPolicyDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b40b2-109">BuiltinFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="b40b2-109">BuiltinFilterParameterSet</span></span>
```
Get-AzPolicyDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Builtin]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b40b2-110">CustomFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="b40b2-110">CustomFilterParameterSet</span></span>
```
Get-AzPolicyDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Custom]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b40b2-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b40b2-111">DESCRIPTION</span></span>
<span data-ttu-id="b40b2-112">O cmdlet **Get-AzPolicyDefinition** Obtém uma coleção de definições de política ou uma definição de política específica identificada por nome ou ID.</span><span class="sxs-lookup"><span data-stu-id="b40b2-112">The **Get-AzPolicyDefinition** cmdlet gets a collection of policy definitions or a specific policy definition identified by name or ID.</span></span>

## <span data-ttu-id="b40b2-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b40b2-113">EXAMPLES</span></span>

### <span data-ttu-id="b40b2-114">Exemplo 1: obter todas as definições de política</span><span class="sxs-lookup"><span data-stu-id="b40b2-114">Example 1: Get all policy definitions</span></span>
```
PS C:\> Get-AzPolicyDefinition
```

<span data-ttu-id="b40b2-115">Esse comando obtém todas as definições de política.</span><span class="sxs-lookup"><span data-stu-id="b40b2-115">This command gets all the policy definitions.</span></span>

### <span data-ttu-id="b40b2-116">Exemplo 2: obter a definição de política da assinatura atual por nome</span><span class="sxs-lookup"><span data-stu-id="b40b2-116">Example 2: Get policy definition from current subscription by name</span></span>
```
PS C:\> Get-AzPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="b40b2-117">Esse comando obtém a definição de política chamada VMPolicyDefinition da assinatura padrão atual.</span><span class="sxs-lookup"><span data-stu-id="b40b2-117">This command gets the policy definition named VMPolicyDefinition from the current default subscription.</span></span>

### <span data-ttu-id="b40b2-118">Exemplo 3: obter a definição de política do grupo Gerenciamento por nome</span><span class="sxs-lookup"><span data-stu-id="b40b2-118">Example 3: Get policy definition from management group by name</span></span>
```
PS C:\> Get-AzPolicyDefinition -Name 'VMPolicyDefinition' -ManagementGroupName 'Dept42'
```

<span data-ttu-id="b40b2-119">Esse comando obtém a definição de política chamada VMPolicyDefinition do grupo de gerenciamento chamado Dept42.</span><span class="sxs-lookup"><span data-stu-id="b40b2-119">This command gets the policy definition named VMPolicyDefinition from the management group named Dept42.</span></span>

### <span data-ttu-id="b40b2-120">Exemplo 4: obter todas as definições de política internas da assinatura</span><span class="sxs-lookup"><span data-stu-id="b40b2-120">Example 4: Get all built-in policy definitions from subscription</span></span>
```
PS C:\> Get-AzPolicyDefinition -SubscriptionId '3bf44b72-c631-427a-b8c8-53e2595398ca' -Builtin
```

<span data-ttu-id="b40b2-121">Este comando obtém todas as definições de política internas da assinatura com ID 3bf44b72-c631-427A-b8c8-53e2595398ca.</span><span class="sxs-lookup"><span data-stu-id="b40b2-121">This command gets all built-in policy definitions from the subscription with ID 3bf44b72-c631-427a-b8c8-53e2595398ca.</span></span>

## <span data-ttu-id="b40b2-122">OS</span><span class="sxs-lookup"><span data-stu-id="b40b2-122">PARAMETERS</span></span>

### <span data-ttu-id="b40b2-123">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b40b2-123">-ApiVersion</span></span>
<span data-ttu-id="b40b2-124">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="b40b2-124">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="b40b2-125">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="b40b2-125">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="b40b2-126">-Builtin</span><span class="sxs-lookup"><span data-stu-id="b40b2-126">-Builtin</span></span>
<span data-ttu-id="b40b2-127">Limita a lista de resultados a somente definições de política internas.</span><span class="sxs-lookup"><span data-stu-id="b40b2-127">Limits list of results to only built-in policy definitions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BuiltinFilterParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b40b2-128">-Personalizado</span><span class="sxs-lookup"><span data-stu-id="b40b2-128">-Custom</span></span>
<span data-ttu-id="b40b2-129">Limita a lista de resultados a somente definições de política personalizadas.</span><span class="sxs-lookup"><span data-stu-id="b40b2-129">Limits list of results to only custom policy definitions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CustomFilterParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b40b2-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b40b2-130">-DefaultProfile</span></span>
<span data-ttu-id="b40b2-131">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="b40b2-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b40b2-132">-ID</span><span class="sxs-lookup"><span data-stu-id="b40b2-132">-Id</span></span>
<span data-ttu-id="b40b2-133">Especifica a ID de recurso totalmente qualificado para a definição de política que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="b40b2-133">Specifies the fully qualified resource ID for the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b40b2-134">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="b40b2-134">-InformationAction</span></span>
<span data-ttu-id="b40b2-135">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="b40b2-135">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="b40b2-136">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="b40b2-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b40b2-137">Contínuo</span><span class="sxs-lookup"><span data-stu-id="b40b2-137">Continue</span></span>
- <span data-ttu-id="b40b2-138">Ignorar</span><span class="sxs-lookup"><span data-stu-id="b40b2-138">Ignore</span></span>
- <span data-ttu-id="b40b2-139">Inquire</span><span class="sxs-lookup"><span data-stu-id="b40b2-139">Inquire</span></span>
- <span data-ttu-id="b40b2-140">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b40b2-140">SilentlyContinue</span></span>
- <span data-ttu-id="b40b2-141">Finaliza</span><span class="sxs-lookup"><span data-stu-id="b40b2-141">Stop</span></span>
- <span data-ttu-id="b40b2-142">Suspensão</span><span class="sxs-lookup"><span data-stu-id="b40b2-142">Suspend</span></span>

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

### <span data-ttu-id="b40b2-143">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b40b2-143">-InformationVariable</span></span>
<span data-ttu-id="b40b2-144">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="b40b2-144">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b40b2-145">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="b40b2-145">-ManagementGroupName</span></span>
<span data-ttu-id="b40b2-146">O nome do grupo de gerenciamento da (s) definição (ões) da política a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="b40b2-146">The name of the management group of the policy definition(s) to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: BuiltinFilterParameterSet, CustomFilterParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b40b2-147">-Nome</span><span class="sxs-lookup"><span data-stu-id="b40b2-147">-Name</span></span>
<span data-ttu-id="b40b2-148">Especifica o nome da definição de política que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="b40b2-148">Specifies the name of the policy definition that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b40b2-149">-Pre</span><span class="sxs-lookup"><span data-stu-id="b40b2-149">-Pre</span></span>
<span data-ttu-id="b40b2-150">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="b40b2-150">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="b40b2-151">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b40b2-151">-SubscriptionId</span></span>
<span data-ttu-id="b40b2-152">A ID da assinatura da (s) definição (ões) da política a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="b40b2-152">The subscription ID of the policy definition(s) to get.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: BuiltinFilterParameterSet, CustomFilterParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b40b2-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b40b2-153">CommonParameters</span></span>
<span data-ttu-id="b40b2-154">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b40b2-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b40b2-155">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b40b2-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b40b2-156">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b40b2-156">INPUTS</span></span>

## <span data-ttu-id="b40b2-157">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b40b2-157">OUTPUTS</span></span>

## <span data-ttu-id="b40b2-158">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b40b2-158">NOTES</span></span>

## <span data-ttu-id="b40b2-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b40b2-159">RELATED LINKS</span></span>

[<span data-ttu-id="b40b2-160">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b40b2-160">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="b40b2-161">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b40b2-161">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)

[<span data-ttu-id="b40b2-162">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b40b2-162">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


