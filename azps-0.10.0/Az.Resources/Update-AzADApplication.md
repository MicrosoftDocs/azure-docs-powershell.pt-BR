---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-Azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Update-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Update-AzADApplication.md
ms.openlocfilehash: 8eb01ccfa16b1d3610468f98117ee650376d4b6c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776300"
---
# <span data-ttu-id="6fd04-101">Update-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="6fd04-101">Update-AzADApplication</span></span>

## <span data-ttu-id="6fd04-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6fd04-102">SYNOPSIS</span></span>
<span data-ttu-id="6fd04-103">Atualiza um aplicativo existente do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6fd04-103">Updates an existing azure active directory application.</span></span>

## <span data-ttu-id="6fd04-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6fd04-104">SYNTAX</span></span>

### <span data-ttu-id="6fd04-105">ApplicationObjectIdWithUpdateParamsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="6fd04-105">ApplicationObjectIdWithUpdateParamsParameterSet (Default)</span></span>
```
Update-AzADApplication -ObjectId <Guid> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fd04-106">ApplicationIdWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fd04-106">ApplicationIdWithUpdateParamsParameterSet</span></span>
```
Update-AzADApplication -ApplicationId <Guid> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fd04-107">InputObjectWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fd04-107">InputObjectWithUpdateParamsParameterSet</span></span>
```
Update-AzADApplication -InputObject <PSADApplication> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6fd04-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6fd04-108">DESCRIPTION</span></span>
<span data-ttu-id="6fd04-109">Atualiza um aplicativo existente do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6fd04-109">Updates an existing azure active directory application.</span></span>
<span data-ttu-id="6fd04-110">Para atualizar as credenciais associadas a esse aplicativo, use o cmdlet New-AzADAppCredential.</span><span class="sxs-lookup"><span data-stu-id="6fd04-110">To update the credentials associated with this application, please use the New-AzADAppCredential cmdlet.</span></span>

## <span data-ttu-id="6fd04-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6fd04-111">EXAMPLES</span></span>

### <span data-ttu-id="6fd04-112">Exemplo 1-atualize o nome de exibição de um aplicativo</span><span class="sxs-lookup"><span data-stu-id="6fd04-112">Example 1 - Update the display name of an application</span></span>

```
PS C:\> Update-AzADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName MyNewDisplayName
```

<span data-ttu-id="6fd04-113">Atualiza o nome de exibição do aplicativo com a ID de objeto ' fb7b3405-ca44-4B5B-8584-12392f5d96d7 ' para ser ' MyNewDisplayName '.</span><span class="sxs-lookup"><span data-stu-id="6fd04-113">Updates the display name of the application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="6fd04-114">Exemplo 2 – atualizar todas as propriedades de um aplicativo</span><span class="sxs-lookup"><span data-stu-id="6fd04-114">Example 2 - Update all properties of an application</span></span>

```
PS C:\> Update-AzADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName MyNewDisplayName -HomePage https://www.microsoft.com -IdentifierUris "https://UpdateAppUri"
```

<span data-ttu-id="6fd04-115">Atualiza as propriedades de um aplicativo com a ID de objeto ' fb7b3405-ca44-4B5B-8584-12392f5d96d7 '.</span><span class="sxs-lookup"><span data-stu-id="6fd04-115">Updates the properties of an application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7'.</span></span>

### <span data-ttu-id="6fd04-116">Exemplo 3-atualize o nome de exibição de um aplicativo usando o encanamento</span><span class="sxs-lookup"><span data-stu-id="6fd04-116">Example 3 - Update the display name of an application using piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 | Update-AzADApplication -DisplayName MyNewDisplayName
```

<span data-ttu-id="6fd04-117">Obtém o aplicativo com a ID de objeto ' fb7b3405-ca44-4B5B-8584-12392f5d96d7 ' e canaliza-o para o cmdlet Update-AzADApplication para atualizar o nome de exibição do aplicativo para "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="6fd04-117">Gets the application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7' and pipes that to the Update-AzADApplication cmdlet to update the display name of the application to "MyNewDisplayName".</span></span>

