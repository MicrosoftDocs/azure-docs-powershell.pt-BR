---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6396AEC3-DFE6-45DA-BCF4-69C55C5D051B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermpolicydefinition
schema: 2.0.0
ms.openlocfilehash: 5bd650583a933ba8d7ea56762c918d386b630c6c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785865"
---
# <span data-ttu-id="18395-101">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="18395-101">Get-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="18395-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="18395-102">SYNOPSIS</span></span>
<span data-ttu-id="18395-103">Obtém definições de política.</span><span class="sxs-lookup"><span data-stu-id="18395-103">Gets policy definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18395-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="18395-104">SYNTAX</span></span>

### <span data-ttu-id="18395-105">NameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="18395-105">NameParameterSet (Default)</span></span>
```
Get-AzureRmPolicyDefinition [-Name <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="18395-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="18395-106">ManagementGroupNameParameterSet</span></span>
```
Get-AzureRmPolicyDefinition [-Name <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="18395-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="18395-107">SubscriptionIdParameterSet</span></span>
```
Get-AzureRmPolicyDefinition [-Name <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="18395-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="18395-108">IdParameterSet</span></span>
```
Get-AzureRmPolicyDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="18395-109">BuiltinFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="18395-109">BuiltinFilterParameterSet</span></span>
```
Get-AzureRmPolicyDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Builtin]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="18395-110">CustomFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="18395-110">CustomFilterParameterSet</span></span>
```
Get-AzureRmPolicyDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Custom]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="18395-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="18395-111">DESCRIPTION</span></span>
<span data-ttu-id="18395-112">O cmdlet **Get-AzureRmPolicyDefinition** Obtém uma coleção de definições de política ou uma definição de política específica identificada por nome ou ID.</span><span class="sxs-lookup"><span data-stu-id="18395-112">The **Get-AzureRmPolicyDefinition** cmdlet gets a collection of policy definitions or a specific policy definition identified by name or ID.</span></span>

## <span data-ttu-id="18395-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="18395-113">EXAMPLES</span></span>

### <span data-ttu-id="18395-114">Exemplo 1: obter todas as definições de política</span><span class="sxs-lookup"><span data-stu-id="18395-114">Example 1: Get all policy definitions</span></span>
```
PS C:\> Get-AzureRmPolicyDefinition
```

<span data-ttu-id="18395-115">Esse comando obtém todas as definições de política.</span><span class="sxs-lookup"><span data-stu-id="18395-115">This command gets all the policy definitions.</span></span>

