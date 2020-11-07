---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C61FA834-BEBE-4DBF-888F-C6CB8CC95390
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADAppCredential.md
ms.openlocfilehash: 94a6b1ed2d02e3072a23ccc82fc4a49149b2ae2e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776369"
---
# <span data-ttu-id="c7fb9-101">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="c7fb9-101">Remove-AzADAppCredential</span></span>

## <span data-ttu-id="c7fb9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c7fb9-102">SYNOPSIS</span></span>
<span data-ttu-id="c7fb9-103">Remove uma credencial de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c7fb9-103">Removes a credential from an application.</span></span>

## <span data-ttu-id="c7fb9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c7fb9-104">SYNTAX</span></span>

### <span data-ttu-id="c7fb9-105">ApplicationObjectIdWithKeyIdParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="c7fb9-105">ApplicationObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzADAppCredential -ObjectId <Guid> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7fb9-106">ApplicationIdWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7fb9-106">ApplicationIdWithKeyIdParameterSet</span></span>
```
Remove-AzADAppCredential -ApplicationId <Guid> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7fb9-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7fb9-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzADAppCredential -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7fb9-108">ApplicationObjectWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7fb9-108">ApplicationObjectWithKeyIdParameterSet</span></span>
```
Remove-AzADAppCredential [-KeyId <Guid>] -ApplicationObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7fb9-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c7fb9-109">DESCRIPTION</span></span>
<span data-ttu-id="c7fb9-110">O cmdlet Remove-AzADAppCredential pode ser usado para remover uma chave de credencial de um aplicativo no caso de um comprometimento ou como parte da expiração da sobreposição da chave da credencial.</span><span class="sxs-lookup"><span data-stu-id="c7fb9-110">The Remove-AzADAppCredential cmdlet can be used to remove a credential key from an application in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="c7fb9-111">O aplicativo é identificado fornecendo o ID do objeto ou AppId.</span><span class="sxs-lookup"><span data-stu-id="c7fb9-111">The application is identified by supplying either the object ID or AppId.</span></span>
<span data-ttu-id="c7fb9-112">A credencial a ser removida é identificada pela ID da chave.</span><span class="sxs-lookup"><span data-stu-id="c7fb9-112">The credential to be removed is identified by its key ID.</span></span>

## <span data-ttu-id="c7fb9-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c7fb9-113">EXAMPLES</span></span>

### <span data-ttu-id="c7fb9-114">Exemplo 1: remover uma credencial específica de um aplicativo</span><span class="sxs-lookup"><span data-stu-id="c7fb9-114">Example 1 - Remove a specific credential from an application</span></span>

```
PS C:\> Remove-AzADAppCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="c7fb9-115">Remove a credencial com a ID da chave ' 9044423a-60a3-45ac-9ab1-09534157ebb ' do aplicativo com a ID de objeto ' 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 '.</span><span class="sxs-lookup"><span data-stu-id="c7fb9-115">Removes the credential with key id '9044423a-60a3-45ac-9ab1-09534157ebb' from the application with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span></span>

### <span data-ttu-id="c7fb9-116">Exemplo 2-remover todas as credenciais de um aplicativo</span><span class="sxs-lookup"><span data-stu-id="c7fb9-116">Example 2 - Remove all credentials from an application</span></span>

```
PS C:\> Remove-AzADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58
```

<span data-ttu-id="c7fb9-117">Remove todas as credenciais do aplicativo com a ID de aplicativo ' 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 '.</span><span class="sxs-lookup"><span data-stu-id="c7fb9-117">Removes all credentials from the application with application id '4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58'.</span></span>

### <span data-ttu-id="c7fb9-118">Exemplo 3-remover todas as credenciais usando o encanamento</span><span class="sxs-lookup"><span data-stu-id="c7fb9-118">Example 3 - Remove all credentials using piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 | Remove-AzADAppCredential
```

<span data-ttu-id="c7fb9-119">Obtém o aplicativo com a ID de objeto ' 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 ' e canaliza-o para o cmdlet Remove-AzADAppCredential e remove todas as credenciais desse aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c7fb9-119">Gets the application with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82' and pipes that to the Remove-AzADAppCredential cmdlet and removes all credentials from that application.</span></span>

