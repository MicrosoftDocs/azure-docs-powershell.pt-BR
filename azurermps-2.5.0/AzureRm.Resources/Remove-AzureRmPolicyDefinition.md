---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: DEC01722-EB1A-45CE-BD30-9DB861718573
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermpolicydefinition
schema: 2.0.0
ms.openlocfilehash: 03da83268a06ac4026604728281b10f767fab9a3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786376"
---
# <span data-ttu-id="d4752-101">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d4752-101">Remove-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="d4752-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d4752-102">SYNOPSIS</span></span>
<span data-ttu-id="d4752-103">Remove uma definição de política.</span><span class="sxs-lookup"><span data-stu-id="d4752-103">Removes a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4752-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d4752-104">SYNTAX</span></span>

### <span data-ttu-id="d4752-105">NameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="d4752-105">NameParameterSet (Default)</span></span>
```
Remove-AzureRmPolicyDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4752-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4752-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzureRmPolicyDefinition -Name <String> [-Force] -ManagementGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4752-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4752-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzureRmPolicyDefinition -Name <String> [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4752-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4752-108">IdParameterSet</span></span>
```
Remove-AzureRmPolicyDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4752-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d4752-109">DESCRIPTION</span></span>
<span data-ttu-id="d4752-110">O cmdlet **Remove-AzureRmPolicyDefinition** remove uma definição de política.</span><span class="sxs-lookup"><span data-stu-id="d4752-110">The **Remove-AzureRmPolicyDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="d4752-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d4752-111">EXAMPLES</span></span>

### <span data-ttu-id="d4752-112">Exemplo 1: remover a definição de política por nome</span><span class="sxs-lookup"><span data-stu-id="d4752-112">Example 1: Remove the policy definition by name</span></span>
```
PS C:\> Remove-AzureRmPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="d4752-113">Este comando Remove a definição de política especificada.</span><span class="sxs-lookup"><span data-stu-id="d4752-113">This command removes the specified policy definition.</span></span>

### <span data-ttu-id="d4752-114">Exemplo 2: remover a definição de política por ID do recurso</span><span class="sxs-lookup"><span data-stu-id="d4752-114">Example 2: Remove policy definition by resource ID</span></span>
```
PS C:\> $PolicyDefinition = Get-AzureRmPolicyDefinition -Name 'VMPolicyDefinition' 
PS C:\> Remove-AzureRmPolicyDefinition -Id $PolicyDefinition.ResourceId -Force
```

<span data-ttu-id="d4752-115">O primeiro comando obtém uma definição de política chamada VMPolicyDefinition usando o cmdlet Get-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="d4752-115">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="d4752-116">O comando o armazena na variável $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="d4752-116">The command stores it in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="d4752-117">O segundo comando Remove a definição de política identificada pela propriedade **ResourceId** de $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="d4752-117">The second command removes the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="d4752-118">OS</span><span class="sxs-lookup"><span data-stu-id="d4752-118">PARAMETERS</span></span>

### <span data-ttu-id="d4752-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d4752-119">-ApiVersion</span></span>
<span data-ttu-id="d4752-120">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="d4752-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="d4752-121">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="d4752-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="d4752-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4752-122">-DefaultProfile</span></span>
<span data-ttu-id="d4752-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="d4752-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d4752-124">-Force</span><span class="sxs-lookup"><span data-stu-id="d4752-124">-Force</span></span>
<span data-ttu-id="d4752-125">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="d4752-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d4752-126">-ID</span><span class="sxs-lookup"><span data-stu-id="d4752-126">-Id</span></span>
<span data-ttu-id="d4752-127">Especifica a ID de recurso totalmente qualificado para a definição de política que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="d4752-127">Specifies the fully qualified resource ID for the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d4752-128">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="d4752-128">-InformationAction</span></span>
<span data-ttu-id="d4752-129">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="d4752-129">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="d4752-130">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="d4752-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d4752-131">Contínuo</span><span class="sxs-lookup"><span data-stu-id="d4752-131">Continue</span></span>
- <span data-ttu-id="d4752-132">Ignorar</span><span class="sxs-lookup"><span data-stu-id="d4752-132">Ignore</span></span>
- <span data-ttu-id="d4752-133">Inquire</span><span class="sxs-lookup"><span data-stu-id="d4752-133">Inquire</span></span>
- <span data-ttu-id="d4752-134">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d4752-134">SilentlyContinue</span></span>
- <span data-ttu-id="d4752-135">Finaliza</span><span class="sxs-lookup"><span data-stu-id="d4752-135">Stop</span></span>
- <span data-ttu-id="d4752-136">Suspensão</span><span class="sxs-lookup"><span data-stu-id="d4752-136">Suspend</span></span>

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

### <span data-ttu-id="d4752-137">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d4752-137">-InformationVariable</span></span>
<span data-ttu-id="d4752-138">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="d4752-138">Specifies an information variable.</span></span>

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

### <span data-ttu-id="d4752-139">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="d4752-139">-ManagementGroupName</span></span>
<span data-ttu-id="d4752-140">O nome do grupo de gerenciamento da definição de política a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="d4752-140">The name of the management group of the policy definition to delete.</span></span>

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

### <span data-ttu-id="d4752-141">-Nome</span><span class="sxs-lookup"><span data-stu-id="d4752-141">-Name</span></span>
<span data-ttu-id="d4752-142">Especifica o nome da definição de política que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="d4752-142">Specifies the name of the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d4752-143">-Pre</span><span class="sxs-lookup"><span data-stu-id="d4752-143">-Pre</span></span>
<span data-ttu-id="d4752-144">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="d4752-144">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="d4752-145">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d4752-145">-SubscriptionId</span></span>
<span data-ttu-id="d4752-146">A ID da assinatura da definição da política a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="d4752-146">The subscription ID of the policy definition to delete.</span></span>

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

### <span data-ttu-id="d4752-147">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d4752-147">-Confirm</span></span>
<span data-ttu-id="d4752-148">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4752-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4752-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4752-149">-WhatIf</span></span>
<span data-ttu-id="d4752-150">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d4752-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4752-151">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d4752-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4752-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4752-152">CommonParameters</span></span>
<span data-ttu-id="d4752-153">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4752-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4752-154">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4752-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4752-155">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d4752-155">INPUTS</span></span>

## <span data-ttu-id="d4752-156">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d4752-156">OUTPUTS</span></span>

## <span data-ttu-id="d4752-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d4752-157">NOTES</span></span>

## <span data-ttu-id="d4752-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d4752-158">RELATED LINKS</span></span>

[<span data-ttu-id="d4752-159">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d4752-159">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="d4752-160">New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d4752-160">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="d4752-161">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d4752-161">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


