---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6396AEC3-DFE6-45DA-BCF4-69C55C5D051B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyDefinition.md
ms.openlocfilehash: 78dc06f53a94f6fe1524189a0cea32f214439f66
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599430"
---
# <span data-ttu-id="34c0b-101">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="34c0b-101">Get-AzPolicyDefinition</span></span>

## <span data-ttu-id="34c0b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="34c0b-102">SYNOPSIS</span></span>
<span data-ttu-id="34c0b-103">Obtém definições de política.</span><span class="sxs-lookup"><span data-stu-id="34c0b-103">Gets policy definitions.</span></span>

## <span data-ttu-id="34c0b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="34c0b-104">SYNTAX</span></span>

### <span data-ttu-id="34c0b-105">NameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="34c0b-105">NameParameterSet (Default)</span></span>
```
Get-AzPolicyDefinition [-Name <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34c0b-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="34c0b-106">ManagementGroupNameParameterSet</span></span>
```
Get-AzPolicyDefinition [-Name <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34c0b-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="34c0b-107">SubscriptionIdParameterSet</span></span>
```
Get-AzPolicyDefinition [-Name <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34c0b-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="34c0b-108">IdParameterSet</span></span>
```
Get-AzPolicyDefinition -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="34c0b-109">BuiltinFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="34c0b-109">BuiltinFilterParameterSet</span></span>
```
Get-AzPolicyDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Builtin]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34c0b-110">CustomFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="34c0b-110">CustomFilterParameterSet</span></span>
```
Get-AzPolicyDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Custom]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34c0b-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="34c0b-111">DESCRIPTION</span></span>
<span data-ttu-id="34c0b-112">O cmdlet **Get-AzPolicyDefinition** Obtém uma coleção de definições de política ou uma definição de política específica identificada por nome ou ID.</span><span class="sxs-lookup"><span data-stu-id="34c0b-112">The **Get-AzPolicyDefinition** cmdlet gets a collection of policy definitions or a specific policy definition identified by name or ID.</span></span>

## <span data-ttu-id="34c0b-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="34c0b-113">EXAMPLES</span></span>

### <span data-ttu-id="34c0b-114">Exemplo 1: obter todas as definições de política</span><span class="sxs-lookup"><span data-stu-id="34c0b-114">Example 1: Get all policy definitions</span></span>
```
PS C:\> Get-AzPolicyDefinition
```

<span data-ttu-id="34c0b-115">Esse comando obtém todas as definições de política.</span><span class="sxs-lookup"><span data-stu-id="34c0b-115">This command gets all the policy definitions.</span></span>

