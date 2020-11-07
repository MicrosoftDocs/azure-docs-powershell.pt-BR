---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: E1AC7139-786C-4DD6-A898-242723E0D159
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
ms.openlocfilehash: 9f6f23babc1dfaf947a7eb8cea88011ff184cce7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941737"
---
# <span data-ttu-id="1d971-101">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1d971-101">Set-AzPolicyDefinition</span></span>

## <span data-ttu-id="1d971-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1d971-102">SYNOPSIS</span></span>
<span data-ttu-id="1d971-103">Modifica uma definição de política.</span><span class="sxs-lookup"><span data-stu-id="1d971-103">Modifies a policy definition.</span></span>

## <span data-ttu-id="1d971-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1d971-104">SYNTAX</span></span>

### <span data-ttu-id="1d971-105">NameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="1d971-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d971-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1d971-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d971-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1d971-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -SubscriptionId <Guid> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d971-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1d971-108">IdParameterSet</span></span>
```
Set-AzPolicyDefinition -Id <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d971-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1d971-109">DESCRIPTION</span></span>
<span data-ttu-id="1d971-110">O cmdlet **set-AzPolicyDefinition** modifica uma definição de política.</span><span class="sxs-lookup"><span data-stu-id="1d971-110">The **Set-AzPolicyDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="1d971-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1d971-111">EXAMPLES</span></span>

### <span data-ttu-id="1d971-112">Exemplo 1: atualizar a descrição de uma definição de política</span><span class="sxs-lookup"><span data-stu-id="1d971-112">Example 1: Update the description of a policy definition</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition'
PS C:\> Set-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="1d971-113">O primeiro comando obtém uma definição de política chamada VMPolicyDefinition usando o cmdlet Get-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="1d971-113">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="1d971-114">O comando armazena esse objeto na variável $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="1d971-114">The command stores that object in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="1d971-115">O segundo comando atualiza a descrição da definição de política identificada pela propriedade **ResourceId** de $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="1d971-115">The second command updates the description of the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

### <span data-ttu-id="1d971-116">Exemplo 2: atualizar o modo de uma definição de política</span><span class="sxs-lookup"><span data-stu-id="1d971-116">Example 2: Update the mode of a policy definition</span></span>
```
PS C:\> Set-AzPolicyDefinition -Name 'VMPolicyDefinition' -Mode 'All'
```

<span data-ttu-id="1d971-117">Esse comando atualiza a definição de política chamada VMPolicyDefinition usando o cmdlet Set-AzPolicyDefinition para definir a propriedade Mode como ' all'.</span><span class="sxs-lookup"><span data-stu-id="1d971-117">This command updates the policy definition named VMPolicyDefinition by using the Set-AzPolicyDefinition cmdlet to set its mode property to 'All'.</span></span>

### <span data-ttu-id="1d971-118">Exemplo 3: atualizar os metadados de uma definição de política</span><span class="sxs-lookup"><span data-stu-id="1d971-118">Example 3: Update the metadata of a policy definition</span></span>
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

<span data-ttu-id="1d971-119">Esse comando atualiza os metadados de uma definição de política chamada VMPolicyDefinition para indicar que sua categoria é "máquina virtual".</span><span class="sxs-lookup"><span data-stu-id="1d971-119">This command updates the metadata of a policy definition named VMPolicyDefinition to indicate its category is "Virtual Machine".</span></span>

## <span data-ttu-id="1d971-120">OS</span><span class="sxs-lookup"><span data-stu-id="1d971-120">PARAMETERS</span></span>

### <span data-ttu-id="1d971-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="1d971-121">-ApiVersion</span></span>
<span data-ttu-id="1d971-122">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="1d971-122">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="1d971-123">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="1d971-123">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="1d971-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d971-124">-DefaultProfile</span></span>
<span data-ttu-id="1d971-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="1d971-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1d971-126">-Descrição</span><span class="sxs-lookup"><span data-stu-id="1d971-126">-Description</span></span>
<span data-ttu-id="1d971-127">Especifica uma nova descrição para a definição de política.</span><span class="sxs-lookup"><span data-stu-id="1d971-127">Specifies a new description for the policy definition.</span></span>

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

### <span data-ttu-id="1d971-128">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="1d971-128">-DisplayName</span></span>
<span data-ttu-id="1d971-129">Especifica um novo nome de exibição para a definição de política.</span><span class="sxs-lookup"><span data-stu-id="1d971-129">Specifies a new display name for the policy definition.</span></span>

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

### <span data-ttu-id="1d971-130">-ID</span><span class="sxs-lookup"><span data-stu-id="1d971-130">-Id</span></span>
<span data-ttu-id="1d971-131">Especifica a ID de recurso totalmente qualificado para a definição de política que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="1d971-131">Specifies the fully qualified resource ID for the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="1d971-132">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="1d971-132">-ManagementGroupName</span></span>
<span data-ttu-id="1d971-133">O nome do grupo de gerenciamento da definição de política a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="1d971-133">The name of the management group of the policy definition to update.</span></span>

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

### <span data-ttu-id="1d971-134">-Metadados</span><span class="sxs-lookup"><span data-stu-id="1d971-134">-Metadata</span></span>
<span data-ttu-id="1d971-135">Os metadados da definição da política.</span><span class="sxs-lookup"><span data-stu-id="1d971-135">The metadata for policy definition.</span></span> <span data-ttu-id="1d971-136">Isso pode ser um caminho para um nome de arquivo que contém os metadados ou os metadados como cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="1d971-136">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

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

### <span data-ttu-id="1d971-137">-Mode</span><span class="sxs-lookup"><span data-stu-id="1d971-137">-Mode</span></span>
<span data-ttu-id="1d971-138">O modo da nova definição de política.</span><span class="sxs-lookup"><span data-stu-id="1d971-138">The mode of the new policy definition.</span></span>

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

### <span data-ttu-id="1d971-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="1d971-139">-Name</span></span>
<span data-ttu-id="1d971-140">Especifica o nome da definição de política que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="1d971-140">Specifies the name of the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="1d971-141">-Parâmetro</span><span class="sxs-lookup"><span data-stu-id="1d971-141">-Parameter</span></span>
<span data-ttu-id="1d971-142">A declaração Parameters para a definição da política.</span><span class="sxs-lookup"><span data-stu-id="1d971-142">The parameters declaration for policy definition.</span></span> <span data-ttu-id="1d971-143">Isso pode ser um caminho para um nome de arquivo ou URI que contém a declaração Parameters ou a declaração Parameters como cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="1d971-143">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="1d971-144">-Política</span><span class="sxs-lookup"><span data-stu-id="1d971-144">-Policy</span></span>
<span data-ttu-id="1d971-145">Especifica a nova regra de política para a definição de política.</span><span class="sxs-lookup"><span data-stu-id="1d971-145">Specifies new policy rule for the policy definition.</span></span>
<span data-ttu-id="1d971-146">Você pode especificar o caminho de um arquivo. JSON ou uma cadeia de caracteres que contém a política no formato JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="1d971-146">You can specify the path of a .json file or a string that contains the policy in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="1d971-147">-Pre</span><span class="sxs-lookup"><span data-stu-id="1d971-147">-Pre</span></span>
<span data-ttu-id="1d971-148">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="1d971-148">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="1d971-149">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1d971-149">-SubscriptionId</span></span>
<span data-ttu-id="1d971-150">A ID da assinatura da definição da política a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="1d971-150">The subscription ID of the policy definition to update.</span></span>

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

### <span data-ttu-id="1d971-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d971-151">CommonParameters</span></span>
<span data-ttu-id="1d971-152">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d971-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d971-153">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1d971-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d971-154">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1d971-154">INPUTS</span></span>

### <span data-ttu-id="1d971-155">System. String</span><span class="sxs-lookup"><span data-stu-id="1d971-155">System.String</span></span>

### <span data-ttu-id="1d971-156">System. Nullable ' 1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1d971-156">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="1d971-157">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1d971-157">OUTPUTS</span></span>

### <span data-ttu-id="1d971-158">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="1d971-158">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="1d971-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1d971-159">NOTES</span></span>

## <span data-ttu-id="1d971-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1d971-160">RELATED LINKS</span></span>

[<span data-ttu-id="1d971-161">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1d971-161">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="1d971-162">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1d971-162">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="1d971-163">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1d971-163">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)


