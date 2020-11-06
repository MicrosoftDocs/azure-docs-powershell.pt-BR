---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: E1AC7139-786C-4DD6-A898-242723E0D159
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyDefinition.md
ms.openlocfilehash: 4f71814790d5c543a867ad4de0aaac37c98079a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440283"
---
# <span data-ttu-id="92f5a-101">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="92f5a-101">Set-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="92f5a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="92f5a-102">SYNOPSIS</span></span>
<span data-ttu-id="92f5a-103">Modifica uma definição de política.</span><span class="sxs-lookup"><span data-stu-id="92f5a-103">Modifies a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92f5a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="92f5a-104">SYNTAX</span></span>

### <span data-ttu-id="92f5a-105">NameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="92f5a-105">NameParameterSet (Default)</span></span>
```
Set-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="92f5a-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="92f5a-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="92f5a-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="92f5a-107">SubscriptionIdParameterSet</span></span>
```
Set-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] -SubscriptionId <Guid>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="92f5a-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="92f5a-108">IdParameterSet</span></span>
```
Set-AzureRmPolicyDefinition -Id <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="92f5a-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="92f5a-109">DESCRIPTION</span></span>
<span data-ttu-id="92f5a-110">O cmdlet **set-AzureRmPolicyDefinition** modifica uma definição de política.</span><span class="sxs-lookup"><span data-stu-id="92f5a-110">The **Set-AzureRmPolicyDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="92f5a-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="92f5a-111">EXAMPLES</span></span>

### <span data-ttu-id="92f5a-112">Exemplo 1: atualizar a descrição de uma definição de política</span><span class="sxs-lookup"><span data-stu-id="92f5a-112">Example 1: Update the description of a policy definition</span></span>
```
PS C:\> $PolicyDefinition = Get-AzureRmPolicyDefinition -Name 'VMPolicyDefinition'
PS C:\> Set-AzureRmPolicyDefinition -Id $PolicyDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="92f5a-113">O primeiro comando obtém uma definição de política chamada VMPolicyDefinition usando o cmdlet Get-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="92f5a-113">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="92f5a-114">O comando armazena esse objeto na variável $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="92f5a-114">The command stores that object in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="92f5a-115">O segundo comando atualiza a descrição da definição de política identificada pela propriedade **ResourceId** de $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="92f5a-115">The second command updates the description of the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

### <span data-ttu-id="92f5a-116">Exemplo 2: atualizar o modo de uma definição de política</span><span class="sxs-lookup"><span data-stu-id="92f5a-116">Example 2: Update the mode of a policy definition</span></span>
```
PS C:\> Set-AzureRmPolicyDefinition -Name 'VMPolicyDefinition' -Mode 'All'
```

<span data-ttu-id="92f5a-117">Esse comando atualiza a definição de política chamada VMPolicyDefinition usando o cmdlet Set-AzureRmPolicyDefinition para definir a propriedade Mode como ' all'.</span><span class="sxs-lookup"><span data-stu-id="92f5a-117">This command updates the policy definition named VMPolicyDefinition by using the Set-AzureRmPolicyDefinition cmdlet to set its mode property to 'All'.</span></span>

## <span data-ttu-id="92f5a-118">OS</span><span class="sxs-lookup"><span data-stu-id="92f5a-118">PARAMETERS</span></span>

### <span data-ttu-id="92f5a-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="92f5a-119">-ApiVersion</span></span>
<span data-ttu-id="92f5a-120">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="92f5a-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="92f5a-121">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="92f5a-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="92f5a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92f5a-122">-DefaultProfile</span></span>
<span data-ttu-id="92f5a-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="92f5a-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="92f5a-124">-Descrição</span><span class="sxs-lookup"><span data-stu-id="92f5a-124">-Description</span></span>
<span data-ttu-id="92f5a-125">Especifica uma nova descrição para a definição de política.</span><span class="sxs-lookup"><span data-stu-id="92f5a-125">Specifies a new description for the policy definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92f5a-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="92f5a-126">-DisplayName</span></span>
<span data-ttu-id="92f5a-127">Especifica um novo nome de exibição para a definição de política.</span><span class="sxs-lookup"><span data-stu-id="92f5a-127">Specifies a new display name for the policy definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92f5a-128">-ID</span><span class="sxs-lookup"><span data-stu-id="92f5a-128">-Id</span></span>
<span data-ttu-id="92f5a-129">Especifica a ID de recurso totalmente qualificado para a definição de política que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="92f5a-129">Specifies the fully qualified resource ID for the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="92f5a-130">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="92f5a-130">-InformationAction</span></span>
<span data-ttu-id="92f5a-131">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="92f5a-131">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="92f5a-132">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="92f5a-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="92f5a-133">Contínuo</span><span class="sxs-lookup"><span data-stu-id="92f5a-133">Continue</span></span>
- <span data-ttu-id="92f5a-134">Ignorar</span><span class="sxs-lookup"><span data-stu-id="92f5a-134">Ignore</span></span>
- <span data-ttu-id="92f5a-135">Inquire</span><span class="sxs-lookup"><span data-stu-id="92f5a-135">Inquire</span></span>
- <span data-ttu-id="92f5a-136">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="92f5a-136">SilentlyContinue</span></span>
- <span data-ttu-id="92f5a-137">Finaliza</span><span class="sxs-lookup"><span data-stu-id="92f5a-137">Stop</span></span>
- <span data-ttu-id="92f5a-138">Suspensão</span><span class="sxs-lookup"><span data-stu-id="92f5a-138">Suspend</span></span>

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

