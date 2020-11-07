---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: DEC01722-EB1A-45CE-BD30-9DB861718573
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
ms.openlocfilehash: 8cd1ee1d8f32bd203e9fb2d8ac5d75c2d6b2938d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776345"
---
# <span data-ttu-id="020f4-101">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="020f4-101">Remove-AzPolicyDefinition</span></span>

## <span data-ttu-id="020f4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="020f4-102">SYNOPSIS</span></span>
<span data-ttu-id="020f4-103">Remove uma definição de política.</span><span class="sxs-lookup"><span data-stu-id="020f4-103">Removes a policy definition.</span></span>

## <span data-ttu-id="020f4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="020f4-104">SYNTAX</span></span>

### <span data-ttu-id="020f4-105">NameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="020f4-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="020f4-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="020f4-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -ManagementGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="020f4-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="020f4-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="020f4-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="020f4-108">IdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="020f4-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="020f4-109">DESCRIPTION</span></span>
<span data-ttu-id="020f4-110">O cmdlet **Remove-AzPolicyDefinition** remove uma definição de política.</span><span class="sxs-lookup"><span data-stu-id="020f4-110">The **Remove-AzPolicyDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="020f4-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="020f4-111">EXAMPLES</span></span>

### <span data-ttu-id="020f4-112">Exemplo 1: remover a definição de política por nome</span><span class="sxs-lookup"><span data-stu-id="020f4-112">Example 1: Remove the policy definition by name</span></span>
```
PS C:\> Remove-AzPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="020f4-113">Este comando Remove a definição de política especificada.</span><span class="sxs-lookup"><span data-stu-id="020f4-113">This command removes the specified policy definition.</span></span>

### <span data-ttu-id="020f4-114">Exemplo 2: remover a definição de política por ID do recurso</span><span class="sxs-lookup"><span data-stu-id="020f4-114">Example 2: Remove policy definition by resource ID</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition' 
PS C:\> Remove-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Force
```

<span data-ttu-id="020f4-115">O primeiro comando obtém uma definição de política chamada VMPolicyDefinition usando o cmdlet Get-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="020f4-115">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="020f4-116">O comando o armazena na variável $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="020f4-116">The command stores it in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="020f4-117">O segundo comando Remove a definição de política identificada pela propriedade **ResourceId** de $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="020f4-117">The second command removes the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="020f4-118">OS</span><span class="sxs-lookup"><span data-stu-id="020f4-118">PARAMETERS</span></span>

### <span data-ttu-id="020f4-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="020f4-119">-ApiVersion</span></span>
<span data-ttu-id="020f4-120">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="020f4-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="020f4-121">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="020f4-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="020f4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="020f4-122">-DefaultProfile</span></span>
<span data-ttu-id="020f4-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="020f4-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="020f4-124">-Force</span><span class="sxs-lookup"><span data-stu-id="020f4-124">-Force</span></span>
<span data-ttu-id="020f4-125">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="020f4-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="020f4-126">-ID</span><span class="sxs-lookup"><span data-stu-id="020f4-126">-Id</span></span>
<span data-ttu-id="020f4-127">Especifica a ID de recurso totalmente qualificado para a definição de política que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="020f4-127">Specifies the fully qualified resource ID for the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="020f4-128">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="020f4-128">-InformationAction</span></span>
<span data-ttu-id="020f4-129">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="020f4-129">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="020f4-130">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="020f4-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="020f4-131">Contínuo</span><span class="sxs-lookup"><span data-stu-id="020f4-131">Continue</span></span>
- <span data-ttu-id="020f4-132">Ignorar</span><span class="sxs-lookup"><span data-stu-id="020f4-132">Ignore</span></span>
- <span data-ttu-id="020f4-133">Inquire</span><span class="sxs-lookup"><span data-stu-id="020f4-133">Inquire</span></span>
- <span data-ttu-id="020f4-134">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="020f4-134">SilentlyContinue</span></span>
- <span data-ttu-id="020f4-135">Finaliza</span><span class="sxs-lookup"><span data-stu-id="020f4-135">Stop</span></span>
- <span data-ttu-id="020f4-136">Suspensão</span><span class="sxs-lookup"><span data-stu-id="020f4-136">Suspend</span></span>

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

### <span data-ttu-id="020f4-137">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="020f4-137">-InformationVariable</span></span>
<span data-ttu-id="020f4-138">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="020f4-138">Specifies an information variable.</span></span>

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

### <span data-ttu-id="020f4-139">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="020f4-139">-ManagementGroupName</span></span>
<span data-ttu-id="020f4-140">O nome do grupo de gerenciamento da definição de política a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="020f4-140">The name of the management group of the policy definition to delete.</span></span>

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

### <span data-ttu-id="020f4-141">-Nome</span><span class="sxs-lookup"><span data-stu-id="020f4-141">-Name</span></span>
<span data-ttu-id="020f4-142">Especifica o nome da definição de política que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="020f4-142">Specifies the name of the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="020f4-143">-Pre</span><span class="sxs-lookup"><span data-stu-id="020f4-143">-Pre</span></span>
<span data-ttu-id="020f4-144">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="020f4-144">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="020f4-145">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="020f4-145">-SubscriptionId</span></span>
<span data-ttu-id="020f4-146">A ID da assinatura da definição da política a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="020f4-146">The subscription ID of the policy definition to delete.</span></span>

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

### <span data-ttu-id="020f4-147">-Confirme</span><span class="sxs-lookup"><span data-stu-id="020f4-147">-Confirm</span></span>
<span data-ttu-id="020f4-148">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="020f4-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="020f4-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="020f4-149">-WhatIf</span></span>
<span data-ttu-id="020f4-150">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="020f4-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="020f4-151">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="020f4-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="020f4-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="020f4-152">CommonParameters</span></span>
<span data-ttu-id="020f4-153">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="020f4-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="020f4-154">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="020f4-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="020f4-155">SENSORES</span><span class="sxs-lookup"><span data-stu-id="020f4-155">INPUTS</span></span>

## <span data-ttu-id="020f4-156">EXIBE</span><span class="sxs-lookup"><span data-stu-id="020f4-156">OUTPUTS</span></span>

## <span data-ttu-id="020f4-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="020f4-157">NOTES</span></span>

## <span data-ttu-id="020f4-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="020f4-158">RELATED LINKS</span></span>

[<span data-ttu-id="020f4-159">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="020f4-159">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="020f4-160">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="020f4-160">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="020f4-161">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="020f4-161">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