## <span data-ttu-id="6fd04-118">OS</span><span class="sxs-lookup"><span data-stu-id="6fd04-118">PARAMETERS</span></span>

### <span data-ttu-id="6fd04-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="6fd04-119">-ApplicationId</span></span>
<span data-ttu-id="6fd04-120">A ID do aplicativo a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="6fd04-120">The application id of the application to update.</span></span>

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

### <span data-ttu-id="6fd04-121">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="6fd04-121">-AvailableToOtherTenants</span></span>
<span data-ttu-id="6fd04-122">Verdadeiro se o aplicativo for compartilhado com outros locatários; caso contrário, false.</span><span class="sxs-lookup"><span data-stu-id="6fd04-122">True if the application is shared with other tenants; otherwise, false.</span></span>

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

### <span data-ttu-id="6fd04-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fd04-123">-DefaultProfile</span></span>
<span data-ttu-id="6fd04-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6fd04-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fd04-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="6fd04-125">-DisplayName</span></span>
<span data-ttu-id="6fd04-126">O nome de exibição do aplicativo a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="6fd04-126">The display name for the application to update.</span></span>

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

### <span data-ttu-id="6fd04-127">-Página inicial</span><span class="sxs-lookup"><span data-stu-id="6fd04-127">-HomePage</span></span>
<span data-ttu-id="6fd04-128">A URL para a página inicial do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6fd04-128">The URL to the application's homepage.</span></span>

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

### <span data-ttu-id="6fd04-129">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="6fd04-129">-IdentifierUri</span></span>
<span data-ttu-id="6fd04-130">Os URIs que identificam o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6fd04-130">The URIs that identify the application.</span></span>

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

### <span data-ttu-id="6fd04-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6fd04-131">-InputObject</span></span>
<span data-ttu-id="6fd04-132">O objeto que representa o aplicativo a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="6fd04-132">The object representing the application to update.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6fd04-133">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="6fd04-133">-ObjectId</span></span>
<span data-ttu-id="6fd04-134">A ID de objeto do aplicativo a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="6fd04-134">The object id of the application to update.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fd04-135">-ReplyUrl</span><span class="sxs-lookup"><span data-stu-id="6fd04-135">-ReplyUrl</span></span>
<span data-ttu-id="6fd04-136">Especifica as URLs às quais os tokens de usuário são enviados para entrar ou os URIs de redirecionamento dos quais códigos de autorização OAuth 2,0 e tokens de acesso são enviados.</span><span class="sxs-lookup"><span data-stu-id="6fd04-136">Specifies the URLs that user tokens are sent to for sign in, or the redirect URIs that OAuth 2.0 authorization codes and access tokens are sent to.</span></span>

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

### <span data-ttu-id="6fd04-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6fd04-137">-Confirm</span></span>
<span data-ttu-id="6fd04-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6fd04-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fd04-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fd04-139">-WhatIf</span></span>
<span data-ttu-id="6fd04-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6fd04-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6fd04-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6fd04-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fd04-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fd04-142">CommonParameters</span></span>
<span data-ttu-id="6fd04-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fd04-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fd04-144">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fd04-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fd04-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6fd04-145">INPUTS</span></span>

### <span data-ttu-id="6fd04-146">System. GUID</span><span class="sxs-lookup"><span data-stu-id="6fd04-146">System.Guid</span></span>

### <span data-ttu-id="6fd04-147">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="6fd04-147">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="6fd04-148">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6fd04-148">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="6fd04-149">System. String</span><span class="sxs-lookup"><span data-stu-id="6fd04-149">System.String</span></span>

### <span data-ttu-id="6fd04-150">System. String []</span><span class="sxs-lookup"><span data-stu-id="6fd04-150">System.String[]</span></span>

### <span data-ttu-id="6fd04-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6fd04-151">System.Boolean</span></span>

## <span data-ttu-id="6fd04-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6fd04-152">OUTPUTS</span></span>

### <span data-ttu-id="6fd04-153">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="6fd04-153">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="6fd04-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6fd04-154">NOTES</span></span>

## <span data-ttu-id="6fd04-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6fd04-155">RELATED LINKS</span></span>
