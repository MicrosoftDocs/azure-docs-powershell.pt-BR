---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C61FA834-BEBE-4DBF-888F-C6CB8CC95390
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADAppCredential.md
ms.openlocfilehash: 6c076258acd19714f30976fd353d7cbbacdf1d94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428369"
---
# <span data-ttu-id="7efdb-101">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="7efdb-101">Remove-AzureRmADAppCredential</span></span>

## <span data-ttu-id="7efdb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7efdb-102">SYNOPSIS</span></span>
<span data-ttu-id="7efdb-103">Remove uma credencial de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7efdb-103">Removes a credential from an application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7efdb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7efdb-104">SYNTAX</span></span>

### <span data-ttu-id="7efdb-105">ApplicationObjectIdWithKeyIdParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="7efdb-105">ApplicationObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzureRmADAppCredential -ObjectId <Guid> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7efdb-106">ApplicationIdWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7efdb-106">ApplicationIdWithKeyIdParameterSet</span></span>
```
Remove-AzureRmADAppCredential -ApplicationId <Guid> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7efdb-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7efdb-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzureRmADAppCredential -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7efdb-108">ApplicationObjectWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7efdb-108">ApplicationObjectWithKeyIdParameterSet</span></span>
```
Remove-AzureRmADAppCredential [-KeyId <Guid>] -ApplicationObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7efdb-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7efdb-109">DESCRIPTION</span></span>
<span data-ttu-id="7efdb-110">O cmdlet Remove-AzureRmADAppCredential pode ser usado para remover uma chave de credencial de um aplicativo no caso de um comprometimento ou como parte da expiração da sobreposição da chave da credencial.</span><span class="sxs-lookup"><span data-stu-id="7efdb-110">The Remove-AzureRmADAppCredential cmdlet can be used to remove a credential key from an application in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="7efdb-111">O aplicativo é identificado fornecendo o ID do objeto ou AppId.</span><span class="sxs-lookup"><span data-stu-id="7efdb-111">The application is identified by supplying either the object ID or AppId.</span></span>
<span data-ttu-id="7efdb-112">A credencial a ser removida é identificada pela ID da chave.</span><span class="sxs-lookup"><span data-stu-id="7efdb-112">The credential to be removed is identified by its key ID.</span></span>

## <span data-ttu-id="7efdb-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7efdb-113">EXAMPLES</span></span>

### <span data-ttu-id="7efdb-114">Exemplo 1: remover uma credencial específica de um aplicativo</span><span class="sxs-lookup"><span data-stu-id="7efdb-114">Example 1 - Remove a specific credential from an application</span></span>

