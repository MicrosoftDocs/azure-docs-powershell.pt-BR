---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/update-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADApplication.md
ms.openlocfilehash: 329620701c4afb52bdebd145ef461c7d311c26a2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891257"
---
# <span data-ttu-id="00b13-101">Update-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="00b13-101">Update-AzADApplication</span></span>

## <span data-ttu-id="00b13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00b13-102">SYNOPSIS</span></span>
<span data-ttu-id="00b13-103">Atualiza um aplicativo existente do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="00b13-103">Updates an existing azure active directory application.</span></span>

## <span data-ttu-id="00b13-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="00b13-104">SYNTAX</span></span>

### <span data-ttu-id="00b13-105">ApplicationObjectIdWithUpdateParamsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="00b13-105">ApplicationObjectIdWithUpdateParamsParameterSet (Default)</span></span>
```
Update-AzADApplication -ObjectId <String> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00b13-106">ApplicationIdWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="00b13-106">ApplicationIdWithUpdateParamsParameterSet</span></span>
```
Update-AzADApplication -ApplicationId <Guid> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00b13-107">InputObjectWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="00b13-107">InputObjectWithUpdateParamsParameterSet</span></span>
```
Update-AzADApplication -InputObject <PSADApplication> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00b13-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="00b13-108">DESCRIPTION</span></span>
<span data-ttu-id="00b13-109">Atualiza um aplicativo existente do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="00b13-109">Updates an existing azure active directory application.</span></span>
<span data-ttu-id="00b13-110">Para atualizar as credenciais associadas a este aplicativo, use o cmdlet New-AzADAppCredential usuário.</span><span class="sxs-lookup"><span data-stu-id="00b13-110">To update the credentials associated with this application, please use the New-AzADAppCredential cmdlet.</span></span>

## <span data-ttu-id="00b13-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="00b13-111">EXAMPLES</span></span>

### <span data-ttu-id="00b13-112">Exemplo 1 - Atualizar o nome de exibição de um aplicativo</span><span class="sxs-lookup"><span data-stu-id="00b13-112">Example 1 - Update the display name of an application</span></span>

```
PS C:\> Update-AzADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName MyNewDisplayName
```

<span data-ttu-id="00b13-113">Atualiza o nome de exibição do aplicativo com a id do objeto 'fb7b3405-ca44-4b5b-8584-12392f5d96d7' como 'MyNewDisplayName'.</span><span class="sxs-lookup"><span data-stu-id="00b13-113">Updates the display name of the application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="00b13-114">Exemplo 2 - Atualizar todas as propriedades de um aplicativo</span><span class="sxs-lookup"><span data-stu-id="00b13-114">Example 2 - Update all properties of an application</span></span>

```
PS C:\> Update-AzADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName MyNewDisplayName -HomePage https://www.microsoft.com -IdentifierUris "https://UpdateAppUri"
```

<span data-ttu-id="00b13-115">Atualiza as propriedades de um aplicativo com a id do objeto 'fb7b3405-ca44-4b5b-8584-12392f5d96d7'.</span><span class="sxs-lookup"><span data-stu-id="00b13-115">Updates the properties of an application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7'.</span></span>

### <span data-ttu-id="00b13-116">Exemplo 3 - Atualizar o nome de exibição de um aplicativo usando a canalização</span><span class="sxs-lookup"><span data-stu-id="00b13-116">Example 3 - Update the display name of an application using piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 | Update-AzADApplication -DisplayName MyNewDisplayName
```

<span data-ttu-id="00b13-117">Obtém o aplicativo com a id do objeto 'fb7b3405-ca44-4b5b-8584-12392f5d96d7' e canaliza isso para o cmdlet Update-AzADApplication para atualizar o nome de exibição do aplicativo para "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="00b13-117">Gets the application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7' and pipes that to the Update-AzADApplication cmdlet to update the display name of the application to "MyNewDisplayName".</span></span>

## <span data-ttu-id="00b13-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="00b13-118">PARAMETERS</span></span>

