---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6396AEC3-DFE6-45DA-BCF4-69C55C5D051B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyDefinition.md
ms.openlocfilehash: 52de80f1ad3cf84a7aa309b5e97b7fa24e9419b8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281931"
---
# <span data-ttu-id="c3818-101">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c3818-101">Get-AzPolicyDefinition</span></span>

## <span data-ttu-id="c3818-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c3818-102">SYNOPSIS</span></span>
<span data-ttu-id="c3818-103">Obtém definições de política.</span><span class="sxs-lookup"><span data-stu-id="c3818-103">Gets policy definitions.</span></span>

## <span data-ttu-id="c3818-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c3818-104">SYNTAX</span></span>

### <span data-ttu-id="c3818-105">NameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="c3818-105">NameParameterSet (Default)</span></span>
```
Get-AzPolicyDefinition [-Name <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3818-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3818-106">ManagementGroupNameParameterSet</span></span>
```
Get-AzPolicyDefinition [-Name <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3818-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3818-107">SubscriptionIdParameterSet</span></span>
```
Get-AzPolicyDefinition [-Name <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3818-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3818-108">IdParameterSet</span></span>
```
Get-AzPolicyDefinition -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c3818-109">BuiltinFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3818-109">BuiltinFilterParameterSet</span></span>
```
Get-AzPolicyDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Builtin]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3818-110">CustomFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3818-110">CustomFilterParameterSet</span></span>
```
Get-AzPolicyDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Custom]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3818-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c3818-111">DESCRIPTION</span></span>
<span data-ttu-id="c3818-112">O cmdlet **Get-AzPolicyDefinition** Obtém uma coleção de definições de política ou uma definição de política específica identificada por nome ou ID.</span><span class="sxs-lookup"><span data-stu-id="c3818-112">The **Get-AzPolicyDefinition** cmdlet gets a collection of policy definitions or a specific policy definition identified by name or ID.</span></span>

## <span data-ttu-id="c3818-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c3818-113">EXAMPLES</span></span>

### <span data-ttu-id="c3818-114">Exemplo 1: obter todas as definições de política</span><span class="sxs-lookup"><span data-stu-id="c3818-114">Example 1: Get all policy definitions</span></span>
```
PS C:\> Get-AzPolicyDefinition
```

<span data-ttu-id="c3818-115">Esse comando obtém todas as definições de política.</span><span class="sxs-lookup"><span data-stu-id="c3818-115">This command gets all the policy definitions.</span></span>

