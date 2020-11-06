---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: DEC01722-EB1A-45CE-BD30-9DB861718573
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyDefinition.md
ms.openlocfilehash: 9d59a974a29743004228efb414a92627782bd8e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609747"
---
# <span data-ttu-id="b2403-101">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b2403-101">Remove-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="b2403-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b2403-102">SYNOPSIS</span></span>
<span data-ttu-id="b2403-103">Remove uma definição de política.</span><span class="sxs-lookup"><span data-stu-id="b2403-103">Removes a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2403-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b2403-104">SYNTAX</span></span>

### <span data-ttu-id="b2403-105">NameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="b2403-105">NameParameterSet (Default)</span></span>
```
Remove-AzureRmPolicyDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2403-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2403-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzureRmPolicyDefinition -Name <String> [-Force] -ManagementGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2403-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2403-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzureRmPolicyDefinition -Name <String> [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2403-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2403-108">IdParameterSet</span></span>
```
Remove-AzureRmPolicyDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2403-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b2403-109">DESCRIPTION</span></span>
<span data-ttu-id="b2403-110">O cmdlet **Remove-AzureRmPolicyDefinition** remove uma definição de política.</span><span class="sxs-lookup"><span data-stu-id="b2403-110">The **Remove-AzureRmPolicyDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="b2403-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b2403-111">EXAMPLES</span></span>

### <span data-ttu-id="b2403-112">Exemplo 1: remover a definição de política por nome</span><span class="sxs-lookup"><span data-stu-id="b2403-112">Example 1: Remove the policy definition by name</span></span>
```
PS C:\> Remove-AzureRmPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="b2403-113">Este comando Remove a definição de política especificada.</span><span class="sxs-lookup"><span data-stu-id="b2403-113">This command removes the specified policy definition.</span></span>

### <span data-ttu-id="b2403-114">Exemplo 2: remover a definição de política por ID do recurso</span><span class="sxs-lookup"><span data-stu-id="b2403-114">Example 2: Remove policy definition by resource ID</span></span>
```
PS C:\> $PolicyDefinition = Get-AzureRmPolicyDefinition -Name 'VMPolicyDefinition' 
PS C:\> Remove-AzureRmPolicyDefinition -Id $PolicyDefinition.ResourceId -Force
```

<span data-ttu-id="b2403-115">O primeiro comando obtém uma definição de política chamada VMPolicyDefinition usando o cmdlet Get-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="b2403-115">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="b2403-116">O comando o armazena na variável $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="b2403-116">The command stores it in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="b2403-117">O segundo comando Remove a definição de política identificada pela propriedade **ResourceId** de $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="b2403-117">The second command removes the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="b2403-118">OS</span><span class="sxs-lookup"><span data-stu-id="b2403-118">PARAMETERS</span></span>

### <span data-ttu-id="b2403-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b2403-119">-ApiVersion</span></span>
<span data-ttu-id="b2403-120">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="b2403-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="b2403-121">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="b2403-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="b2403-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2403-122">-DefaultProfile</span></span>
<span data-ttu-id="b2403-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="b2403-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b2403-124">-Force</span><span class="sxs-lookup"><span data-stu-id="b2403-124">-Force</span></span>
<span data-ttu-id="b2403-125">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="b2403-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b2403-126">-ID</span><span class="sxs-lookup"><span data-stu-id="b2403-126">-Id</span></span>
<span data-ttu-id="b2403-127">Especifica a ID de recurso totalmente qualificado para a definição de política que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="b2403-127">Specifies the fully qualified resource ID for the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b2403-128">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="b2403-128">-InformationAction</span></span>
<span data-ttu-id="b2403-129">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="b2403-129">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="b2403-130">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="b2403-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b2403-131">Contínuo</span><span class="sxs-lookup"><span data-stu-id="b2403-131">Continue</span></span>
- <span data-ttu-id="b2403-132">Ignorar</span><span class="sxs-lookup"><span data-stu-id="b2403-132">Ignore</span></span>
- <span data-ttu-id="b2403-133">Inquire</span><span class="sxs-lookup"><span data-stu-id="b2403-133">Inquire</span></span>
- <span data-ttu-id="b2403-134">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b2403-134">SilentlyContinue</span></span>
- <span data-ttu-id="b2403-135">Finaliza</span><span class="sxs-lookup"><span data-stu-id="b2403-135">Stop</span></span>
- <span data-ttu-id="b2403-136">Suspensão</span><span class="sxs-lookup"><span data-stu-id="b2403-136">Suspend</span></span>

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

### <span data-ttu-id="b2403-137">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b2403-137">-InformationVariable</span></span>
<span data-ttu-id="b2403-138">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="b2403-138">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b2403-139">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="b2403-139">-ManagementGroupName</span></span>
<span data-ttu-id="b2403-140">O nome do grupo de gerenciamento da definição de política a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="b2403-140">The name of the management group of the policy definition to delete.</span></span>

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

### <span data-ttu-id="b2403-141">-Nome</span><span class="sxs-lookup"><span data-stu-id="b2403-141">-Name</span></span>
<span data-ttu-id="b2403-142">Especifica o nome da definição de política que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="b2403-142">Specifies the name of the policy definition that this cmdlet removes.</span></span>

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

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2403-143">-Pre</span><span class="sxs-lookup"><span data-stu-id="b2403-143">-Pre</span></span>
<span data-ttu-id="b2403-144">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="b2403-144">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="b2403-145">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b2403-145">-SubscriptionId</span></span>
<span data-ttu-id="b2403-146">A ID da assinatura da definição da política a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="b2403-146">The subscription ID of the policy definition to delete.</span></span>

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

### <span data-ttu-id="b2403-147">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b2403-147">-Confirm</span></span>
<span data-ttu-id="b2403-148">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2403-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2403-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2403-149">-WhatIf</span></span>
<span data-ttu-id="b2403-150">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b2403-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2403-151">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b2403-151">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2403-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2403-152">CommonParameters</span></span>
<span data-ttu-id="b2403-153">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2403-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2403-154">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2403-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2403-155">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b2403-155">INPUTS</span></span>

## <span data-ttu-id="b2403-156">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b2403-156">OUTPUTS</span></span>

## <span data-ttu-id="b2403-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b2403-157">NOTES</span></span>

## <span data-ttu-id="b2403-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b2403-158">RELATED LINKS</span></span>

[<span data-ttu-id="b2403-159">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b2403-159">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="b2403-160">New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b2403-160">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="b2403-161">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b2403-161">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


