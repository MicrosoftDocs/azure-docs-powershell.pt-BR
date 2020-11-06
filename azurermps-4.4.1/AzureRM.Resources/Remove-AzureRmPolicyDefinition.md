---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: DEC01722-EB1A-45CE-BD30-9DB861718573
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyDefinition.md
ms.openlocfilehash: 46323b260330ca84ee1ac2426ee7b6e2ab474f21
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610181"
---
# <span data-ttu-id="23680-101">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="23680-101">Remove-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="23680-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="23680-102">SYNOPSIS</span></span>
<span data-ttu-id="23680-103">Remove uma definição de política.</span><span class="sxs-lookup"><span data-stu-id="23680-103">Removes a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23680-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="23680-104">SYNTAX</span></span>

### <span data-ttu-id="23680-105">O parâmetro nome da definição de política definido.</span><span class="sxs-lookup"><span data-stu-id="23680-105">The policy definition name parameter set.</span></span> <span data-ttu-id="23680-106">Assume</span><span class="sxs-lookup"><span data-stu-id="23680-106">(Default)</span></span>
```
Remove-AzureRmPolicyDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23680-107">O conjunto de parâmetros de ID de definição de política.</span><span class="sxs-lookup"><span data-stu-id="23680-107">The policy definition Id parameter set.</span></span>
```
Remove-AzureRmPolicyDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23680-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="23680-108">DESCRIPTION</span></span>
<span data-ttu-id="23680-109">O cmdlet **Remove-AzureRmPolicyDefinition** remove uma definição de política.</span><span class="sxs-lookup"><span data-stu-id="23680-109">The **Remove-AzureRmPolicyDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="23680-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="23680-110">EXAMPLES</span></span>

### <span data-ttu-id="23680-111">Exemplo 1: remover a definição de política por nome</span><span class="sxs-lookup"><span data-stu-id="23680-111">Example 1: Remove the policy definition by name</span></span>
```
PS C:\>Remove-AzureRmPolicyDefinition -Name "VMPolicyDefinition"
```

<span data-ttu-id="23680-112">Este comando Remove a definição de política especificada.</span><span class="sxs-lookup"><span data-stu-id="23680-112">This command removes the specified policy definition.</span></span>

### <span data-ttu-id="23680-113">Exemplo 2: remover a definição de política por ID do recurso</span><span class="sxs-lookup"><span data-stu-id="23680-113">Example 2: Remove policy definition by resource ID</span></span>
```
PS C:\>$PolicyDefinition = Get-AzureRmPolicyDefinition -Name "VMPolicyDefinition" 
PS C:\> Remove-AzureRmPolicyDefinition -Id $PolicyDefinition.ResourceId -Force
```

<span data-ttu-id="23680-114">O primeiro comando obtém uma definição de política chamada VMPolicyDefinition usando o cmdlet Get-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="23680-114">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="23680-115">O comando o armazena na variável $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="23680-115">The command stores it in the $PolicyDefinition variable.</span></span>

<span data-ttu-id="23680-116">O segundo comando Remove a definição de política identificada pela propriedade **ResourceId** de $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="23680-116">The second command removes the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="23680-117">OS</span><span class="sxs-lookup"><span data-stu-id="23680-117">PARAMETERS</span></span>

### <span data-ttu-id="23680-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="23680-118">-ApiVersion</span></span>
<span data-ttu-id="23680-119">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="23680-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="23680-120">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="23680-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="23680-121">-Force</span><span class="sxs-lookup"><span data-stu-id="23680-121">-Force</span></span>
<span data-ttu-id="23680-122">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="23680-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="23680-123">-ID</span><span class="sxs-lookup"><span data-stu-id="23680-123">-Id</span></span>
<span data-ttu-id="23680-124">Especifica a ID de recurso totalmente qualificado para a definição de política que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="23680-124">Specifies the fully qualified resource ID for the policy definition that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy definition Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23680-125">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="23680-125">-InformationAction</span></span>
<span data-ttu-id="23680-126">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="23680-126">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="23680-127">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="23680-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="23680-128">Contínuo</span><span class="sxs-lookup"><span data-stu-id="23680-128">Continue</span></span>
- <span data-ttu-id="23680-129">Ignorar</span><span class="sxs-lookup"><span data-stu-id="23680-129">Ignore</span></span>
- <span data-ttu-id="23680-130">Inquire</span><span class="sxs-lookup"><span data-stu-id="23680-130">Inquire</span></span>
- <span data-ttu-id="23680-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="23680-131">SilentlyContinue</span></span>
- <span data-ttu-id="23680-132">Finaliza</span><span class="sxs-lookup"><span data-stu-id="23680-132">Stop</span></span>
- <span data-ttu-id="23680-133">Suspensão</span><span class="sxs-lookup"><span data-stu-id="23680-133">Suspend</span></span>

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

### <span data-ttu-id="23680-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="23680-134">-InformationVariable</span></span>
<span data-ttu-id="23680-135">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="23680-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="23680-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="23680-136">-Name</span></span>
<span data-ttu-id="23680-137">Especifica o nome da definição de política que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="23680-137">Specifies the name of the policy definition that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23680-138">-Pre</span><span class="sxs-lookup"><span data-stu-id="23680-138">-Pre</span></span>
<span data-ttu-id="23680-139">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="23680-139">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="23680-140">-Confirme</span><span class="sxs-lookup"><span data-stu-id="23680-140">-Confirm</span></span>
<span data-ttu-id="23680-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23680-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23680-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23680-142">-WhatIf</span></span>
<span data-ttu-id="23680-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="23680-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23680-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="23680-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23680-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23680-145">-DefaultProfile</span></span>
<span data-ttu-id="23680-146">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="23680-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23680-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23680-147">CommonParameters</span></span>
<span data-ttu-id="23680-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23680-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23680-149">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23680-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23680-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="23680-150">INPUTS</span></span>

## <span data-ttu-id="23680-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="23680-151">OUTPUTS</span></span>

### <span data-ttu-id="23680-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="23680-152">System.Boolean</span></span>

## <span data-ttu-id="23680-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="23680-153">NOTES</span></span>

## <span data-ttu-id="23680-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="23680-154">RELATED LINKS</span></span>

[<span data-ttu-id="23680-155">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="23680-155">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="23680-156">New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="23680-156">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="23680-157">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="23680-157">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


