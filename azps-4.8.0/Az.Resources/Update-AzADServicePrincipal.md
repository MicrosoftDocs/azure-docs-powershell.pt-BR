---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADServicePrincipal.md
ms.openlocfilehash: 4a4888573199c4fd5f76282fb5c8eb1702911e00
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93947645"
---
# <span data-ttu-id="15e32-101">Update-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="15e32-101">Update-AzADServicePrincipal</span></span>

## <span data-ttu-id="15e32-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="15e32-102">SYNOPSIS</span></span>
<span data-ttu-id="15e32-103">Atualiza uma entidade de serviço existente do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="15e32-103">Updates an existing azure active directory service principal.</span></span>

## <span data-ttu-id="15e32-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="15e32-104">SYNTAX</span></span>

### <span data-ttu-id="15e32-105">SpObjectIdWithDisplayNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="15e32-105">SpObjectIdWithDisplayNameParameterSet (Default)</span></span>
```
Update-AzADServicePrincipal -ObjectId <String> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15e32-106">SpApplicationIdWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="15e32-106">SpApplicationIdWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -ApplicationId <Guid> [-Homepage <String>] [-IdentifierUri <String[]>]
 [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15e32-107">SPNWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="15e32-107">SPNWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -ServicePrincipalName <String> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15e32-108">InputObjectWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="15e32-108">InputObjectWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -InputObject <PSADServicePrincipal> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15e32-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="15e32-109">DESCRIPTION</span></span>
<span data-ttu-id="15e32-110">Atualiza uma entidade de serviço existente do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="15e32-110">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="15e32-111">Para atualizar as credenciais associadas a essa entidade de serviço, use o cmdlet New-AzADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="15e32-111">To update the credentials associated with this service principal, please use New-AzADSpCredential cmdlet.</span></span> <span data-ttu-id="15e32-112">Para atualizar as propriedades associadas ao aplicativo subjacente, use Update-AzADApplication cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15e32-112">To update the properties associated with the underlying application, please use Update-AzADApplication cmdlet.</span></span>

## <span data-ttu-id="15e32-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="15e32-113">EXAMPLES</span></span>

### <span data-ttu-id="15e32-114">Exemplo 1: atualizar o nome de exibição de uma entidade de serviço</span><span class="sxs-lookup"><span data-stu-id="15e32-114">Example 1: Update the display name of a service principal</span></span>

```powershell
PS C:\> Update-AzADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 -DisplayName MyNewDisplayName
```

<span data-ttu-id="15e32-115">Atualiza o nome de exibição da entidade de serviço com a ID de objeto ' 784136ca-3ae2-4fdd-A388-89d793e7c780 ' para ser ' MyNewDisplayName '.</span><span class="sxs-lookup"><span data-stu-id="15e32-115">Updates the display name of the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="15e32-116">Exemplo 2: atualizar o nome de exibição de uma entidade de serviço usando o encanamento</span><span class="sxs-lookup"><span data-stu-id="15e32-116">Example 2: Update the display name of a service principal using piping</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 | Update-AzADServicePrincipal -DisplayName MyNewDisplayName
```

<span data-ttu-id="15e32-117">Obtém a entidade de serviço com a ID de objeto ' 784136ca-3ae2-4fdd-A388-89d793e7c780 ' e canaliza-a para o cmdlet Update-AzADServicePrincipal para atualizar o nome de exibição da entidade de serviço para "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="15e32-117">Gets the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' and pipes that to the Update-AzADServicePrincipal cmdlet to update the display name of the service principal to "MyNewDisplayName".</span></span>

### <span data-ttu-id="15e32-118">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="15e32-118">Example 3</span></span>