```
PS C:\> Remove-AzureRmADAppCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="7efdb-115">Remove a credencial com a ID da chave ' 9044423a-60a3-45ac-9ab1-09534157ebb ' do aplicativo com a ID de objeto ' 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 '.</span><span class="sxs-lookup"><span data-stu-id="7efdb-115">Removes the credential with key id '9044423a-60a3-45ac-9ab1-09534157ebb' from the application with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span></span>

### <span data-ttu-id="7efdb-116">Exemplo 2-remover todas as credenciais de um aplicativo</span><span class="sxs-lookup"><span data-stu-id="7efdb-116">Example 2 - Remove all credentials from an application</span></span>

```
PS C:\> Remove-AzureRmADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58
```

<span data-ttu-id="7efdb-117">Remove todas as credenciais do aplicativo com a ID de aplicativo ' 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 '.</span><span class="sxs-lookup"><span data-stu-id="7efdb-117">Removes all credentials from the application with application id '4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58'.</span></span>

### <span data-ttu-id="7efdb-118">Exemplo 3-remover todas as credenciais usando o encanamento</span><span class="sxs-lookup"><span data-stu-id="7efdb-118">Example 3 - Remove all credentials using piping</span></span>

```
PS C:\> Get-AzureRmADApplication -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 | Remove-AzureRmADAppCredential
```

<span data-ttu-id="7efdb-119">Obtém o aplicativo com a ID de objeto ' 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 ' e canaliza-o para o cmdlet Remove-AzureRmADAppCredential e remove todas as credenciais desse aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7efdb-119">Gets the application with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82' and pipes that to the Remove-AzureRmADAppCredential cmdlet and removes all credentials from that application.</span></span>

## <span data-ttu-id="7efdb-120">OS</span><span class="sxs-lookup"><span data-stu-id="7efdb-120">PARAMETERS</span></span>

### <span data-ttu-id="7efdb-121">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="7efdb-121">-ApplicationId</span></span>
<span data-ttu-id="7efdb-122">A ID do aplicativo do qual as credenciais será removida.</span><span class="sxs-lookup"><span data-stu-id="7efdb-122">The id of the application to remove the credentials from.</span></span>

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

### <span data-ttu-id="7efdb-123">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="7efdb-123">-ApplicationObject</span></span>
<span data-ttu-id="7efdb-124">O objeto de aplicativo do qual as credenciais será removida.</span><span class="sxs-lookup"><span data-stu-id="7efdb-124">The application object to remove the credentials from.</span></span>

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

### <span data-ttu-id="7efdb-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7efdb-125">-DefaultProfile</span></span>
<span data-ttu-id="7efdb-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="7efdb-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7efdb-127">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="7efdb-127">-DisplayName</span></span>
<span data-ttu-id="7efdb-128">O nome de exibição do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7efdb-128">The display name of the application.</span></span>

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

### <span data-ttu-id="7efdb-129">-Force</span><span class="sxs-lookup"><span data-stu-id="7efdb-129">-Force</span></span>
<span data-ttu-id="7efdb-130">Alternar para excluir credencial sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="7efdb-130">Switch to delete credential without a confirmation.</span></span>

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

### <span data-ttu-id="7efdb-131">-KeyId</span><span class="sxs-lookup"><span data-stu-id="7efdb-131">-KeyId</span></span>
<span data-ttu-id="7efdb-132">Especifica a chave de credencial a ser removida.</span><span class="sxs-lookup"><span data-stu-id="7efdb-132">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="7efdb-133">As IDs de chave do aplicativo podem ser obtidas usando o cmdlet Get-AzureRmADAppCredential.</span><span class="sxs-lookup"><span data-stu-id="7efdb-133">The key Ids for the application can be obtained using the Get-AzureRmADAppCredential cmdlet.</span></span>

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

### <span data-ttu-id="7efdb-134">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="7efdb-134">-ObjectId</span></span>
<span data-ttu-id="7efdb-135">A ID de objeto do aplicativo do qual as credenciais será removida.</span><span class="sxs-lookup"><span data-stu-id="7efdb-135">The object id of the application to remove the credentials from.</span></span>

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

### <span data-ttu-id="7efdb-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7efdb-136">-PassThru</span></span>
<span data-ttu-id="7efdb-137">Se o comando foi concluído, a especificação será retorna true se o comando foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="7efdb-137">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="7efdb-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7efdb-138">-Confirm</span></span>
<span data-ttu-id="7efdb-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7efdb-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7efdb-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7efdb-140">-WhatIf</span></span>
<span data-ttu-id="7efdb-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7efdb-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7efdb-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7efdb-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7efdb-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7efdb-143">CommonParameters</span></span>
<span data-ttu-id="7efdb-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7efdb-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7efdb-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7efdb-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7efdb-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7efdb-146">INPUTS</span></span>

### <span data-ttu-id="7efdb-147">System. GUID</span><span class="sxs-lookup"><span data-stu-id="7efdb-147">System.Guid</span></span>

### <span data-ttu-id="7efdb-148">System. String</span><span class="sxs-lookup"><span data-stu-id="7efdb-148">System.String</span></span>

### <span data-ttu-id="7efdb-149">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="7efdb-149">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="7efdb-150">Parâmetros: applicationObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7efdb-150">Parameters: ApplicationObject (ByValue)</span></span>

## <span data-ttu-id="7efdb-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7efdb-151">OUTPUTS</span></span>

### <span data-ttu-id="7efdb-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7efdb-152">System.Boolean</span></span>

## <span data-ttu-id="7efdb-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7efdb-153">NOTES</span></span>

## <span data-ttu-id="7efdb-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7efdb-154">RELATED LINKS</span></span>

[<span data-ttu-id="7efdb-155">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="7efdb-155">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="7efdb-156">New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="7efdb-156">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="7efdb-157">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="7efdb-157">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)