## <span data-ttu-id="c7fb9-120">OS</span><span class="sxs-lookup"><span data-stu-id="c7fb9-120">PARAMETERS</span></span>

### <span data-ttu-id="c7fb9-121">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="c7fb9-121">-ApplicationId</span></span>
<span data-ttu-id="c7fb9-122">A ID do aplicativo do qual as credenciais será removida.</span><span class="sxs-lookup"><span data-stu-id="c7fb9-122">The id of the application to remove the credentials from.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7fb9-123">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="c7fb9-123">-ApplicationObject</span></span>
<span data-ttu-id="c7fb9-124">O objeto de aplicativo do qual as credenciais será removida.</span><span class="sxs-lookup"><span data-stu-id="c7fb9-124">The application object to remove the credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c7fb9-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7fb9-125">-DefaultProfile</span></span>
<span data-ttu-id="c7fb9-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="c7fb9-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c7fb9-127">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c7fb9-127">-DisplayName</span></span>
<span data-ttu-id="c7fb9-128">O nome de exibição do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c7fb9-128">The display name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7fb9-129">-Force</span><span class="sxs-lookup"><span data-stu-id="c7fb9-129">-Force</span></span>
<span data-ttu-id="c7fb9-130">Alternar para excluir credencial sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="c7fb9-130">Switch to delete credential without a confirmation.</span></span>

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

### <span data-ttu-id="c7fb9-131">-KeyId</span><span class="sxs-lookup"><span data-stu-id="c7fb9-131">-KeyId</span></span>
<span data-ttu-id="c7fb9-132">Especifica a chave de credencial a ser removida.</span><span class="sxs-lookup"><span data-stu-id="c7fb9-132">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="c7fb9-133">As IDs de chave do aplicativo podem ser obtidas usando o cmdlet Get-AzADAppCredential.</span><span class="sxs-lookup"><span data-stu-id="c7fb9-133">The key Ids for the application can be obtained using the Get-AzADAppCredential cmdlet.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet, ApplicationIdWithKeyIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectWithKeyIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7fb9-134">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="c7fb9-134">-ObjectId</span></span>
<span data-ttu-id="c7fb9-135">A ID de objeto do aplicativo do qual as credenciais será removida.</span><span class="sxs-lookup"><span data-stu-id="c7fb9-135">The object id of the application to remove the credentials from.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7fb9-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c7fb9-136">-PassThru</span></span>
<span data-ttu-id="c7fb9-137">Se o comando foi concluído, a especificação será retorna true se o comando foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="c7fb9-137">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="c7fb9-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c7fb9-138">-Confirm</span></span>
<span data-ttu-id="c7fb9-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7fb9-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7fb9-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7fb9-140">-WhatIf</span></span>
<span data-ttu-id="c7fb9-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c7fb9-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7fb9-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c7fb9-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7fb9-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7fb9-143">CommonParameters</span></span>
<span data-ttu-id="c7fb9-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7fb9-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7fb9-145">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7fb9-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7fb9-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c7fb9-146">INPUTS</span></span>

### <span data-ttu-id="c7fb9-147">System. GUID</span><span class="sxs-lookup"><span data-stu-id="c7fb9-147">System.Guid</span></span>

### <span data-ttu-id="c7fb9-148">System. String</span><span class="sxs-lookup"><span data-stu-id="c7fb9-148">System.String</span></span>

### <span data-ttu-id="c7fb9-149">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="c7fb9-149">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="c7fb9-150">Parâmetros: applicationObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c7fb9-150">Parameters: ApplicationObject (ByValue)</span></span>

## <span data-ttu-id="c7fb9-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c7fb9-151">OUTPUTS</span></span>

### <span data-ttu-id="c7fb9-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c7fb9-152">System.Boolean</span></span>

## <span data-ttu-id="c7fb9-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c7fb9-153">NOTES</span></span>

## <span data-ttu-id="c7fb9-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c7fb9-154">RELATED LINKS</span></span>

[<span data-ttu-id="c7fb9-155">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="c7fb9-155">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="c7fb9-156">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="c7fb9-156">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="c7fb9-157">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="c7fb9-157">Get-AzADApplication</span></span>](./Get-AzADApplication.md)