<span data-ttu-id="15e32-119">Atualiza uma entidade de serviço existente do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="15e32-119">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="15e32-120">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="15e32-120">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Update-AzADServicePrincipal -IdentifierUri https://mySecretApp1 -ObjectId 00000000-0000-0000-0000-00000000000000000
```

## <span data-ttu-id="15e32-121">OS</span><span class="sxs-lookup"><span data-stu-id="15e32-121">PARAMETERS</span></span>

### <span data-ttu-id="15e32-122">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="15e32-122">-ApplicationId</span></span>
<span data-ttu-id="15e32-123">A ID do aplicativo da entidade de serviço a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="15e32-123">The application id of the service principal to update.</span></span>

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

### <span data-ttu-id="15e32-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15e32-124">-DefaultProfile</span></span>
<span data-ttu-id="15e32-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="15e32-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15e32-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="15e32-126">-DisplayName</span></span>
<span data-ttu-id="15e32-127">O nome de exibição para a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="15e32-127">The display name for the service principal.</span></span>

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

### <span data-ttu-id="15e32-128">-Página inicial</span><span class="sxs-lookup"><span data-stu-id="15e32-128">-Homepage</span></span>
<span data-ttu-id="15e32-129">A Home Page da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="15e32-129">The homepage for the service principal.</span></span>

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

### <span data-ttu-id="15e32-130">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="15e32-130">-IdentifierUri</span></span>
<span data-ttu-id="15e32-131">O (s) URI (s) identificadores para a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="15e32-131">The identifier URI(s) for the service principal.</span></span>

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

### <span data-ttu-id="15e32-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="15e32-132">-InputObject</span></span>
<span data-ttu-id="15e32-133">O objeto que representa a entidade de serviço a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="15e32-133">The object representing the service principal to update.</span></span>

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

### <span data-ttu-id="15e32-134">-Keycredential</span><span class="sxs-lookup"><span data-stu-id="15e32-134">-KeyCredential</span></span>
<span data-ttu-id="15e32-135">A (s) credencial (s) chave (is) para a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="15e32-135">The key credential(s) for the service principal.</span></span>

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

### <span data-ttu-id="15e32-136">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="15e32-136">-ObjectId</span></span>
<span data-ttu-id="15e32-137">A ID de objeto da entidade de serviço a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="15e32-137">The object id of the service principal to update.</span></span>

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

### <span data-ttu-id="15e32-138">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="15e32-138">-PasswordCredential</span></span>
<span data-ttu-id="15e32-139">A (s) credencial (s) senha (s) para a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="15e32-139">The password credential(s) for the service principal.</span></span>

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

### <span data-ttu-id="15e32-140">-Serviceprincipalnamename</span><span class="sxs-lookup"><span data-stu-id="15e32-140">-ServicePrincipalName</span></span>
<span data-ttu-id="15e32-141">O SPN da entidade de serviço a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="15e32-141">The SPN of the service principal to update.</span></span>

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

### <span data-ttu-id="15e32-142">-Confirme</span><span class="sxs-lookup"><span data-stu-id="15e32-142">-Confirm</span></span>
<span data-ttu-id="15e32-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15e32-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15e32-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15e32-144">-WhatIf</span></span>
<span data-ttu-id="15e32-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="15e32-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15e32-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="15e32-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15e32-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15e32-147">CommonParameters</span></span>
<span data-ttu-id="15e32-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15e32-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15e32-149">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="15e32-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15e32-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="15e32-150">INPUTS</span></span>

### <span data-ttu-id="15e32-151">System. String</span><span class="sxs-lookup"><span data-stu-id="15e32-151">System.String</span></span>

### <span data-ttu-id="15e32-152">System. GUID</span><span class="sxs-lookup"><span data-stu-id="15e32-152">System.Guid</span></span>

### <span data-ttu-id="15e32-153">Microsoft. Azure. Commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="15e32-153">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="15e32-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="15e32-154">OUTPUTS</span></span>

### <span data-ttu-id="15e32-155">Microsoft. Azure. Commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="15e32-155">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="15e32-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="15e32-156">NOTES</span></span>

## <span data-ttu-id="15e32-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="15e32-157">RELATED LINKS</span></span>
