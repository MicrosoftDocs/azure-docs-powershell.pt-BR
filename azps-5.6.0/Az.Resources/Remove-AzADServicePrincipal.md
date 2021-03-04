---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0C8C07CA-6720-452F-A952-48C76EBF3BBD
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADServicePrincipal.md
ms.openlocfilehash: e9e4a8e902b3d71507a9e9d731ceb518825f8aa6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887680"
---
# <span data-ttu-id="be675-101">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="be675-101">Remove-AzADServicePrincipal</span></span>

## <span data-ttu-id="be675-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be675-102">SYNOPSIS</span></span>
<span data-ttu-id="be675-103">Exclui a entidade de serviço do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="be675-103">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="be675-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="be675-104">SYNTAX</span></span>

### <span data-ttu-id="be675-105">ObjectIdParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="be675-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADServicePrincipal -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be675-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="be675-106">ApplicationIdParameterSet</span></span>
```
Remove-AzADServicePrincipal -ApplicationId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be675-107">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="be675-107">SPNParameterSet</span></span>
```
Remove-AzADServicePrincipal -ServicePrincipalName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be675-108">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="be675-108">DisplayNameParameterSet</span></span>
```
Remove-AzADServicePrincipal -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be675-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="be675-109">InputObjectParameterSet</span></span>
```
Remove-AzADServicePrincipal -InputObject <PSADServicePrincipal> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be675-110">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="be675-110">ApplicationObjectParameterSet</span></span>
```
Remove-AzADServicePrincipal -ApplicationObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be675-111">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="be675-111">DESCRIPTION</span></span>
<span data-ttu-id="be675-112">Exclui a entidade de serviço do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="be675-112">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="be675-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="be675-113">EXAMPLES</span></span>

### <span data-ttu-id="be675-114">Exemplo 1 - Remover uma entidade de serviço por id do objeto</span><span class="sxs-lookup"><span data-stu-id="be675-114">Example 1 - Remove a service principal by object id</span></span>

```
PS C:\> Remove-AzADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45
```

<span data-ttu-id="be675-115">Remove a entidade de serviço com a id do objeto '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45'.</span><span class="sxs-lookup"><span data-stu-id="be675-115">Removes the service principal with object id '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45'.</span></span>

### <span data-ttu-id="be675-116">Exemplo 2 - Remover uma entidade de serviço por id do aplicativo</span><span class="sxs-lookup"><span data-stu-id="be675-116">Example 2 - Remove a service principal by application id</span></span>

```
PS C:\> Remove-AzADServicePrincipal -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76
```

<span data-ttu-id="be675-117">Remove a entidade de serviço com a id do aplicativo '9263469e-d328-4321-8646-3e3e75d20e76'.</span><span class="sxs-lookup"><span data-stu-id="be675-117">Removes the service principal with application id '9263469e-d328-4321-8646-3e3e75d20e76'.</span></span>

### <span data-ttu-id="be675-118">Exemplo 3 - Remover uma entidade de serviço pelo SPN</span><span class="sxs-lookup"><span data-stu-id="be675-118">Example 3 - Remove a service principal by SPN</span></span>

```
PS C:\> Remove-AzADServicePrincipal -ServicePrincipalName MyServicePrincipal
```

<span data-ttu-id="be675-119">Remover a entidade de serviço com o nome da entidade de serviço "MyServicePrincipal"</span><span class="sxs-lookup"><span data-stu-id="be675-119">Remove the service principal with service principal name "MyServicePrincipal"</span></span>

### <span data-ttu-id="be675-120">Exemplo 4 - Remover uma entidade de serviço canalização</span><span class="sxs-lookup"><span data-stu-id="be675-120">Example 4 - Remove a service principal by piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45 | Remove-AzADServicePrincipal
```

<span data-ttu-id="be675-121">Obtém a entidade de serviço com a id do objeto '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45' e canalização para o cmdlet Remove-AzADServicePrincipal para remover essa entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="be675-121">Gets the service principal with object id '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45' and pipes that to the Remove-AzADServicePrincipal cmdlet to remove that service principal.</span></span>

### <span data-ttu-id="be675-122">Exemplo 5 - Remover uma entidade de serviço canalização de um aplicativo</span><span class="sxs-lookup"><span data-stu-id="be675-122">Example 5 - Remove a service principal by piping an application</span></span>

