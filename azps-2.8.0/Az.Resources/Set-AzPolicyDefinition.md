---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: E1AC7139-786C-4DD6-A898-242723E0D159
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
ms.openlocfilehash: 4016809ed2592c5d10bc284e4a692381d7965107
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773305"
---
# <span data-ttu-id="cc3d2-101">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="cc3d2-101">Set-AzPolicyDefinition</span></span>

## <span data-ttu-id="cc3d2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cc3d2-102">SYNOPSIS</span></span>
<span data-ttu-id="cc3d2-103">Modifica uma definição de política.</span><span class="sxs-lookup"><span data-stu-id="cc3d2-103">Modifies a policy definition.</span></span>

## <span data-ttu-id="cc3d2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cc3d2-104">SYNTAX</span></span>

### <span data-ttu-id="cc3d2-105">NameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="cc3d2-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cc3d2-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc3d2-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cc3d2-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc3d2-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -SubscriptionId <Guid> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cc3d2-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc3d2-108">IdParameterSet</span></span>
```
Set-AzPolicyDefinition -Id <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc3d2-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cc3d2-109">DESCRIPTION</span></span>
<span data-ttu-id="cc3d2-110">O cmdlet **set-AzPolicyDefinition** modifica uma definição de política.</span><span class="sxs-lookup"><span data-stu-id="cc3d2-110">The **Set-AzPolicyDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="cc3d2-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cc3d2-111">EXAMPLES</span></span>

### <span data-ttu-id="cc3d2-112">Exemplo 1: atualizar a descrição de uma definição de política</span><span class="sxs-lookup"><span data-stu-id="cc3d2-112">Example 1: Update the description of a policy definition</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition'
PS C:\> Set-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="cc3d2-113">O primeiro comando obtém uma definição de política chamada VMPolicyDefinition usando o cmdlet Get-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="cc3d2-113">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="cc3d2-114">O comando armazena esse objeto na variável $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="cc3d2-114">The command stores that object in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="cc3d2-115">O segundo comando atualiza a descrição da definição de política identificada pela propriedade **ResourceId** de $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="cc3d2-115">The second command updates the description of the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

### <span data-ttu-id="cc3d2-116">Exemplo 2: atualizar o modo de uma definição de política</span><span class="sxs-lookup"><span data-stu-id="cc3d2-116">Example 2: Update the mode of a policy definition</span></span>
```
PS C:\> Set-AzPolicyDefinition -Name 'VMPolicyDefinition' -Mode 'All'
```

<span data-ttu-id="cc3d2-117">Esse comando atualiza a definição de política chamada VMPolicyDefinition usando o cmdlet Set-AzPolicyDefinition para definir a propriedade Mode como ' all'.</span><span class="sxs-lookup"><span data-stu-id="cc3d2-117">This command updates the policy definition named VMPolicyDefinition by using the Set-AzPolicyDefinition cmdlet to set its mode property to 'All'.</span></span>

### <span data-ttu-id="cc3d2-118">Exemplo 3: atualizar os metadados de uma definição de política</span><span class="sxs-lookup"><span data-stu-id="cc3d2-118">Example 3: Update the metadata of a policy definition</span></span>
```
PS C:\> Set-AzPolicyDefinition -Name 'VMPolicyDefinition' -Metadata '{"category":"Virtual Machine"}'


