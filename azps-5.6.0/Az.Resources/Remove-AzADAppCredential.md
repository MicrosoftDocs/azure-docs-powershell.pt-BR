---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C61FA834-BEBE-4DBF-888F-C6CB8CC95390
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADAppCredential.md
ms.openlocfilehash: 93e2b62cf1261b20df1ea6c90d48caa1e1d88ec2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889160"
---
# <span data-ttu-id="7c2ca-101">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="7c2ca-101">Remove-AzADAppCredential</span></span>

## <span data-ttu-id="7c2ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c2ca-102">SYNOPSIS</span></span>
<span data-ttu-id="7c2ca-103">Remove uma credencial de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7c2ca-103">Removes a credential from an application.</span></span>

## <span data-ttu-id="7c2ca-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7c2ca-104">SYNTAX</span></span>

### <span data-ttu-id="7c2ca-105">ApplicationObjectIdWithKeyIdParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7c2ca-105">ApplicationObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzADAppCredential -ObjectId <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c2ca-106">ApplicationIdWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c2ca-106">ApplicationIdWithKeyIdParameterSet</span></span>
```
Remove-AzADAppCredential -ApplicationId <Guid> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c2ca-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c2ca-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzADAppCredential -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c2ca-108">ApplicationObjectWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c2ca-108">ApplicationObjectWithKeyIdParameterSet</span></span>
```
Remove-AzADAppCredential [-KeyId <Guid>] -ApplicationObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c2ca-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7c2ca-109">DESCRIPTION</span></span>
<span data-ttu-id="7c2ca-110">O Remove-AzADAppCredential cmdlet pode ser usado para remover uma chave de credencial de um aplicativo no caso de um comprometimento ou como parte da expiração de rolagem de chave de credencial.</span><span class="sxs-lookup"><span data-stu-id="7c2ca-110">The Remove-AzADAppCredential cmdlet can be used to remove a credential key from an application in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="7c2ca-111">O aplicativo é identificado fornecendo a ID do objeto ou AppId.</span><span class="sxs-lookup"><span data-stu-id="7c2ca-111">The application is identified by supplying either the object ID or AppId.</span></span>
<span data-ttu-id="7c2ca-112">A credencial a ser removida é identificada por sua ID de chave.</span><span class="sxs-lookup"><span data-stu-id="7c2ca-112">The credential to be removed is identified by its key ID.</span></span>

## <span data-ttu-id="7c2ca-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7c2ca-113">EXAMPLES</span></span>

### <span data-ttu-id="7c2ca-114">Exemplo 1: Remover uma credencial específica de um aplicativo</span><span class="sxs-lookup"><span data-stu-id="7c2ca-114">Example 1: Remove a specific credential from an application</span></span>

