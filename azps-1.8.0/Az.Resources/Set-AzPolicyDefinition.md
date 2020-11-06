---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: E1AC7139-786C-4DD6-A898-242723E0D159
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
ms.openlocfilehash: f96ea5b7f36806378dff31cc81d211074638342c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599315"
---
# <span data-ttu-id="49e48-101">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="49e48-101">Set-AzPolicyDefinition</span></span>

## <span data-ttu-id="49e48-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="49e48-102">SYNOPSIS</span></span>
<span data-ttu-id="49e48-103">Modifica uma definição de política.</span><span class="sxs-lookup"><span data-stu-id="49e48-103">Modifies a policy definition.</span></span>

## <span data-ttu-id="49e48-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="49e48-104">SYNTAX</span></span>

### <span data-ttu-id="49e48-105">NameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="49e48-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49e48-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="49e48-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49e48-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="49e48-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -SubscriptionId <Guid> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49e48-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="49e48-108">IdParameterSet</span></span>
```
Set-AzPolicyDefinition -Id <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49e48-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="49e48-109">DESCRIPTION</span></span>
<span data-ttu-id="49e48-110">O cmdlet **set-AzPolicyDefinition** modifica uma definição de política.</span><span class="sxs-lookup"><span data-stu-id="49e48-110">The **Set-AzPolicyDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="49e48-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="49e48-111">EXAMPLES</span></span>

### <span data-ttu-id="49e48-112">Exemplo 1: atualizar a descrição de uma definição de política</span><span class="sxs-lookup"><span data-stu-id="49e48-112">Example 1: Update the description of a policy definition</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition'
PS C:\> Set-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="49e48-113">O primeiro comando obtém uma definição de política chamada VMPolicyDefinition usando o cmdlet Get-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="49e48-113">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="49e48-114">O comando armazena esse objeto na variável $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="49e48-114">The command stores that object in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="49e48-115">O segundo comando atualiza a descrição da definição de política identificada pela propriedade **ResourceId** de $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="49e48-115">The second command updates the description of the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

### <span data-ttu-id="49e48-116">Exemplo 2: atualizar o modo de uma definição de política</span><span class="sxs-lookup"><span data-stu-id="49e48-116">Example 2: Update the mode of a policy definition</span></span>
```
PS C:\> Set-AzPolicyDefinition -Name 'VMPolicyDefinition' -Mode 'All'
```

<span data-ttu-id="49e48-117">Esse comando atualiza a definição de política chamada VMPolicyDefinition usando o cmdlet Set-AzPolicyDefinition para definir a propriedade Mode como ' all'.</span><span class="sxs-lookup"><span data-stu-id="49e48-117">This command updates the policy definition named VMPolicyDefinition by using the Set-AzPolicyDefinition cmdlet to set its mode property to 'All'.</span></span>

## <span data-ttu-id="49e48-118">OS</span><span class="sxs-lookup"><span data-stu-id="49e48-118">PARAMETERS</span></span>

### <span data-ttu-id="49e48-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="49e48-119">-ApiVersion</span></span>
<span data-ttu-id="49e48-120">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="49e48-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="49e48-121">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="49e48-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="49e48-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49e48-122">-DefaultProfile</span></span>
<span data-ttu-id="49e48-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="49e48-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="49e48-124">-Descrição</span><span class="sxs-lookup"><span data-stu-id="49e48-124">-Description</span></span>
<span data-ttu-id="49e48-125">Especifica uma nova descrição para a definição de política.</span><span class="sxs-lookup"><span data-stu-id="49e48-125">Specifies a new description for the policy definition.</span></span>

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

### <span data-ttu-id="49e48-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="49e48-126">-DisplayName</span></span>
<span data-ttu-id="49e48-127">Especifica um novo nome de exibição para a definição de política.</span><span class="sxs-lookup"><span data-stu-id="49e48-127">Specifies a new display name for the policy definition.</span></span>

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

### <span data-ttu-id="49e48-128">-ID</span><span class="sxs-lookup"><span data-stu-id="49e48-128">-Id</span></span>
<span data-ttu-id="49e48-129">Especifica a ID de recurso totalmente qualificado para a definição de política que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="49e48-129">Specifies the fully qualified resource ID for the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="49e48-130">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="49e48-130">-ManagementGroupName</span></span>
<span data-ttu-id="49e48-131">O nome do grupo de gerenciamento da definição de política a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="49e48-131">The name of the management group of the policy definition to update.</span></span>

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

### <span data-ttu-id="49e48-132">-Metadados</span><span class="sxs-lookup"><span data-stu-id="49e48-132">-Metadata</span></span>
<span data-ttu-id="49e48-133">Os metadados da definição da política.</span><span class="sxs-lookup"><span data-stu-id="49e48-133">The metadata for policy definition.</span></span> <span data-ttu-id="49e48-134">Isso pode ser um caminho para um nome de arquivo que contém os metadados ou os metadados como cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="49e48-134">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

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

### <span data-ttu-id="49e48-135">-Mode</span><span class="sxs-lookup"><span data-stu-id="49e48-135">-Mode</span></span>
<span data-ttu-id="49e48-136">O modo da nova definição de política.</span><span class="sxs-lookup"><span data-stu-id="49e48-136">The mode of the new policy definition.</span></span>

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

### <span data-ttu-id="49e48-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="49e48-137">-Name</span></span>
<span data-ttu-id="49e48-138">Especifica o nome da definição de política que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="49e48-138">Specifies the name of the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="49e48-139">-Parâmetro</span><span class="sxs-lookup"><span data-stu-id="49e48-139">-Parameter</span></span>
<span data-ttu-id="49e48-140">A declaração Parameters para a definição da política.</span><span class="sxs-lookup"><span data-stu-id="49e48-140">The parameters declaration for policy definition.</span></span> <span data-ttu-id="49e48-141">Isso pode ser um caminho para um nome de arquivo ou URI que contém a declaração Parameters ou a declaração Parameters como cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="49e48-141">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="49e48-142">-Política</span><span class="sxs-lookup"><span data-stu-id="49e48-142">-Policy</span></span>
<span data-ttu-id="49e48-143">Especifica a nova regra de política para a definição de política.</span><span class="sxs-lookup"><span data-stu-id="49e48-143">Specifies new policy rule for the policy definition.</span></span>
<span data-ttu-id="49e48-144">Você pode especificar o caminho de um arquivo. JSON ou uma cadeia de caracteres que contém a política no formato JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="49e48-144">You can specify the path of a .json file or a string that contains the policy in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="49e48-145">-Pre</span><span class="sxs-lookup"><span data-stu-id="49e48-145">-Pre</span></span>
<span data-ttu-id="49e48-146">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="49e48-146">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="49e48-147">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="49e48-147">-SubscriptionId</span></span>
<span data-ttu-id="49e48-148">A ID da assinatura da definição da política a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="49e48-148">The subscription ID of the policy definition to update.</span></span>

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

### <span data-ttu-id="49e48-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49e48-149">CommonParameters</span></span>
<span data-ttu-id="49e48-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49e48-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49e48-151">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49e48-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49e48-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="49e48-152">INPUTS</span></span>

### <span data-ttu-id="49e48-153">System. String</span><span class="sxs-lookup"><span data-stu-id="49e48-153">System.String</span></span>

### <span data-ttu-id="49e48-154">System. Nullable ' 1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="49e48-154">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="49e48-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="49e48-155">OUTPUTS</span></span>

### <span data-ttu-id="49e48-156">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="49e48-156">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="49e48-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="49e48-157">NOTES</span></span>

## <span data-ttu-id="49e48-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="49e48-158">RELATED LINKS</span></span>

[<span data-ttu-id="49e48-159">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="49e48-159">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="49e48-160">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="49e48-160">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="49e48-161">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="49e48-161">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)