### <span data-ttu-id="c3818-116">Exemplo 2: obter a definição de política da assinatura atual por nome</span><span class="sxs-lookup"><span data-stu-id="c3818-116">Example 2: Get policy definition from current subscription by name</span></span>
```
PS C:\> Get-AzPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="c3818-117">Esse comando obtém a definição de política chamada VMPolicyDefinition da assinatura padrão atual.</span><span class="sxs-lookup"><span data-stu-id="c3818-117">This command gets the policy definition named VMPolicyDefinition from the current default subscription.</span></span>

### <span data-ttu-id="c3818-118">Exemplo 3: obter a definição de política do grupo Gerenciamento por nome</span><span class="sxs-lookup"><span data-stu-id="c3818-118">Example 3: Get policy definition from management group by name</span></span>
```
PS C:\> Get-AzPolicyDefinition -Name 'VMPolicyDefinition' -ManagementGroupName 'Dept42'
```

<span data-ttu-id="c3818-119">Esse comando obtém a definição de política chamada VMPolicyDefinition do grupo de gerenciamento chamado Dept42.</span><span class="sxs-lookup"><span data-stu-id="c3818-119">This command gets the policy definition named VMPolicyDefinition from the management group named Dept42.</span></span>

### <span data-ttu-id="c3818-120">Exemplo 4: obter todas as definições de política internas da assinatura</span><span class="sxs-lookup"><span data-stu-id="c3818-120">Example 4: Get all built-in policy definitions from subscription</span></span>
```
PS C:\> Get-AzPolicyDefinition -SubscriptionId '3bf44b72-c631-427a-b8c8-53e2595398ca' -Builtin
```

<span data-ttu-id="c3818-121">Este comando obtém todas as definições de política internas da assinatura com ID 3bf44b72-c631-427A-b8c8-53e2595398ca.</span><span class="sxs-lookup"><span data-stu-id="c3818-121">This command gets all built-in policy definitions from the subscription with ID 3bf44b72-c631-427a-b8c8-53e2595398ca.</span></span>

### <span data-ttu-id="c3818-122">Exemplo 5: obter definições de política de uma determinada categoria</span><span class="sxs-lookup"><span data-stu-id="c3818-122">Example 5: Get policy definitions from a given category</span></span>
```
PS C:\> Get-AzPolicyDefinition | where-object {$_.Properties.metadata.category -eq "Virtual Machine"}
```

<span data-ttu-id="c3818-123">Este comando obtém todas as definições de política na categoria "máquina virtual".</span><span class="sxs-lookup"><span data-stu-id="c3818-123">This command gets all policy definitions in category "Virtual Machine".</span></span>

## <span data-ttu-id="c3818-124">OS</span><span class="sxs-lookup"><span data-stu-id="c3818-124">PARAMETERS</span></span>

### <span data-ttu-id="c3818-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c3818-125">-ApiVersion</span></span>
<span data-ttu-id="c3818-126">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="c3818-126">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="c3818-127">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="c3818-127">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="c3818-128">-Builtin</span><span class="sxs-lookup"><span data-stu-id="c3818-128">-Builtin</span></span>
<span data-ttu-id="c3818-129">Limita a lista de resultados a somente definições de política internas.</span><span class="sxs-lookup"><span data-stu-id="c3818-129">Limits list of results to only built-in policy definitions.</span></span>

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

### <span data-ttu-id="c3818-130">-Personalizado</span><span class="sxs-lookup"><span data-stu-id="c3818-130">-Custom</span></span>
<span data-ttu-id="c3818-131">Limita a lista de resultados a somente definições de política personalizadas.</span><span class="sxs-lookup"><span data-stu-id="c3818-131">Limits list of results to only custom policy definitions.</span></span>

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

### <span data-ttu-id="c3818-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3818-132">-DefaultProfile</span></span>
<span data-ttu-id="c3818-133">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="c3818-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c3818-134">-ID</span><span class="sxs-lookup"><span data-stu-id="c3818-134">-Id</span></span>
<span data-ttu-id="c3818-135">Especifica a ID de recurso totalmente qualificado para a definição de política que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="c3818-135">Specifies the fully qualified resource ID for the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c3818-136">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="c3818-136">-ManagementGroupName</span></span>
<span data-ttu-id="c3818-137">O nome do grupo de gerenciamento da (s) definição (ões) da política a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="c3818-137">The name of the management group of the policy definition(s) to get.</span></span>

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

### <span data-ttu-id="c3818-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="c3818-138">-Name</span></span>
<span data-ttu-id="c3818-139">Especifica o nome da definição de política que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="c3818-139">Specifies the name of the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c3818-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="c3818-140">-Pre</span></span>
<span data-ttu-id="c3818-141">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="c3818-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="c3818-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c3818-142">-SubscriptionId</span></span>
<span data-ttu-id="c3818-143">A ID da assinatura da (s) definição (ões) da política a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="c3818-143">The subscription ID of the policy definition(s) to get.</span></span>

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

### <span data-ttu-id="c3818-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3818-144">CommonParameters</span></span>
<span data-ttu-id="c3818-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3818-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3818-146">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c3818-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3818-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c3818-147">INPUTS</span></span>

### <span data-ttu-id="c3818-148">System. String</span><span class="sxs-lookup"><span data-stu-id="c3818-148">System.String</span></span>

### <span data-ttu-id="c3818-149">System. Nullable ' 1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c3818-149">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="c3818-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c3818-150">OUTPUTS</span></span>

### <span data-ttu-id="c3818-151">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="c3818-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="c3818-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c3818-152">NOTES</span></span>

## <span data-ttu-id="c3818-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c3818-153">RELATED LINKS</span></span>

[<span data-ttu-id="c3818-154">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c3818-154">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="c3818-155">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c3818-155">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)

[<span data-ttu-id="c3818-156">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c3818-156">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


