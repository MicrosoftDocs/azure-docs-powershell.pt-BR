---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-Azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Update-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Update-AzADServicePrincipal.md
ms.openlocfilehash: e2c8e8fea9f8f86f06a9808158c50cb63915106b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776295"
---
# <span data-ttu-id="1f26b-101">Update-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="1f26b-101">Update-AzADServicePrincipal</span></span>

## <span data-ttu-id="1f26b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1f26b-102">SYNOPSIS</span></span>
<span data-ttu-id="1f26b-103">Atualiza uma entidade de serviço existente do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1f26b-103">Updates an existing azure active directory service principal.</span></span>

## <span data-ttu-id="1f26b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1f26b-104">SYNTAX</span></span>

### <span data-ttu-id="1f26b-105">SpObjectIdWithDisplayNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="1f26b-105">SpObjectIdWithDisplayNameParameterSet (Default)</span></span>
```
Update-AzADServicePrincipal -ObjectId <Guid> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f26b-106">SpApplicationIdWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f26b-106">SpApplicationIdWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -ApplicationId <Guid> [-Homepage <String>] [-IdentifierUri <String[]>]
 [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f26b-107">SPNWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f26b-107">SPNWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -ServicePrincipalName <String> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f26b-108">InputObjectWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f26b-108">InputObjectWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -InputObject <PSADServicePrincipal> [-DisplayName <String>]
 [-Homepage <String>] [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>]
 [-PasswordCredential <PasswordCredential[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1f26b-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1f26b-109">DESCRIPTION</span></span>
<span data-ttu-id="1f26b-110">Atualiza uma entidade de serviço existente do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1f26b-110">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="1f26b-111">Para atualizar as credenciais associadas a essa entidade de serviço, use o cmdlet New-AzADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="1f26b-111">To update the credentials associated with this service principal, please use New-AzADSpCredential cmdlet.</span></span> <span data-ttu-id="1f26b-112">Para atualizar as propriedades associadas ao aplicativo subjacente, use Update-AzADApplication cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f26b-112">To update the properties associated with the underlying application, please use Update-AzADApplication cmdlet.</span></span>

## <span data-ttu-id="1f26b-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1f26b-113">EXAMPLES</span></span>

### <span data-ttu-id="1f26b-114">Exemplo 1-atualize o nome de exibição de uma entidade de serviço</span><span class="sxs-lookup"><span data-stu-id="1f26b-114">Example 1 - Update the display name of a service principal</span></span>

```
PS C:\> Update-AzADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 -DisplayName MyNewDisplayName
```

<span data-ttu-id="1f26b-115">Atualiza o nome de exibição da entidade de serviço com a ID de objeto ' 784136ca-3ae2-4fdd-A388-89d793e7c780 ' para ser ' MyNewDisplayName '.</span><span class="sxs-lookup"><span data-stu-id="1f26b-115">Updates the display name of the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="1f26b-116">Exemplo 2-Atualize o nome de exibição de uma entidade de serviço usando o encanamento</span><span class="sxs-lookup"><span data-stu-id="1f26b-116">Example 2 - Update the display name of a service principal using piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 | Update-AzADServicePrincipal -DisplayName MyNewDisplayName
```

<span data-ttu-id="1f26b-117">Obtém a entidade de serviço com a ID de objeto ' 784136ca-3ae2-4fdd-A388-89d793e7c780 ' e canaliza-a para o cmdlet Update-AzADServicePrincipal para atualizar o nome de exibição da entidade de serviço para "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="1f26b-117">Gets the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' and pipes that to the Update-AzADServicePrincipal cmdlet to update the display name of the service principal to "MyNewDisplayName".</span></span>

## <span data-ttu-id="1f26b-118">OS</span><span class="sxs-lookup"><span data-stu-id="1f26b-118">PARAMETERS</span></span>

### <span data-ttu-id="1f26b-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="1f26b-119">-ApplicationId</span></span>
<span data-ttu-id="1f26b-120">A ID do aplicativo da entidade de serviço a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="1f26b-120">The application id of the service principal to update.</span></span>

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

### <span data-ttu-id="1f26b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f26b-121">-DefaultProfile</span></span>
<span data-ttu-id="1f26b-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1f26b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f26b-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="1f26b-123">-DisplayName</span></span>
<span data-ttu-id="1f26b-124">O nome de exibição para a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="1f26b-124">The display name for the service principal.</span></span>

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

### <span data-ttu-id="1f26b-125">-Página inicial</span><span class="sxs-lookup"><span data-stu-id="1f26b-125">-Homepage</span></span>
<span data-ttu-id="1f26b-126">A Home Page da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="1f26b-126">The homepage for the service principal.</span></span>

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

### <span data-ttu-id="1f26b-127">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="1f26b-127">-IdentifierUri</span></span>
<span data-ttu-id="1f26b-128">O (s) URI (s) identificadores para a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="1f26b-128">The identifier URI(s) for the service principal.</span></span>

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

### <span data-ttu-id="1f26b-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1f26b-129">-InputObject</span></span>
<span data-ttu-id="1f26b-130">O objeto que representa a entidade de serviço a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="1f26b-130">The object representing the service principal to update.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal
Parameter Sets: InputObjectWithDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1f26b-131">-Keycredential</span><span class="sxs-lookup"><span data-stu-id="1f26b-131">-KeyCredential</span></span>
<span data-ttu-id="1f26b-132">A (s) credencial (s) chave (is) para a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="1f26b-132">The key credential(s) for the service principal.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.Models.KeyCredential[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f26b-133">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="1f26b-133">-ObjectId</span></span>
<span data-ttu-id="1f26b-134">A ID de objeto da entidade de serviço a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="1f26b-134">The object id of the service principal to update.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SpObjectIdWithDisplayNameParameterSet
Aliases: ServicePrincipalObjectId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f26b-135">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="1f26b-135">-PasswordCredential</span></span>
<span data-ttu-id="1f26b-136">A (s) credencial (s) senha (s) para a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="1f26b-136">The password credential(s) for the service principal.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.Models.PasswordCredential[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f26b-137">-Serviceprincipalnamename</span><span class="sxs-lookup"><span data-stu-id="1f26b-137">-ServicePrincipalName</span></span>
<span data-ttu-id="1f26b-138">O SPN da entidade de serviço a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="1f26b-138">The SPN of the service principal to update.</span></span>

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

### <span data-ttu-id="1f26b-139">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1f26b-139">-Confirm</span></span>
<span data-ttu-id="1f26b-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f26b-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f26b-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f26b-141">-WhatIf</span></span>
<span data-ttu-id="1f26b-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1f26b-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f26b-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1f26b-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f26b-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f26b-144">CommonParameters</span></span>
<span data-ttu-id="1f26b-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f26b-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f26b-146">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f26b-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f26b-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1f26b-147">INPUTS</span></span>

### <span data-ttu-id="1f26b-148">System. GUID</span><span class="sxs-lookup"><span data-stu-id="1f26b-148">System.Guid</span></span>

### <span data-ttu-id="1f26b-149">System. String</span><span class="sxs-lookup"><span data-stu-id="1f26b-149">System.String</span></span>

### <span data-ttu-id="1f26b-150">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="1f26b-150">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>
<span data-ttu-id="1f26b-151">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1f26b-151">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="1f26b-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1f26b-152">OUTPUTS</span></span>

### <span data-ttu-id="1f26b-153">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="1f26b-153">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="1f26b-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1f26b-154">NOTES</span></span>

## <span data-ttu-id="1f26b-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1f26b-155">RELATED LINKS</span></span>
