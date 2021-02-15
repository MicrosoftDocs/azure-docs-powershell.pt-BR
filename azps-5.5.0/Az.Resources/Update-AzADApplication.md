---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADApplication.md
ms.openlocfilehash: c4754ecf8cae06fd43f57bc50d3b3fbeaf1d5081
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118726"
---
# <span data-ttu-id="cbac0-101">Update-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="cbac0-101">Update-AzADApplication</span></span>

## <span data-ttu-id="cbac0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cbac0-102">SYNOPSIS</span></span>
<span data-ttu-id="cbac0-103">Atualiza um aplicativo existente do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="cbac0-103">Updates an existing azure active directory application.</span></span>

## <span data-ttu-id="cbac0-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cbac0-104">SYNTAX</span></span>

### <span data-ttu-id="cbac0-105">ApplicationObjectIdWithUpdateParamsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="cbac0-105">ApplicationObjectIdWithUpdateParamsParameterSet (Default)</span></span>
```
Update-AzADApplication -ObjectId <String> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbac0-106">ApplicationIdWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="cbac0-106">ApplicationIdWithUpdateParamsParameterSet</span></span>
```
Update-AzADApplication -ApplicationId <Guid> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbac0-107">InputObjectWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="cbac0-107">InputObjectWithUpdateParamsParameterSet</span></span>
```
Update-AzADApplication -InputObject <PSADApplication> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cbac0-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="cbac0-108">DESCRIPTION</span></span>
<span data-ttu-id="cbac0-109">Atualiza um aplicativo existente do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="cbac0-109">Updates an existing azure active directory application.</span></span>
<span data-ttu-id="cbac0-110">Para atualizar as credenciais associadas a este aplicativo, use o cmdlet New-AzADAppCredential dados.</span><span class="sxs-lookup"><span data-stu-id="cbac0-110">To update the credentials associated with this application, please use the New-AzADAppCredential cmdlet.</span></span>

## <span data-ttu-id="cbac0-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="cbac0-111">EXAMPLES</span></span>

### <span data-ttu-id="cbac0-112">Exemplo 1 - Atualizar o nome de exibição de um aplicativo</span><span class="sxs-lookup"><span data-stu-id="cbac0-112">Example 1 - Update the display name of an application</span></span>

```
PS C:\> Update-AzADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName MyNewDisplayName
```

<span data-ttu-id="cbac0-113">Atualiza o nome de exibição do aplicativo com a ID do objeto 'fb7b3405-ca44-4b5b-8584-12392f5d96d7' como 'MeuNewDisplayName'.</span><span class="sxs-lookup"><span data-stu-id="cbac0-113">Updates the display name of the application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="cbac0-114">Exemplo 2 - Atualizar todas as propriedades de um aplicativo</span><span class="sxs-lookup"><span data-stu-id="cbac0-114">Example 2 - Update all properties of an application</span></span>

```
PS C:\> Update-AzADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName MyNewDisplayName -HomePage https://www.microsoft.com -IdentifierUris "https://UpdateAppUri"
```

<span data-ttu-id="cbac0-115">Atualiza as propriedades de um aplicativo com a ID do objeto 'fb7b3405-ca44-4b5b-8584-12392f5d96d7'.</span><span class="sxs-lookup"><span data-stu-id="cbac0-115">Updates the properties of an application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7'.</span></span>

### <span data-ttu-id="cbac0-116">Exemplo 3 - Atualizar o nome de exibição de um aplicativo usando a cana</span><span class="sxs-lookup"><span data-stu-id="cbac0-116">Example 3 - Update the display name of an application using piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 | Update-AzADApplication -DisplayName MyNewDisplayName
```

<span data-ttu-id="cbac0-117">Obtém o aplicativo com a ID do objeto 'fb7b3405-ca44-4b5b-8584-12392f5d96d7' e canos que para o cmdlet Update-AzADApplication para atualizar o nome de exibição do aplicativo para "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="cbac0-117">Gets the application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7' and pipes that to the Update-AzADApplication cmdlet to update the display name of the application to "MyNewDisplayName".</span></span>

## <span data-ttu-id="cbac0-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cbac0-118">PARAMETERS</span></span>