```powershell
PS C:\> Remove-AzADAppCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="7c2ca-115">Remove a credencial com a id da chave '9044423a-60a3-45ac-9ab1-09534157ebb' do aplicativo com a id do objeto '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span><span class="sxs-lookup"><span data-stu-id="7c2ca-115">Removes the credential with key id '9044423a-60a3-45ac-9ab1-09534157ebb' from the application with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span></span>

### <span data-ttu-id="7c2ca-116">Exemplo 2: Remover todas as credenciais de um aplicativo</span><span class="sxs-lookup"><span data-stu-id="7c2ca-116">Example 2: Remove all credentials from an application</span></span>

```powershell
PS C:\> Remove-AzADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58
```

<span data-ttu-id="7c2ca-117">Remove todas as credenciais do aplicativo com a id do aplicativo '4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58'.</span><span class="sxs-lookup"><span data-stu-id="7c2ca-117">Removes all credentials from the application with application id '4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58'.</span></span>

### <span data-ttu-id="7c2ca-118">Exemplo 3: Remover todas as credenciais usando a canalização</span><span class="sxs-lookup"><span data-stu-id="7c2ca-118">Example 3: Remove all credentials using piping</span></span>

```powershell
PS C:\> Get-AzADApplication -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 | Remove-AzADAppCredential
```

<span data-ttu-id="7c2ca-119">Obtém o aplicativo com a id do objeto '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82' e canalização para o cmdlet Remove-AzADAppCredential e remove todas as credenciais desse aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7c2ca-119">Gets the application with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82' and pipes that to the Remove-AzADAppCredential cmdlet and removes all credentials from that application.</span></span>

## <span data-ttu-id="7c2ca-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7c2ca-120">PARAMETERS</span></span>

### <span data-ttu-id="7c2ca-121">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="7c2ca-121">-ApplicationId</span></span>
<span data-ttu-id="7c2ca-122">A id do aplicativo para remover as credenciais.</span><span class="sxs-lookup"><span data-stu-id="7c2ca-122">The id of the application to remove the credentials from.</span></span>

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

### <span data-ttu-id="7c2ca-123">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="7c2ca-123">-ApplicationObject</span></span>
<span data-ttu-id="7c2ca-124">O objeto application para remover as credenciais.</span><span class="sxs-lookup"><span data-stu-id="7c2ca-124">The application object to remove the credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7c2ca-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c2ca-125">-DefaultProfile</span></span>
<span data-ttu-id="7c2ca-126">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="7c2ca-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7c2ca-127">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="7c2ca-127">-DisplayName</span></span>
<span data-ttu-id="7c2ca-128">O nome de exibição do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7c2ca-128">The display name of the application.</span></span>

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

### <span data-ttu-id="7c2ca-129">-Force</span><span class="sxs-lookup"><span data-stu-id="7c2ca-129">-Force</span></span>
<span data-ttu-id="7c2ca-130">Alternar para excluir credencial sem uma confirmação.</span><span class="sxs-lookup"><span data-stu-id="7c2ca-130">Switch to delete credential without a confirmation.</span></span>

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

### <span data-ttu-id="7c2ca-131">-KeyId</span><span class="sxs-lookup"><span data-stu-id="7c2ca-131">-KeyId</span></span>
<span data-ttu-id="7c2ca-132">Especifica a chave de credencial a ser removida.</span><span class="sxs-lookup"><span data-stu-id="7c2ca-132">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="7c2ca-133">As IDs de chave do aplicativo podem ser obtidas usando o cmdlet Get-AzADAppCredential.</span><span class="sxs-lookup"><span data-stu-id="7c2ca-133">The key Ids for the application can be obtained using the Get-AzADAppCredential cmdlet.</span></span>

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

### <span data-ttu-id="7c2ca-134">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="7c2ca-134">-ObjectId</span></span>
<span data-ttu-id="7c2ca-135">A id do objeto do aplicativo para remover as credenciais.</span><span class="sxs-lookup"><span data-stu-id="7c2ca-135">The object id of the application to remove the credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c2ca-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7c2ca-136">-PassThru</span></span>
<span data-ttu-id="7c2ca-137">Especificar isso retornará true se o comando tiver sido bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="7c2ca-137">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="7c2ca-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7c2ca-138">-Confirm</span></span>
<span data-ttu-id="7c2ca-139">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c2ca-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c2ca-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c2ca-140">-WhatIf</span></span>
<span data-ttu-id="7c2ca-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7c2ca-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c2ca-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7c2ca-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c2ca-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c2ca-143">CommonParameters</span></span>
<span data-ttu-id="7c2ca-144">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c2ca-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c2ca-145">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7c2ca-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c2ca-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7c2ca-146">INPUTS</span></span>

### <span data-ttu-id="7c2ca-147">System.String</span><span class="sxs-lookup"><span data-stu-id="7c2ca-147">System.String</span></span>

### <span data-ttu-id="7c2ca-148">System.Guid</span><span class="sxs-lookup"><span data-stu-id="7c2ca-148">System.Guid</span></span>

### <span data-ttu-id="7c2ca-149">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="7c2ca-149">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="7c2ca-150">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7c2ca-150">OUTPUTS</span></span>

### <span data-ttu-id="7c2ca-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7c2ca-151">System.Boolean</span></span>

## <span data-ttu-id="7c2ca-152">NOTES</span><span class="sxs-lookup"><span data-stu-id="7c2ca-152">NOTES</span></span>

## <span data-ttu-id="7c2ca-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7c2ca-153">RELATED LINKS</span></span>

[<span data-ttu-id="7c2ca-154">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="7c2ca-154">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="7c2ca-155">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="7c2ca-155">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="7c2ca-156">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="7c2ca-156">Get-AzADApplication</span></span>](./Get-AzADApplication.md)
