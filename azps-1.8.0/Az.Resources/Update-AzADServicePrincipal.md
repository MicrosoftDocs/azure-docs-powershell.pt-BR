---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADServicePrincipal.md
ms.openlocfilehash: e4fafb6c1ddc4dda05b6536501f713d04c312172
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599292"
---
# <span data-ttu-id="e9038-101">Update-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e9038-101">Update-AzADServicePrincipal</span></span>

## <span data-ttu-id="e9038-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e9038-102">SYNOPSIS</span></span>
<span data-ttu-id="e9038-103">Atualiza uma entidade de serviço existente do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e9038-103">Updates an existing azure active directory service principal.</span></span>

## <span data-ttu-id="e9038-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e9038-104">SYNTAX</span></span>

### <span data-ttu-id="e9038-105">SpObjectIdWithDisplayNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="e9038-105">SpObjectIdWithDisplayNameParameterSet (Default)</span></span>
```
Update-AzADServicePrincipal -ObjectId <String> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9038-106">SpApplicationIdWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9038-106">SpApplicationIdWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -ApplicationId <Guid> [-Homepage <String>] [-IdentifierUri <String[]>]
 [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9038-107">SPNWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9038-107">SPNWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -ServicePrincipalName <String> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9038-108">InputObjectWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9038-108">InputObjectWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -InputObject <PSADServicePrincipal> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9038-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e9038-109">DESCRIPTION</span></span>
<span data-ttu-id="e9038-110">Atualiza uma entidade de serviço existente do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e9038-110">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="e9038-111">Para atualizar as credenciais associadas a essa entidade de serviço, use o cmdlet New-AzADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="e9038-111">To update the credentials associated with this service principal, please use New-AzADSpCredential cmdlet.</span></span> <span data-ttu-id="e9038-112">Para atualizar as propriedades associadas ao aplicativo subjacente, use Update-AzADApplication cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9038-112">To update the properties associated with the underlying application, please use Update-AzADApplication cmdlet.</span></span>

## <span data-ttu-id="e9038-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e9038-113">EXAMPLES</span></span>

### <span data-ttu-id="e9038-114">Exemplo 1-atualize o nome de exibição de uma entidade de serviço</span><span class="sxs-lookup"><span data-stu-id="e9038-114">Example 1 - Update the display name of a service principal</span></span>

```
PS C:\> Update-AzADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 -DisplayName MyNewDisplayName
```

<span data-ttu-id="e9038-115">Atualiza o nome de exibição da entidade de serviço com a ID de objeto ' 784136ca-3ae2-4fdd-A388-89d793e7c780 ' para ser ' MyNewDisplayName '.</span><span class="sxs-lookup"><span data-stu-id="e9038-115">Updates the display name of the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="e9038-116">Exemplo 2-Atualize o nome de exibição de uma entidade de serviço usando o encanamento</span><span class="sxs-lookup"><span data-stu-id="e9038-116">Example 2 - Update the display name of a service principal using piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 | Update-AzADServicePrincipal -DisplayName MyNewDisplayName
```

<span data-ttu-id="e9038-117">Obtém a entidade de serviço com a ID de objeto ' 784136ca-3ae2-4fdd-A388-89d793e7c780 ' e canaliza-a para o cmdlet Update-AzADServicePrincipal para atualizar o nome de exibição da entidade de serviço para "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="e9038-117">Gets the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' and pipes that to the Update-AzADServicePrincipal cmdlet to update the display name of the service principal to "MyNewDisplayName".</span></span>

## <span data-ttu-id="e9038-118">OS</span><span class="sxs-lookup"><span data-stu-id="e9038-118">PARAMETERS</span></span>

### <span data-ttu-id="e9038-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="e9038-119">-ApplicationId</span></span>
<span data-ttu-id="e9038-120">A ID do aplicativo da entidade de serviço a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="e9038-120">The application id of the service principal to update.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SpApplicationIdWithDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9038-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9038-121">-DefaultProfile</span></span>
<span data-ttu-id="e9038-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e9038-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9038-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e9038-123">-DisplayName</span></span>
<span data-ttu-id="e9038-124">O nome de exibição para a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="e9038-124">The display name for the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: SpObjectIdWithDisplayNameParameterSet, SPNWithDisplayNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObjectWithDisplayNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9038-125">-Página inicial</span><span class="sxs-lookup"><span data-stu-id="e9038-125">-Homepage</span></span>
<span data-ttu-id="e9038-126">A Home Page da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="e9038-126">The homepage for the service principal.</span></span>

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

### <span data-ttu-id="e9038-127">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="e9038-127">-IdentifierUri</span></span>
<span data-ttu-id="e9038-128">O (s) URI (s) identificadores para a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="e9038-128">The identifier URI(s) for the service principal.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9038-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e9038-129">-InputObject</span></span>
<span data-ttu-id="e9038-130">O objeto que representa a entidade de serviço a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="e9038-130">The object representing the service principal to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal
Parameter Sets: InputObjectWithDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e9038-131">-Keycredential</span><span class="sxs-lookup"><span data-stu-id="e9038-131">-KeyCredential</span></span>
<span data-ttu-id="e9038-132">A (s) credencial (s) chave (is) para a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="e9038-132">The key credential(s) for the service principal.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Models.KeyCredential[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9038-133">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="e9038-133">-ObjectId</span></span>
<span data-ttu-id="e9038-134">A ID de objeto da entidade de serviço a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="e9038-134">The object id of the service principal to update.</span></span>

```yaml
Type: System.String
Parameter Sets: SpObjectIdWithDisplayNameParameterSet
Aliases: ServicePrincipalObjectId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9038-135">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="e9038-135">-PasswordCredential</span></span>
<span data-ttu-id="e9038-136">A (s) credencial (s) senha (s) para a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="e9038-136">The password credential(s) for the service principal.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Models.PasswordCredential[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9038-137">-Serviceprincipalnamename</span><span class="sxs-lookup"><span data-stu-id="e9038-137">-ServicePrincipalName</span></span>
<span data-ttu-id="e9038-138">O SPN da entidade de serviço a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="e9038-138">The SPN of the service principal to update.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNWithDisplayNameParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9038-139">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e9038-139">-Confirm</span></span>
<span data-ttu-id="e9038-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9038-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9038-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9038-141">-WhatIf</span></span>
<span data-ttu-id="e9038-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e9038-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9038-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e9038-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9038-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9038-144">CommonParameters</span></span>
<span data-ttu-id="e9038-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9038-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9038-146">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9038-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9038-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e9038-147">INPUTS</span></span>

### <span data-ttu-id="e9038-148">System. String</span><span class="sxs-lookup"><span data-stu-id="e9038-148">System.String</span></span>

### <span data-ttu-id="e9038-149">System. GUID</span><span class="sxs-lookup"><span data-stu-id="e9038-149">System.Guid</span></span>

### <span data-ttu-id="e9038-150">Microsoft. Azure. Commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e9038-150">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="e9038-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e9038-151">OUTPUTS</span></span>

### <span data-ttu-id="e9038-152">Microsoft. Azure. Commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e9038-152">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="e9038-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e9038-153">NOTES</span></span>

## <span data-ttu-id="e9038-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e9038-154">RELATED LINKS</span></span>
