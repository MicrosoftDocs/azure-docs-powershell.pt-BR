---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: E1AC7139-786C-4DD6-A898-242723E0D159
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermpolicydefinition
schema: 2.0.0
ms.openlocfilehash: aa6687efb331cbb702ea36c53cc02cd77cefd45d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785424"
---
# <span data-ttu-id="e42c9-101">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e42c9-101">Set-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="e42c9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e42c9-102">SYNOPSIS</span></span>
<span data-ttu-id="e42c9-103">Modifica uma definição de política.</span><span class="sxs-lookup"><span data-stu-id="e42c9-103">Modifies a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e42c9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e42c9-104">SYNTAX</span></span>

### <span data-ttu-id="e42c9-105">NameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="e42c9-105">NameParameterSet (Default)</span></span>
```
Set-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="e42c9-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e42c9-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="e42c9-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e42c9-107">SubscriptionIdParameterSet</span></span>
```
Set-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] -SubscriptionId <Guid>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="e42c9-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e42c9-108">IdParameterSet</span></span>
```
Set-AzureRmPolicyDefinition -Id <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="e42c9-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e42c9-109">DESCRIPTION</span></span>
<span data-ttu-id="e42c9-110">O cmdlet **set-AzureRmPolicyDefinition** modifica uma definição de política.</span><span class="sxs-lookup"><span data-stu-id="e42c9-110">The **Set-AzureRmPolicyDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="e42c9-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e42c9-111">EXAMPLES</span></span>

### <span data-ttu-id="e42c9-112">Exemplo 1: atualizar a descrição de uma definição de política</span><span class="sxs-lookup"><span data-stu-id="e42c9-112">Example 1: Update the description of a policy definition</span></span>
```
PS C:\> $PolicyDefinition = Get-AzureRmPolicyDefinition -Name 'VMPolicyDefinition'
PS C:\> Set-AzureRmPolicyDefinition -Id $PolicyDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="e42c9-113">O primeiro comando obtém uma definição de política chamada VMPolicyDefinition usando o cmdlet Get-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="e42c9-113">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="e42c9-114">O comando armazena esse objeto na variável $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="e42c9-114">The command stores that object in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="e42c9-115">O segundo comando atualiza a descrição da definição de política identificada pela propriedade **ResourceId** de $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="e42c9-115">The second command updates the description of the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

### <span data-ttu-id="e42c9-116">Exemplo 2: atualizar o modo de uma definição de política</span><span class="sxs-lookup"><span data-stu-id="e42c9-116">Example 2: Update the mode of a policy definition</span></span>
```
PS C:\> Set-AzureRmPolicyDefinition -Name 'VMPolicyDefinition' -Mode 'All'
```

<span data-ttu-id="e42c9-117">Esse comando atualiza a definição de política chamada VMPolicyDefinition usando o cmdlet Set-AzureRmPolicyDefinition para definir a propriedade Mode como ' all'.</span><span class="sxs-lookup"><span data-stu-id="e42c9-117">This command updates the policy definition named VMPolicyDefinition by using the Set-AzureRmPolicyDefinition cmdlet to set its mode property to 'All'.</span></span>

## <span data-ttu-id="e42c9-118">OS</span><span class="sxs-lookup"><span data-stu-id="e42c9-118">PARAMETERS</span></span>

### <span data-ttu-id="e42c9-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e42c9-119">-ApiVersion</span></span>
<span data-ttu-id="e42c9-120">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="e42c9-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="e42c9-121">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="e42c9-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="e42c9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e42c9-122">-DefaultProfile</span></span>
<span data-ttu-id="e42c9-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="e42c9-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e42c9-124">-Descrição</span><span class="sxs-lookup"><span data-stu-id="e42c9-124">-Description</span></span>
<span data-ttu-id="e42c9-125">Especifica uma nova descrição para a definição de política.</span><span class="sxs-lookup"><span data-stu-id="e42c9-125">Specifies a new description for the policy definition.</span></span>

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

### <span data-ttu-id="e42c9-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e42c9-126">-DisplayName</span></span>
<span data-ttu-id="e42c9-127">Especifica um novo nome de exibição para a definição de política.</span><span class="sxs-lookup"><span data-stu-id="e42c9-127">Specifies a new display name for the policy definition.</span></span>

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

