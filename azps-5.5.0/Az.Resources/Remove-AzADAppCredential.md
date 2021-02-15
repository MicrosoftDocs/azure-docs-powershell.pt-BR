---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C61FA834-BEBE-4DBF-888F-C6CB8CC95390
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADAppCredential.md
ms.openlocfilehash: f6344590828663a0cf44d96d6fe733adff8757c5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114523"
---
# <span data-ttu-id="bd036-101">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="bd036-101">Remove-AzADAppCredential</span></span>

## <span data-ttu-id="bd036-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bd036-102">SYNOPSIS</span></span>
<span data-ttu-id="bd036-103">Remove uma credencial de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bd036-103">Removes a credential from an application.</span></span>

## <span data-ttu-id="bd036-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bd036-104">SYNTAX</span></span>

### <span data-ttu-id="bd036-105">ApplicationObjectIdWithKeyIdParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="bd036-105">ApplicationObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzADAppCredential -ObjectId <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd036-106">ApplicationIdWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd036-106">ApplicationIdWithKeyIdParameterSet</span></span>
```
Remove-AzADAppCredential -ApplicationId <Guid> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd036-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd036-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzADAppCredential -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd036-108">ApplicationObjectWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd036-108">ApplicationObjectWithKeyIdParameterSet</span></span>
```
Remove-AzADAppCredential [-KeyId <Guid>] -ApplicationObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd036-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="bd036-109">DESCRIPTION</span></span>
<span data-ttu-id="bd036-110">O Remove-AzADAppCredential cmdlet pode ser usado para remover uma chave de credencial de um aplicativo no caso de um comprometimento ou como parte da expiração da chave de credencial.</span><span class="sxs-lookup"><span data-stu-id="bd036-110">The Remove-AzADAppCredential cmdlet can be used to remove a credential key from an application in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="bd036-111">O aplicativo é identificado fornecendo a ID do objeto ou AppId.</span><span class="sxs-lookup"><span data-stu-id="bd036-111">The application is identified by supplying either the object ID or AppId.</span></span>
<span data-ttu-id="bd036-112">A credencial a ser removida é identificada por sua ID de chave.</span><span class="sxs-lookup"><span data-stu-id="bd036-112">The credential to be removed is identified by its key ID.</span></span>

## <span data-ttu-id="bd036-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bd036-113">EXAMPLES</span></span>

### <span data-ttu-id="bd036-114">Exemplo 1: remover uma credencial específica de um aplicativo</span><span class="sxs-lookup"><span data-stu-id="bd036-114">Example 1: Remove a specific credential from an application</span></span>