### <span data-ttu-id="92f5a-139">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="92f5a-139">-InformationVariable</span></span>
<span data-ttu-id="92f5a-140">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="92f5a-140">Specifies an information variable.</span></span>

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

### <span data-ttu-id="92f5a-141">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="92f5a-141">-ManagementGroupName</span></span>
<span data-ttu-id="92f5a-142">O nome do grupo de gerenciamento da definição de política a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="92f5a-142">The name of the management group of the policy definition to update.</span></span>

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

### <span data-ttu-id="92f5a-143">-Metadados</span><span class="sxs-lookup"><span data-stu-id="92f5a-143">-Metadata</span></span>
<span data-ttu-id="92f5a-144">Os metadados da definição da política.</span><span class="sxs-lookup"><span data-stu-id="92f5a-144">The metadata for policy definition.</span></span> <span data-ttu-id="92f5a-145">Isso pode ser um caminho para um nome de arquivo que contém os metadados ou os metadados como cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="92f5a-145">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92f5a-146">-Mode</span><span class="sxs-lookup"><span data-stu-id="92f5a-146">-Mode</span></span>
<span data-ttu-id="92f5a-147">O modo da nova definição de política.</span><span class="sxs-lookup"><span data-stu-id="92f5a-147">The mode of the new policy definition.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Policy.PolicyDefinitionMode]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92f5a-148">-Nome</span><span class="sxs-lookup"><span data-stu-id="92f5a-148">-Name</span></span>
<span data-ttu-id="92f5a-149">Especifica o nome da definição de política que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="92f5a-149">Specifies the name of the policy definition that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92f5a-150">-Parâmetro</span><span class="sxs-lookup"><span data-stu-id="92f5a-150">-Parameter</span></span>
<span data-ttu-id="92f5a-151">A declaração Parameters para a definição da política.</span><span class="sxs-lookup"><span data-stu-id="92f5a-151">The parameters declaration for policy definition.</span></span> <span data-ttu-id="92f5a-152">Isso pode ser um caminho para um nome de arquivo ou URI que contém a declaração Parameters ou a declaração Parameters como cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="92f5a-152">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92f5a-153">-Política</span><span class="sxs-lookup"><span data-stu-id="92f5a-153">-Policy</span></span>
<span data-ttu-id="92f5a-154">Especifica a nova regra de política para a definição de política.</span><span class="sxs-lookup"><span data-stu-id="92f5a-154">Specifies new policy rule for the policy definition.</span></span>
<span data-ttu-id="92f5a-155">Você pode especificar o caminho de um arquivo. JSON ou uma cadeia de caracteres que contém a política no formato JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="92f5a-155">You can specify the path of a .json file or a string that contains the policy in JavaScript Object Notation (JSON) format.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92f5a-156">-Pre</span><span class="sxs-lookup"><span data-stu-id="92f5a-156">-Pre</span></span>
<span data-ttu-id="92f5a-157">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="92f5a-157">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="92f5a-158">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="92f5a-158">-SubscriptionId</span></span>
<span data-ttu-id="92f5a-159">A ID da assinatura da definição da política a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="92f5a-159">The subscription ID of the policy definition to update.</span></span>

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

### <span data-ttu-id="92f5a-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92f5a-160">CommonParameters</span></span>
<span data-ttu-id="92f5a-161">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92f5a-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92f5a-162">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92f5a-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92f5a-163">SENSORES</span><span class="sxs-lookup"><span data-stu-id="92f5a-163">INPUTS</span></span>

## <span data-ttu-id="92f5a-164">EXIBE</span><span class="sxs-lookup"><span data-stu-id="92f5a-164">OUTPUTS</span></span>

## <span data-ttu-id="92f5a-165">INFORMA</span><span class="sxs-lookup"><span data-stu-id="92f5a-165">NOTES</span></span>

## <span data-ttu-id="92f5a-166">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="92f5a-166">RELATED LINKS</span></span>

[<span data-ttu-id="92f5a-167">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="92f5a-167">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="92f5a-168">New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="92f5a-168">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="92f5a-169">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="92f5a-169">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)


