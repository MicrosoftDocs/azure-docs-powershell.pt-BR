---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: DEC01722-EB1A-45CE-BD30-9DB861718573
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
ms.openlocfilehash: f932e566d9fe6639e19e4f906775282cd17315d0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773313"
---
# <span data-ttu-id="3c46b-101">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="3c46b-101">Remove-AzPolicyDefinition</span></span>

## <span data-ttu-id="3c46b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3c46b-102">SYNOPSIS</span></span>
<span data-ttu-id="3c46b-103">Remove uma definição de política.</span><span class="sxs-lookup"><span data-stu-id="3c46b-103">Removes a policy definition.</span></span>

## <span data-ttu-id="3c46b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3c46b-104">SYNTAX</span></span>

### <span data-ttu-id="3c46b-105">NameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="3c46b-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c46b-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c46b-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c46b-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c46b-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c46b-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c46b-108">IdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c46b-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3c46b-109">DESCRIPTION</span></span>
<span data-ttu-id="3c46b-110">O cmdlet **Remove-AzPolicyDefinition** remove uma definição de política.</span><span class="sxs-lookup"><span data-stu-id="3c46b-110">The **Remove-AzPolicyDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="3c46b-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3c46b-111">EXAMPLES</span></span>

### <span data-ttu-id="3c46b-112">Exemplo 1: remover a definição de política por nome</span><span class="sxs-lookup"><span data-stu-id="3c46b-112">Example 1: Remove the policy definition by name</span></span>
```
PS C:\> Remove-AzPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="3c46b-113">Este comando Remove a definição de política especificada.</span><span class="sxs-lookup"><span data-stu-id="3c46b-113">This command removes the specified policy definition.</span></span>

### <span data-ttu-id="3c46b-114">Exemplo 2: remover a definição de política por ID do recurso</span><span class="sxs-lookup"><span data-stu-id="3c46b-114">Example 2: Remove policy definition by resource ID</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition' 
PS C:\> Remove-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Force
```

<span data-ttu-id="3c46b-115">O primeiro comando obtém uma definição de política chamada VMPolicyDefinition usando o cmdlet Get-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="3c46b-115">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="3c46b-116">O comando o armazena na variável $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="3c46b-116">The command stores it in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="3c46b-117">O segundo comando Remove a definição de política identificada pela propriedade **ResourceId** de $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="3c46b-117">The second command removes the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="3c46b-118">OS</span><span class="sxs-lookup"><span data-stu-id="3c46b-118">PARAMETERS</span></span>

### <span data-ttu-id="3c46b-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="3c46b-119">-ApiVersion</span></span>
<span data-ttu-id="3c46b-120">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="3c46b-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="3c46b-121">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="3c46b-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="3c46b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c46b-122">-DefaultProfile</span></span>
<span data-ttu-id="3c46b-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="3c46b-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3c46b-124">-Force</span><span class="sxs-lookup"><span data-stu-id="3c46b-124">-Force</span></span>
<span data-ttu-id="3c46b-125">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="3c46b-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3c46b-126">-ID</span><span class="sxs-lookup"><span data-stu-id="3c46b-126">-Id</span></span>
<span data-ttu-id="3c46b-127">Especifica a ID de recurso totalmente qualificado para a definição de política que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="3c46b-127">Specifies the fully qualified resource ID for the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3c46b-128">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="3c46b-128">-ManagementGroupName</span></span>
<span data-ttu-id="3c46b-129">O nome do grupo de gerenciamento da definição de política a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="3c46b-129">The name of the management group of the policy definition to delete.</span></span>

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

### <span data-ttu-id="3c46b-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="3c46b-130">-Name</span></span>
<span data-ttu-id="3c46b-131">Especifica o nome da definição de política que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="3c46b-131">Specifies the name of the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3c46b-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="3c46b-132">-Pre</span></span>
<span data-ttu-id="3c46b-133">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="3c46b-133">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="3c46b-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3c46b-134">-SubscriptionId</span></span>
<span data-ttu-id="3c46b-135">A ID da assinatura da definição da política a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="3c46b-135">The subscription ID of the policy definition to delete.</span></span>

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

### <span data-ttu-id="3c46b-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3c46b-136">-Confirm</span></span>
<span data-ttu-id="3c46b-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c46b-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c46b-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c46b-138">-WhatIf</span></span>
<span data-ttu-id="3c46b-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3c46b-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c46b-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3c46b-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c46b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c46b-141">CommonParameters</span></span>
<span data-ttu-id="3c46b-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c46b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c46b-143">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3c46b-143">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c46b-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3c46b-144">INPUTS</span></span>

### <span data-ttu-id="3c46b-145">System. String</span><span class="sxs-lookup"><span data-stu-id="3c46b-145">System.String</span></span>

### <span data-ttu-id="3c46b-146">System. Nullable ' 1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="3c46b-146">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="3c46b-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3c46b-147">OUTPUTS</span></span>

### <span data-ttu-id="3c46b-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3c46b-148">System.Boolean</span></span>

## <span data-ttu-id="3c46b-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3c46b-149">NOTES</span></span>

## <span data-ttu-id="3c46b-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3c46b-150">RELATED LINKS</span></span>

[<span data-ttu-id="3c46b-151">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="3c46b-151">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="3c46b-152">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="3c46b-152">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="3c46b-153">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="3c46b-153">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