Name               : VMPolicyDefinition
ResourceId         : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
ResourceName       : VMPolicyDefinition
ResourceType       : Microsoft.Authorization/policyDefinitions
SubscriptionId     : 11111111-1111-1111-1111-111111111111
Properties         : @{displayName=VMPolicyDefinition; policyType=Custom; mode=All; metadata=; policyRule=}
PolicyDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
```

<span data-ttu-id="cc3d2-119">Esse comando atualiza os metadados de uma definição de política chamada VMPolicyDefinition para indicar que sua categoria é "máquina virtual".</span><span class="sxs-lookup"><span data-stu-id="cc3d2-119">This command updates the metadata of a policy definition named VMPolicyDefinition to indicate its category is "Virtual Machine".</span></span>

## <span data-ttu-id="cc3d2-120">OS</span><span class="sxs-lookup"><span data-stu-id="cc3d2-120">PARAMETERS</span></span>

### <span data-ttu-id="cc3d2-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="cc3d2-121">-ApiVersion</span></span>
<span data-ttu-id="cc3d2-122">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="cc3d2-122">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="cc3d2-123">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="cc3d2-123">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="cc3d2-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc3d2-124">-DefaultProfile</span></span>
<span data-ttu-id="cc3d2-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="cc3d2-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cc3d2-126">-Descrição</span><span class="sxs-lookup"><span data-stu-id="cc3d2-126">-Description</span></span>
<span data-ttu-id="cc3d2-127">Especifica uma nova descrição para a definição de política.</span><span class="sxs-lookup"><span data-stu-id="cc3d2-127">Specifies a new description for the policy definition.</span></span>

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

### <span data-ttu-id="cc3d2-128">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="cc3d2-128">-DisplayName</span></span>
<span data-ttu-id="cc3d2-129">Especifica um novo nome de exibição para a definição de política.</span><span class="sxs-lookup"><span data-stu-id="cc3d2-129">Specifies a new display name for the policy definition.</span></span>

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

### <span data-ttu-id="cc3d2-130">-ID</span><span class="sxs-lookup"><span data-stu-id="cc3d2-130">-Id</span></span>
<span data-ttu-id="cc3d2-131">Especifica a ID de recurso totalmente qualificado para a definição de política que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="cc3d2-131">Specifies the fully qualified resource ID for the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="cc3d2-132">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="cc3d2-132">-ManagementGroupName</span></span>
<span data-ttu-id="cc3d2-133">O nome do grupo de gerenciamento da definição de política a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="cc3d2-133">The name of the management group of the policy definition to update.</span></span>

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

### <span data-ttu-id="cc3d2-134">-Metadados</span><span class="sxs-lookup"><span data-stu-id="cc3d2-134">-Metadata</span></span>
<span data-ttu-id="cc3d2-135">Os metadados da definição da política.</span><span class="sxs-lookup"><span data-stu-id="cc3d2-135">The metadata for policy definition.</span></span> <span data-ttu-id="cc3d2-136">Isso pode ser um caminho para um nome de arquivo que contém os metadados ou os metadados como cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="cc3d2-136">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

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

### <span data-ttu-id="cc3d2-137">-Mode</span><span class="sxs-lookup"><span data-stu-id="cc3d2-137">-Mode</span></span>
<span data-ttu-id="cc3d2-138">O modo da nova definição de política.</span><span class="sxs-lookup"><span data-stu-id="cc3d2-138">The mode of the new policy definition.</span></span>

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

### <span data-ttu-id="cc3d2-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="cc3d2-139">-Name</span></span>
<span data-ttu-id="cc3d2-140">Especifica o nome da definição de política que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="cc3d2-140">Specifies the name of the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="cc3d2-141">-Parâmetro</span><span class="sxs-lookup"><span data-stu-id="cc3d2-141">-Parameter</span></span>
<span data-ttu-id="cc3d2-142">A declaração Parameters para a definição da política.</span><span class="sxs-lookup"><span data-stu-id="cc3d2-142">The parameters declaration for policy definition.</span></span> <span data-ttu-id="cc3d2-143">Isso pode ser um caminho para um nome de arquivo ou URI que contém a declaração Parameters ou a declaração Parameters como cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="cc3d2-143">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="cc3d2-144">-Política</span><span class="sxs-lookup"><span data-stu-id="cc3d2-144">-Policy</span></span>
<span data-ttu-id="cc3d2-145">Especifica a nova regra de política para a definição de política.</span><span class="sxs-lookup"><span data-stu-id="cc3d2-145">Specifies new policy rule for the policy definition.</span></span>
<span data-ttu-id="cc3d2-146">Você pode especificar o caminho de um arquivo. JSON ou uma cadeia de caracteres que contém a política no formato JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="cc3d2-146">You can specify the path of a .json file or a string that contains the policy in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="cc3d2-147">-Pre</span><span class="sxs-lookup"><span data-stu-id="cc3d2-147">-Pre</span></span>
<span data-ttu-id="cc3d2-148">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="cc3d2-148">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="cc3d2-149">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cc3d2-149">-SubscriptionId</span></span>
<span data-ttu-id="cc3d2-150">A ID da assinatura da definição da política a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="cc3d2-150">The subscription ID of the policy definition to update.</span></span>

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

### <span data-ttu-id="cc3d2-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc3d2-151">CommonParameters</span></span>
<span data-ttu-id="cc3d2-152">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc3d2-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc3d2-153">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cc3d2-153">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc3d2-154">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cc3d2-154">INPUTS</span></span>

### <span data-ttu-id="cc3d2-155">System. String</span><span class="sxs-lookup"><span data-stu-id="cc3d2-155">System.String</span></span>

### <span data-ttu-id="cc3d2-156">System. Nullable ' 1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="cc3d2-156">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="cc3d2-157">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cc3d2-157">OUTPUTS</span></span>

### <span data-ttu-id="cc3d2-158">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="cc3d2-158">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="cc3d2-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cc3d2-159">NOTES</span></span>

## <span data-ttu-id="cc3d2-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cc3d2-160">RELATED LINKS</span></span>

[<span data-ttu-id="cc3d2-161">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="cc3d2-161">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="cc3d2-162">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="cc3d2-162">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="cc3d2-163">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="cc3d2-163">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)