### <span data-ttu-id="18395-116">Exemplo 2: obter a definição de política da assinatura atual por nome</span><span class="sxs-lookup"><span data-stu-id="18395-116">Example 2: Get policy definition from current subscription by name</span></span>
```
PS C:\> Get-AzureRmPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="18395-117">Esse comando obtém a definição de política chamada VMPolicyDefinition da assinatura padrão atual.</span><span class="sxs-lookup"><span data-stu-id="18395-117">This command gets the policy definition named VMPolicyDefinition from the current default subscription.</span></span>

### <span data-ttu-id="18395-118">Exemplo 3: obter a definição de política do grupo Gerenciamento por nome</span><span class="sxs-lookup"><span data-stu-id="18395-118">Example 3: Get policy definition from management group by name</span></span>
```
PS C:\> Get-AzureRmPolicyDefinition -Name 'VMPolicyDefinition' -ManagementGroupName 'Dept42'
```

<span data-ttu-id="18395-119">Esse comando obtém a definição de política chamada VMPolicyDefinition do grupo de gerenciamento chamado Dept42.</span><span class="sxs-lookup"><span data-stu-id="18395-119">This command gets the policy definition named VMPolicyDefinition from the management group named Dept42.</span></span>

### <span data-ttu-id="18395-120">Exemplo 4: obter todas as definições de política internas da assinatura</span><span class="sxs-lookup"><span data-stu-id="18395-120">Example 4: Get all built-in policy definitions from subscription</span></span>
```
PS C:\> Get-AzureRmPolicyDefinition -SubscriptionId '3bf44b72-c631-427a-b8c8-53e2595398ca' -Builtin
```

<span data-ttu-id="18395-121">Este comando obtém todas as definições de política internas da assinatura com ID 3bf44b72-c631-427A-b8c8-53e2595398ca.</span><span class="sxs-lookup"><span data-stu-id="18395-121">This command gets all built-in policy definitions from the subscription with ID 3bf44b72-c631-427a-b8c8-53e2595398ca.</span></span>

## <span data-ttu-id="18395-122">OS</span><span class="sxs-lookup"><span data-stu-id="18395-122">PARAMETERS</span></span>

### <span data-ttu-id="18395-123">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="18395-123">-ApiVersion</span></span>
<span data-ttu-id="18395-124">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="18395-124">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="18395-125">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="18395-125">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="18395-126">-Builtin</span><span class="sxs-lookup"><span data-stu-id="18395-126">-Builtin</span></span>
<span data-ttu-id="18395-127">Limita a lista de resultados a somente definições de política internas.</span><span class="sxs-lookup"><span data-stu-id="18395-127">Limits list of results to only built-in policy definitions.</span></span>

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

### <span data-ttu-id="18395-128">-Personalizado</span><span class="sxs-lookup"><span data-stu-id="18395-128">-Custom</span></span>
<span data-ttu-id="18395-129">Limita a lista de resultados a somente definições de política personalizadas.</span><span class="sxs-lookup"><span data-stu-id="18395-129">Limits list of results to only custom policy definitions.</span></span>

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

### <span data-ttu-id="18395-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18395-130">-DefaultProfile</span></span>
<span data-ttu-id="18395-131">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="18395-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="18395-132">-ID</span><span class="sxs-lookup"><span data-stu-id="18395-132">-Id</span></span>
<span data-ttu-id="18395-133">Especifica a ID de recurso totalmente qualificado para a definição de política que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="18395-133">Specifies the fully qualified resource ID for the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="18395-134">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="18395-134">-InformationAction</span></span>
<span data-ttu-id="18395-135">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="18395-135">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="18395-136">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="18395-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="18395-137">Contínuo</span><span class="sxs-lookup"><span data-stu-id="18395-137">Continue</span></span>
- <span data-ttu-id="18395-138">Ignorar</span><span class="sxs-lookup"><span data-stu-id="18395-138">Ignore</span></span>
- <span data-ttu-id="18395-139">Inquire</span><span class="sxs-lookup"><span data-stu-id="18395-139">Inquire</span></span>
- <span data-ttu-id="18395-140">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="18395-140">SilentlyContinue</span></span>
- <span data-ttu-id="18395-141">Finaliza</span><span class="sxs-lookup"><span data-stu-id="18395-141">Stop</span></span>
- <span data-ttu-id="18395-142">Suspensão</span><span class="sxs-lookup"><span data-stu-id="18395-142">Suspend</span></span>

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

### <span data-ttu-id="18395-143">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="18395-143">-InformationVariable</span></span>
<span data-ttu-id="18395-144">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="18395-144">Specifies an information variable.</span></span>

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

### <span data-ttu-id="18395-145">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="18395-145">-ManagementGroupName</span></span>
<span data-ttu-id="18395-146">O nome do grupo de gerenciamento da (s) definição (ões) da política a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="18395-146">The name of the management group of the policy definition(s) to get.</span></span>

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

### <span data-ttu-id="18395-147">-Nome</span><span class="sxs-lookup"><span data-stu-id="18395-147">-Name</span></span>
<span data-ttu-id="18395-148">Especifica o nome da definição de política que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="18395-148">Specifies the name of the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="18395-149">-Pre</span><span class="sxs-lookup"><span data-stu-id="18395-149">-Pre</span></span>
<span data-ttu-id="18395-150">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="18395-150">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="18395-151">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="18395-151">-SubscriptionId</span></span>
<span data-ttu-id="18395-152">A ID da assinatura da (s) definição (ões) da política a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="18395-152">The subscription ID of the policy definition(s) to get.</span></span>

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

### <span data-ttu-id="18395-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18395-153">CommonParameters</span></span>
<span data-ttu-id="18395-154">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18395-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18395-155">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18395-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18395-156">SENSORES</span><span class="sxs-lookup"><span data-stu-id="18395-156">INPUTS</span></span>

## <span data-ttu-id="18395-157">EXIBE</span><span class="sxs-lookup"><span data-stu-id="18395-157">OUTPUTS</span></span>

## <span data-ttu-id="18395-158">INFORMA</span><span class="sxs-lookup"><span data-stu-id="18395-158">NOTES</span></span>

## <span data-ttu-id="18395-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="18395-159">RELATED LINKS</span></span>

[<span data-ttu-id="18395-160">New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="18395-160">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="18395-161">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="18395-161">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)

[<span data-ttu-id="18395-162">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="18395-162">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