### <span data-ttu-id="e42c9-128">-ID</span><span class="sxs-lookup"><span data-stu-id="e42c9-128">-Id</span></span>
<span data-ttu-id="e42c9-129">Especifica a ID de recurso totalmente qualificado para a definição de política que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="e42c9-129">Specifies the fully qualified resource ID for the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="e42c9-130">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="e42c9-130">-InformationAction</span></span>
<span data-ttu-id="e42c9-131">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="e42c9-131">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="e42c9-132">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="e42c9-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e42c9-133">Contínuo</span><span class="sxs-lookup"><span data-stu-id="e42c9-133">Continue</span></span>
- <span data-ttu-id="e42c9-134">Ignorar</span><span class="sxs-lookup"><span data-stu-id="e42c9-134">Ignore</span></span>
- <span data-ttu-id="e42c9-135">Inquire</span><span class="sxs-lookup"><span data-stu-id="e42c9-135">Inquire</span></span>
- <span data-ttu-id="e42c9-136">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e42c9-136">SilentlyContinue</span></span>
- <span data-ttu-id="e42c9-137">Finaliza</span><span class="sxs-lookup"><span data-stu-id="e42c9-137">Stop</span></span>
- <span data-ttu-id="e42c9-138">Suspensão</span><span class="sxs-lookup"><span data-stu-id="e42c9-138">Suspend</span></span>

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

### <span data-ttu-id="e42c9-139">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e42c9-139">-InformationVariable</span></span>
<span data-ttu-id="e42c9-140">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="e42c9-140">Specifies an information variable.</span></span>

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

### <span data-ttu-id="e42c9-141">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="e42c9-141">-ManagementGroupName</span></span>
<span data-ttu-id="e42c9-142">O nome do grupo de gerenciamento da definição de política a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="e42c9-142">The name of the management group of the policy definition to update.</span></span>

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

### <span data-ttu-id="e42c9-143">-Metadados</span><span class="sxs-lookup"><span data-stu-id="e42c9-143">-Metadata</span></span>
<span data-ttu-id="e42c9-144">Os metadados da definição da política.</span><span class="sxs-lookup"><span data-stu-id="e42c9-144">The metadata for policy definition.</span></span> <span data-ttu-id="e42c9-145">Isso pode ser um caminho para um nome de arquivo que contém os metadados ou os metadados como cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="e42c9-145">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

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

### <span data-ttu-id="e42c9-146">-Mode</span><span class="sxs-lookup"><span data-stu-id="e42c9-146">-Mode</span></span>
<span data-ttu-id="e42c9-147">O modo da nova definição de política.</span><span class="sxs-lookup"><span data-stu-id="e42c9-147">The mode of the new policy definition.</span></span>

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

### <span data-ttu-id="e42c9-148">-Nome</span><span class="sxs-lookup"><span data-stu-id="e42c9-148">-Name</span></span>
<span data-ttu-id="e42c9-149">Especifica o nome da definição de política que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="e42c9-149">Specifies the name of the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="e42c9-150">-Parâmetro</span><span class="sxs-lookup"><span data-stu-id="e42c9-150">-Parameter</span></span>
<span data-ttu-id="e42c9-151">A declaração Parameters para a definição da política.</span><span class="sxs-lookup"><span data-stu-id="e42c9-151">The parameters declaration for policy definition.</span></span> <span data-ttu-id="e42c9-152">Isso pode ser um caminho para um nome de arquivo ou URI que contém a declaração Parameters ou a declaração Parameters como cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="e42c9-152">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="e42c9-153">-Política</span><span class="sxs-lookup"><span data-stu-id="e42c9-153">-Policy</span></span>
<span data-ttu-id="e42c9-154">Especifica a nova regra de política para a definição de política.</span><span class="sxs-lookup"><span data-stu-id="e42c9-154">Specifies new policy rule for the policy definition.</span></span>
<span data-ttu-id="e42c9-155">Você pode especificar o caminho de um arquivo. JSON ou uma cadeia de caracteres que contém a política no formato JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="e42c9-155">You can specify the path of a .json file or a string that contains the policy in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="e42c9-156">-Pre</span><span class="sxs-lookup"><span data-stu-id="e42c9-156">-Pre</span></span>
<span data-ttu-id="e42c9-157">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="e42c9-157">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e42c9-158">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e42c9-158">-SubscriptionId</span></span>
<span data-ttu-id="e42c9-159">A ID da assinatura da definição da política a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="e42c9-159">The subscription ID of the policy definition to update.</span></span>

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

### <span data-ttu-id="e42c9-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e42c9-160">CommonParameters</span></span>
<span data-ttu-id="e42c9-161">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e42c9-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e42c9-162">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e42c9-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e42c9-163">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e42c9-163">INPUTS</span></span>

## <span data-ttu-id="e42c9-164">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e42c9-164">OUTPUTS</span></span>

## <span data-ttu-id="e42c9-165">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e42c9-165">NOTES</span></span>

## <span data-ttu-id="e42c9-166">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e42c9-166">RELATED LINKS</span></span>

[<span data-ttu-id="e42c9-167">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e42c9-167">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="e42c9-168">New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e42c9-168">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="e42c9-169">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e42c9-169">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)