```powershell
PS C:\> Remove-AzADAppCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="bd036-115">Remove a credencial com a id de chave '9044423a-60a3-45ac-9ab1-09534157ebb' do aplicativo com a ID do objeto '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span><span class="sxs-lookup"><span data-stu-id="bd036-115">Removes the credential with key id '9044423a-60a3-45ac-9ab1-09534157ebb' from the application with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span></span>

### <span data-ttu-id="bd036-116">Exemplo 2: Remover todas as credenciais de um aplicativo</span><span class="sxs-lookup"><span data-stu-id="bd036-116">Example 2: Remove all credentials from an application</span></span>

```powershell
PS C:\> Remove-AzADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58
```

<span data-ttu-id="bd036-117">Remove todas as credenciais do aplicativo com a id do aplicativo '4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58'.</span><span class="sxs-lookup"><span data-stu-id="bd036-117">Removes all credentials from the application with application id '4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58'.</span></span>

### <span data-ttu-id="bd036-118">Exemplo 3: Remover todas as credenciais usando a piping</span><span class="sxs-lookup"><span data-stu-id="bd036-118">Example 3: Remove all credentials using piping</span></span>

```powershell
PS C:\> Get-AzADApplication -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 | Remove-AzADAppCredential
```

<span data-ttu-id="bd036-119">Obtém o aplicativo com a ID do objeto '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82' e canos que para o cmdlet Remove-AzADAppCredential e remove todas as credenciais desse aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bd036-119">Gets the application with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82' and pipes that to the Remove-AzADAppCredential cmdlet and removes all credentials from that application.</span></span>

## <span data-ttu-id="bd036-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bd036-120">PARAMETERS</span></span>

### <span data-ttu-id="bd036-121">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="bd036-121">-ApplicationId</span></span>
<span data-ttu-id="bd036-122">A ID do aplicativo para remover as credenciais.</span><span class="sxs-lookup"><span data-stu-id="bd036-122">The id of the application to remove the credentials from.</span></span>

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

### <span data-ttu-id="bd036-123">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="bd036-123">-ApplicationObject</span></span>
<span data-ttu-id="bd036-124">O objeto do aplicativo para remover as credenciais.</span><span class="sxs-lookup"><span data-stu-id="bd036-124">The application object to remove the credentials from.</span></span>

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

### <span data-ttu-id="bd036-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd036-125">-DefaultProfile</span></span>
<span data-ttu-id="bd036-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="bd036-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bd036-127">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="bd036-127">-DisplayName</span></span>
<span data-ttu-id="bd036-128">O nome de exibição do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bd036-128">The display name of the application.</span></span>

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

### <span data-ttu-id="bd036-129">-Forçar</span><span class="sxs-lookup"><span data-stu-id="bd036-129">-Force</span></span>
<span data-ttu-id="bd036-130">Alternar para excluir credencial sem uma confirmação.</span><span class="sxs-lookup"><span data-stu-id="bd036-130">Switch to delete credential without a confirmation.</span></span>

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

### <span data-ttu-id="bd036-131">-KeyId</span><span class="sxs-lookup"><span data-stu-id="bd036-131">-KeyId</span></span>
<span data-ttu-id="bd036-132">Especifica a chave de credencial a ser removida.</span><span class="sxs-lookup"><span data-stu-id="bd036-132">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="bd036-133">As IDs de chave do aplicativo podem ser obtidas usando o cmdlet Get-AzADAppCredential dados.</span><span class="sxs-lookup"><span data-stu-id="bd036-133">The key Ids for the application can be obtained using the Get-AzADAppCredential cmdlet.</span></span>

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

### <span data-ttu-id="bd036-134">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="bd036-134">-ObjectId</span></span>
<span data-ttu-id="bd036-135">A ID do objeto do aplicativo para remover as credenciais.</span><span class="sxs-lookup"><span data-stu-id="bd036-135">The object id of the application to remove the credentials from.</span></span>

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

### <span data-ttu-id="bd036-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bd036-136">-PassThru</span></span>
<span data-ttu-id="bd036-137">Especificar isso retornará verdadeiro se o comando tiver sido bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="bd036-137">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="bd036-138">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="bd036-138">-Confirm</span></span>
<span data-ttu-id="bd036-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd036-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd036-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd036-140">-WhatIf</span></span>
<span data-ttu-id="bd036-141">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="bd036-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd036-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bd036-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd036-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd036-143">CommonParameters</span></span>
<span data-ttu-id="bd036-144">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd036-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd036-145">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bd036-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd036-146">Entradas</span><span class="sxs-lookup"><span data-stu-id="bd036-146">INPUTS</span></span>

### <span data-ttu-id="bd036-147">System.String</span><span class="sxs-lookup"><span data-stu-id="bd036-147">System.String</span></span>

### <span data-ttu-id="bd036-148">System.Guid</span><span class="sxs-lookup"><span data-stu-id="bd036-148">System.Guid</span></span>

### <span data-ttu-id="bd036-149">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="bd036-149">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="bd036-150">Saídas</span><span class="sxs-lookup"><span data-stu-id="bd036-150">OUTPUTS</span></span>

### <span data-ttu-id="bd036-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bd036-151">System.Boolean</span></span>

## <span data-ttu-id="bd036-152">Notas</span><span class="sxs-lookup"><span data-stu-id="bd036-152">NOTES</span></span>

## <span data-ttu-id="bd036-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bd036-153">RELATED LINKS</span></span>

[<span data-ttu-id="bd036-154">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="bd036-154">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="bd036-155">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="bd036-155">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="bd036-156">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="bd036-156">Get-AzADApplication</span></span>](./Get-AzADApplication.md)