### <span data-ttu-id="00b13-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="00b13-119">-ApplicationId</span></span>
<span data-ttu-id="00b13-120">A ID do aplicativo a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="00b13-120">The application id of the application to update.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdWithUpdateParamsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00b13-121">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="00b13-121">-AvailableToOtherTenants</span></span>
<span data-ttu-id="00b13-122">True se o aplicativo for compartilhado com outros locatários; caso contrário, false.</span><span class="sxs-lookup"><span data-stu-id="00b13-122">True if the application is shared with other tenants; otherwise, false.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet, ApplicationIdWithUpdateParamsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Boolean
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00b13-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00b13-123">-DefaultProfile</span></span>
<span data-ttu-id="00b13-124">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="00b13-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00b13-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="00b13-125">-DisplayName</span></span>
<span data-ttu-id="00b13-126">O nome de exibição do aplicativo a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="00b13-126">The display name for the application to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet, ApplicationIdWithUpdateParamsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00b13-127">-HomePage</span><span class="sxs-lookup"><span data-stu-id="00b13-127">-HomePage</span></span>
<span data-ttu-id="00b13-128">A URL da página inicial do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="00b13-128">The URL to the application's homepage.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet, ApplicationIdWithUpdateParamsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00b13-129">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="00b13-129">-IdentifierUri</span></span>
<span data-ttu-id="00b13-130">As URIs que identificam o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="00b13-130">The URIs that identify the application.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet, ApplicationIdWithUpdateParamsParameterSet
Aliases: IdentifierUris

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases: IdentifierUris

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00b13-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="00b13-131">-InputObject</span></span>
<span data-ttu-id="00b13-132">O objeto que representa o aplicativo a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="00b13-132">The object representing the application to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="00b13-133">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="00b13-133">-ObjectId</span></span>
<span data-ttu-id="00b13-134">A id do objeto do aplicativo a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="00b13-134">The object id of the application to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00b13-135">-ReplyUrl</span><span class="sxs-lookup"><span data-stu-id="00b13-135">-ReplyUrl</span></span>
<span data-ttu-id="00b13-136">Especifica as URLs às que os tokens de usuário são enviados para entrar ou os URIs de redirecionamento para os que os códigos de autorização do OAuth 2.0 e os tokens de acesso são enviados.</span><span class="sxs-lookup"><span data-stu-id="00b13-136">Specifies the URLs that user tokens are sent to for sign in, or the redirect URIs that OAuth 2.0 authorization codes and access tokens are sent to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet, ApplicationIdWithUpdateParamsParameterSet
Aliases: ReplyUrls

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases: ReplyUrls

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00b13-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="00b13-137">-Confirm</span></span>
<span data-ttu-id="00b13-138">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00b13-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00b13-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00b13-139">-WhatIf</span></span>
<span data-ttu-id="00b13-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="00b13-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00b13-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="00b13-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00b13-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00b13-142">CommonParameters</span></span>
<span data-ttu-id="00b13-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00b13-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00b13-144">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="00b13-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00b13-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="00b13-145">INPUTS</span></span>

### <span data-ttu-id="00b13-146">System.String</span><span class="sxs-lookup"><span data-stu-id="00b13-146">System.String</span></span>

### <span data-ttu-id="00b13-147">System.Guid</span><span class="sxs-lookup"><span data-stu-id="00b13-147">System.Guid</span></span>

### <span data-ttu-id="00b13-148">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="00b13-148">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="00b13-149">System.String[]</span><span class="sxs-lookup"><span data-stu-id="00b13-149">System.String[]</span></span>

### <span data-ttu-id="00b13-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="00b13-150">System.Boolean</span></span>

## <span data-ttu-id="00b13-151">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="00b13-151">OUTPUTS</span></span>

### <span data-ttu-id="00b13-152">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="00b13-152">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="00b13-153">NOTES</span><span class="sxs-lookup"><span data-stu-id="00b13-153">NOTES</span></span>

## <span data-ttu-id="00b13-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="00b13-154">RELATED LINKS</span></span>
