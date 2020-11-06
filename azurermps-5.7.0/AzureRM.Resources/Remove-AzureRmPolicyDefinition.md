---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: DEC01722-EB1A-45CE-BD30-9DB861718573
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyDefinition.md
ms.openlocfilehash: 68c4f94ea4fee91c03ab0c65cbcba0f025c3c43b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602142"
---
# <span data-ttu-id="e2755-101">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e2755-101">Remove-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="e2755-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e2755-102">SYNOPSIS</span></span>
<span data-ttu-id="e2755-103">Remove uma definição de política.</span><span class="sxs-lookup"><span data-stu-id="e2755-103">Removes a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2755-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e2755-104">SYNTAX</span></span>

### <span data-ttu-id="e2755-105">RemoveByPolicyDefinitionName (padrão)</span><span class="sxs-lookup"><span data-stu-id="e2755-105">RemoveByPolicyDefinitionName (Default)</span></span>
```
Remove-AzureRmPolicyDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2755-106">RemoveByPolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="e2755-106">RemoveByPolicyDefinitionId</span></span>
```
Remove-AzureRmPolicyDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2755-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e2755-107">DESCRIPTION</span></span>
<span data-ttu-id="e2755-108">O cmdlet **Remove-AzureRmPolicyDefinition** remove uma definição de política.</span><span class="sxs-lookup"><span data-stu-id="e2755-108">The **Remove-AzureRmPolicyDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="e2755-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e2755-109">EXAMPLES</span></span>

### <span data-ttu-id="e2755-110">Exemplo 1: remover a definição de política por nome</span><span class="sxs-lookup"><span data-stu-id="e2755-110">Example 1: Remove the policy definition by name</span></span>
```
PS C:\>Remove-AzureRmPolicyDefinition -Name "VMPolicyDefinition"
```

<span data-ttu-id="e2755-111">Este comando Remove a definição de política especificada.</span><span class="sxs-lookup"><span data-stu-id="e2755-111">This command removes the specified policy definition.</span></span>

### <span data-ttu-id="e2755-112">Exemplo 2: remover a definição de política por ID do recurso</span><span class="sxs-lookup"><span data-stu-id="e2755-112">Example 2: Remove policy definition by resource ID</span></span>
```
PS C:\>$PolicyDefinition = Get-AzureRmPolicyDefinition -Name "VMPolicyDefinition" 
PS C:\> Remove-AzureRmPolicyDefinition -Id $PolicyDefinition.ResourceId -Force
```

<span data-ttu-id="e2755-113">O primeiro comando obtém uma definição de política chamada VMPolicyDefinition usando o cmdlet Get-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="e2755-113">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="e2755-114">O comando o armazena na variável $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="e2755-114">The command stores it in the $PolicyDefinition variable.</span></span>

<span data-ttu-id="e2755-115">O segundo comando Remove a definição de política identificada pela propriedade **ResourceId** de $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="e2755-115">The second command removes the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="e2755-116">OS</span><span class="sxs-lookup"><span data-stu-id="e2755-116">PARAMETERS</span></span>

### <span data-ttu-id="e2755-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e2755-117">-ApiVersion</span></span>
<span data-ttu-id="e2755-118">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="e2755-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="e2755-119">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="e2755-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2755-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2755-120">-DefaultProfile</span></span>
<span data-ttu-id="e2755-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="e2755-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2755-122">-Force</span><span class="sxs-lookup"><span data-stu-id="e2755-122">-Force</span></span>
<span data-ttu-id="e2755-123">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="e2755-123">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2755-124">-ID</span><span class="sxs-lookup"><span data-stu-id="e2755-124">-Id</span></span>
<span data-ttu-id="e2755-125">Especifica a ID de recurso totalmente qualificado para a definição de política que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="e2755-125">Specifies the fully qualified resource ID for the policy definition that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByPolicyDefinitionId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2755-126">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="e2755-126">-InformationAction</span></span>
<span data-ttu-id="e2755-127">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="e2755-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e2755-128">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="e2755-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e2755-129">Contínuo</span><span class="sxs-lookup"><span data-stu-id="e2755-129">Continue</span></span>
- <span data-ttu-id="e2755-130">Ignorar</span><span class="sxs-lookup"><span data-stu-id="e2755-130">Ignore</span></span>
- <span data-ttu-id="e2755-131">Inquire</span><span class="sxs-lookup"><span data-stu-id="e2755-131">Inquire</span></span>
- <span data-ttu-id="e2755-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e2755-132">SilentlyContinue</span></span>
- <span data-ttu-id="e2755-133">Finaliza</span><span class="sxs-lookup"><span data-stu-id="e2755-133">Stop</span></span>
- <span data-ttu-id="e2755-134">Suspensão</span><span class="sxs-lookup"><span data-stu-id="e2755-134">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2755-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e2755-135">-InformationVariable</span></span>
<span data-ttu-id="e2755-136">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="e2755-136">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2755-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="e2755-137">-Name</span></span>
<span data-ttu-id="e2755-138">Especifica o nome da definição de política que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="e2755-138">Specifies the name of the policy definition that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByPolicyDefinitionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2755-139">-Pre</span><span class="sxs-lookup"><span data-stu-id="e2755-139">-Pre</span></span>
<span data-ttu-id="e2755-140">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="e2755-140">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2755-141">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e2755-141">-Confirm</span></span>
<span data-ttu-id="e2755-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2755-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2755-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2755-143">-WhatIf</span></span>
<span data-ttu-id="e2755-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e2755-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2755-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e2755-145">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2755-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2755-146">CommonParameters</span></span>
<span data-ttu-id="e2755-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2755-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2755-148">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2755-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2755-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e2755-149">INPUTS</span></span>

### <span data-ttu-id="e2755-150">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="e2755-150">None</span></span>
<span data-ttu-id="e2755-151">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="e2755-151">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e2755-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e2755-152">OUTPUTS</span></span>

### <span data-ttu-id="e2755-153">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e2755-153">System.Boolean</span></span>

## <span data-ttu-id="e2755-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e2755-154">NOTES</span></span>

## <span data-ttu-id="e2755-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e2755-155">RELATED LINKS</span></span>

[<span data-ttu-id="e2755-156">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e2755-156">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="e2755-157">New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e2755-157">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="e2755-158">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e2755-158">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