### <span data-ttu-id="cbac0-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="cbac0-119">-ApplicationId</span></span>
<span data-ttu-id="cbac0-120">A ID do aplicativo a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="cbac0-120">The application id of the application to update.</span></span>

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

### <span data-ttu-id="cbac0-121">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="cbac0-121">-AvailableToOtherTenants</span></span>
<span data-ttu-id="cbac0-122">Verdadeiro se o aplicativo for compartilhado com outros locatários; caso contrário, falso.</span><span class="sxs-lookup"><span data-stu-id="cbac0-122">True if the application is shared with other tenants; otherwise, false.</span></span>

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

### <span data-ttu-id="cbac0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbac0-123">-DefaultProfile</span></span>
<span data-ttu-id="cbac0-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cbac0-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbac0-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="cbac0-125">-DisplayName</span></span>
<span data-ttu-id="cbac0-126">O nome de exibição do aplicativo a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="cbac0-126">The display name for the application to update.</span></span>

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

### <span data-ttu-id="cbac0-127">-HomePage</span><span class="sxs-lookup"><span data-stu-id="cbac0-127">-HomePage</span></span>
<span data-ttu-id="cbac0-128">A URL para a home page do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cbac0-128">The URL to the application's homepage.</span></span>

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

### <span data-ttu-id="cbac0-129">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="cbac0-129">-IdentifierUri</span></span>
<span data-ttu-id="cbac0-130">As URIs que identificam o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cbac0-130">The URIs that identify the application.</span></span>

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

### <span data-ttu-id="cbac0-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cbac0-131">-InputObject</span></span>
<span data-ttu-id="cbac0-132">O objeto que representa o aplicativo a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="cbac0-132">The object representing the application to update.</span></span>

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

### <span data-ttu-id="cbac0-133">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="cbac0-133">-ObjectId</span></span>
<span data-ttu-id="cbac0-134">A ID do objeto do aplicativo a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="cbac0-134">The object id of the application to update.</span></span>

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

### <span data-ttu-id="cbac0-135">-ReplyUrl</span><span class="sxs-lookup"><span data-stu-id="cbac0-135">-ReplyUrl</span></span>
<span data-ttu-id="cbac0-136">Especifica as URLs para as que os tokens de usuário são enviados para entrar ou as URIs de redirecionamento para as que os códigos de autorização e tokens de acesso do OAuth 2.0 são enviados.</span><span class="sxs-lookup"><span data-stu-id="cbac0-136">Specifies the URLs that user tokens are sent to for sign in, or the redirect URIs that OAuth 2.0 authorization codes and access tokens are sent to.</span></span>

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

### <span data-ttu-id="cbac0-137">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="cbac0-137">-Confirm</span></span>
<span data-ttu-id="cbac0-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cbac0-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbac0-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbac0-139">-WhatIf</span></span>
<span data-ttu-id="cbac0-140">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="cbac0-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cbac0-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cbac0-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbac0-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbac0-142">CommonParameters</span></span>
<span data-ttu-id="cbac0-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbac0-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbac0-144">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cbac0-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbac0-145">Entradas</span><span class="sxs-lookup"><span data-stu-id="cbac0-145">INPUTS</span></span>

### <span data-ttu-id="cbac0-146">System.String</span><span class="sxs-lookup"><span data-stu-id="cbac0-146">System.String</span></span>

### <span data-ttu-id="cbac0-147">System.Guid</span><span class="sxs-lookup"><span data-stu-id="cbac0-147">System.Guid</span></span>

### <span data-ttu-id="cbac0-148">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="cbac0-148">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="cbac0-149">System.String[]</span><span class="sxs-lookup"><span data-stu-id="cbac0-149">System.String[]</span></span>

### <span data-ttu-id="cbac0-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cbac0-150">System.Boolean</span></span>

## <span data-ttu-id="cbac0-151">Saídas</span><span class="sxs-lookup"><span data-stu-id="cbac0-151">OUTPUTS</span></span>

### <span data-ttu-id="cbac0-152">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="cbac0-152">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="cbac0-153">Notas</span><span class="sxs-lookup"><span data-stu-id="cbac0-153">NOTES</span></span>

## <span data-ttu-id="cbac0-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cbac0-154">RELATED LINKS</span></span>