```
PS C:\> Get-AzApplication -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76 | Remove-AzADServicePrincipal
```

<span data-ttu-id="be675-123">Obtém o aplicativo com a id do aplicativo '9263469e-d328-4321-8646-3e3e75d20e76' e canalizará isso para o cmdlet Remove-AzADServicePrincipal para remover a entidade de serviço associada a esse aplicativo.</span><span class="sxs-lookup"><span data-stu-id="be675-123">Gets the application with application id '9263469e-d328-4321-8646-3e3e75d20e76' and pipes that to the Remove-AzADServicePrincipal cmdlet to remove the service principal associated with that application.</span></span>

## <span data-ttu-id="be675-124">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="be675-124">PARAMETERS</span></span>

### <span data-ttu-id="be675-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="be675-125">-ApplicationId</span></span>
<span data-ttu-id="be675-126">A ID do aplicativo principal do serviço.</span><span class="sxs-lookup"><span data-stu-id="be675-126">The service principal application id.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be675-127">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="be675-127">-ApplicationObject</span></span>
<span data-ttu-id="be675-128">O objeto application cuja entidade de serviço está sendo removida.</span><span class="sxs-lookup"><span data-stu-id="be675-128">The application object whose service principal is being removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be675-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be675-129">-DefaultProfile</span></span>
<span data-ttu-id="be675-130">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="be675-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="be675-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="be675-131">-DisplayName</span></span>
<span data-ttu-id="be675-132">O nome de exibição da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="be675-132">The display name of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be675-133">-Force</span><span class="sxs-lookup"><span data-stu-id="be675-133">-Force</span></span>
<span data-ttu-id="be675-134">Alternar para excluir a entidade de serviço sem uma confirmação.</span><span class="sxs-lookup"><span data-stu-id="be675-134">Switch to delete service principal without a confirmation.</span></span>

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

### <span data-ttu-id="be675-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="be675-135">-InputObject</span></span>
<span data-ttu-id="be675-136">O objeto de entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="be675-136">The service principal object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be675-137">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="be675-137">-ObjectId</span></span>
<span data-ttu-id="be675-138">A id do objeto da entidade de serviço a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="be675-138">The object id of the service principal to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases: PrincipalId, Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be675-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="be675-139">-PassThru</span></span>
<span data-ttu-id="be675-140">Se especificado, retorna a entidade de serviço excluída.</span><span class="sxs-lookup"><span data-stu-id="be675-140">If specified, returns the deleted service principal.</span></span>

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

### <span data-ttu-id="be675-141">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="be675-141">-ServicePrincipalName</span></span>
<span data-ttu-id="be675-142">O nome da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="be675-142">The service principal name.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be675-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="be675-143">-Confirm</span></span>
<span data-ttu-id="be675-144">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be675-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be675-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be675-145">-WhatIf</span></span>
<span data-ttu-id="be675-146">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="be675-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be675-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="be675-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be675-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be675-148">CommonParameters</span></span>
<span data-ttu-id="be675-149">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be675-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be675-150">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="be675-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be675-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="be675-151">INPUTS</span></span>

### <span data-ttu-id="be675-152">System.String</span><span class="sxs-lookup"><span data-stu-id="be675-152">System.String</span></span>

### <span data-ttu-id="be675-153">System.Guid</span><span class="sxs-lookup"><span data-stu-id="be675-153">System.Guid</span></span>

### <span data-ttu-id="be675-154">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="be675-154">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="be675-155">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="be675-155">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="be675-156">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="be675-156">OUTPUTS</span></span>

### <span data-ttu-id="be675-157">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="be675-157">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="be675-158">NOTES</span><span class="sxs-lookup"><span data-stu-id="be675-158">NOTES</span></span>
<span data-ttu-id="be675-159">Palavras-chave: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span><span class="sxs-lookup"><span data-stu-id="be675-159">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="be675-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="be675-160">RELATED LINKS</span></span>

[<span data-ttu-id="be675-161">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="be675-161">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)

[<span data-ttu-id="be675-162">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="be675-162">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="be675-163">Update-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="be675-163">Update-AzADServicePrincipal</span></span>](./Update-AzADServicePrincipal.md)

[<span data-ttu-id="be675-164">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="be675-164">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="be675-165">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="be675-165">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)