### <span data-ttu-id="34c0b-116">Exemplo 2: obter a definição de política da assinatura atual por nome</span><span class="sxs-lookup"><span data-stu-id="34c0b-116">Example 2: Get policy definition from current subscription by name</span></span>
```
PS C:\> Get-AzPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="34c0b-117">Esse comando obtém a definição de política chamada VMPolicyDefinition da assinatura padrão atual.</span><span class="sxs-lookup"><span data-stu-id="34c0b-117">This command gets the policy definition named VMPolicyDefinition from the current default subscription.</span></span>

### <span data-ttu-id="34c0b-118">Exemplo 3: obter a definição de política do grupo Gerenciamento por nome</span><span class="sxs-lookup"><span data-stu-id="34c0b-118">Example 3: Get policy definition from management group by name</span></span>
```
PS C:\> Get-AzPolicyDefinition -Name 'VMPolicyDefinition' -ManagementGroupName 'Dept42'
```

<span data-ttu-id="34c0b-119">Esse comando obtém a definição de política chamada VMPolicyDefinition do grupo de gerenciamento chamado Dept42.</span><span class="sxs-lookup"><span data-stu-id="34c0b-119">This command gets the policy definition named VMPolicyDefinition from the management group named Dept42.</span></span>

### <span data-ttu-id="34c0b-120">Exemplo 4: obter todas as definições de política internas da assinatura</span><span class="sxs-lookup"><span data-stu-id="34c0b-120">Example 4: Get all built-in policy definitions from subscription</span></span>
```
PS C:\> Get-AzPolicyDefinition -SubscriptionId '3bf44b72-c631-427a-b8c8-53e2595398ca' -Builtin
```

<span data-ttu-id="34c0b-121">Este comando obtém todas as definições de política internas da assinatura com ID 3bf44b72-c631-427A-b8c8-53e2595398ca.</span><span class="sxs-lookup"><span data-stu-id="34c0b-121">This command gets all built-in policy definitions from the subscription with ID 3bf44b72-c631-427a-b8c8-53e2595398ca.</span></span>

## <span data-ttu-id="34c0b-122">OS</span><span class="sxs-lookup"><span data-stu-id="34c0b-122">PARAMETERS</span></span>

### <span data-ttu-id="34c0b-123">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="34c0b-123">-ApiVersion</span></span>
<span data-ttu-id="34c0b-124">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="34c0b-124">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="34c0b-125">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="34c0b-125">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="34c0b-126">-Builtin</span><span class="sxs-lookup"><span data-stu-id="34c0b-126">-Builtin</span></span>
<span data-ttu-id="34c0b-127">Limita a lista de resultados a somente definições de política internas.</span><span class="sxs-lookup"><span data-stu-id="34c0b-127">Limits list of results to only built-in policy definitions.</span></span>

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

### <span data-ttu-id="34c0b-128">-Personalizado</span><span class="sxs-lookup"><span data-stu-id="34c0b-128">-Custom</span></span>
<span data-ttu-id="34c0b-129">Limita a lista de resultados a somente definições de política personalizadas.</span><span class="sxs-lookup"><span data-stu-id="34c0b-129">Limits list of results to only custom policy definitions.</span></span>

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

### <span data-ttu-id="34c0b-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34c0b-130">-DefaultProfile</span></span>
<span data-ttu-id="34c0b-131">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="34c0b-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="34c0b-132">-ID</span><span class="sxs-lookup"><span data-stu-id="34c0b-132">-Id</span></span>
<span data-ttu-id="34c0b-133">Especifica a ID de recurso totalmente qualificado para a definição de política que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="34c0b-133">Specifies the fully qualified resource ID for the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="34c0b-134">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="34c0b-134">-ManagementGroupName</span></span>
<span data-ttu-id="34c0b-135">O nome do grupo de gerenciamento da (s) definição (ões) da política a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="34c0b-135">The name of the management group of the policy definition(s) to get.</span></span>

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

### <span data-ttu-id="34c0b-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="34c0b-136">-Name</span></span>
<span data-ttu-id="34c0b-137">Especifica o nome da definição de política que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="34c0b-137">Specifies the name of the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="34c0b-138">-Pre</span><span class="sxs-lookup"><span data-stu-id="34c0b-138">-Pre</span></span>
<span data-ttu-id="34c0b-139">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="34c0b-139">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="34c0b-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="34c0b-140">-SubscriptionId</span></span>
<span data-ttu-id="34c0b-141">A ID da assinatura da (s) definição (ões) da política a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="34c0b-141">The subscription ID of the policy definition(s) to get.</span></span>

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

### <span data-ttu-id="34c0b-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34c0b-142">CommonParameters</span></span>
<span data-ttu-id="34c0b-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34c0b-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34c0b-144">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34c0b-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34c0b-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="34c0b-145">INPUTS</span></span>

### <span data-ttu-id="34c0b-146">System. String</span><span class="sxs-lookup"><span data-stu-id="34c0b-146">System.String</span></span>

### <span data-ttu-id="34c0b-147">System. Nullable ' 1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="34c0b-147">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="34c0b-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="34c0b-148">OUTPUTS</span></span>

### <span data-ttu-id="34c0b-149">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="34c0b-149">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="34c0b-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="34c0b-150">NOTES</span></span>

## <span data-ttu-id="34c0b-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="34c0b-151">RELATED LINKS</span></span>

[<span data-ttu-id="34c0b-152">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="34c0b-152">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="34c0b-153">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="34c0b-153">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)

[<span data-ttu-id="34c0b-154">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="34c0b-154">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


