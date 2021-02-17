---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0C8C07CA-6720-452F-A952-48C76EBF3BBD
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADServicePrincipal.md
ms.openlocfilehash: 2658e5ff70603cb9bbe3aa3a7ccd47713249c726
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100413482"
---
# <span data-ttu-id="efe0c-101">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="efe0c-101">Remove-AzADServicePrincipal</span></span>

## <span data-ttu-id="efe0c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="efe0c-102">SYNOPSIS</span></span>
<span data-ttu-id="efe0c-103">Exclui a entidade de serviço do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="efe0c-103">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="efe0c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="efe0c-104">SYNTAX</span></span>

### <span data-ttu-id="efe0c-105">ObjectIdParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="efe0c-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADServicePrincipal -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efe0c-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="efe0c-106">ApplicationIdParameterSet</span></span>
```
Remove-AzADServicePrincipal -ApplicationId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efe0c-107">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="efe0c-107">SPNParameterSet</span></span>
```
Remove-AzADServicePrincipal -ServicePrincipalName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efe0c-108">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="efe0c-108">DisplayNameParameterSet</span></span>
```
Remove-AzADServicePrincipal -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efe0c-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="efe0c-109">InputObjectParameterSet</span></span>
```
Remove-AzADServicePrincipal -InputObject <PSADServicePrincipal> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efe0c-110">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="efe0c-110">ApplicationObjectParameterSet</span></span>
```
Remove-AzADServicePrincipal -ApplicationObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="efe0c-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="efe0c-111">DESCRIPTION</span></span>
<span data-ttu-id="efe0c-112">Exclui a entidade de serviço do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="efe0c-112">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="efe0c-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="efe0c-113">EXAMPLES</span></span>

### <span data-ttu-id="efe0c-114">Exemplo 1 - Remover uma entidade de serviço por id do objeto</span><span class="sxs-lookup"><span data-stu-id="efe0c-114">Example 1 - Remove a service principal by object id</span></span>

```
PS C:\> Remove-AzADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45
```

<span data-ttu-id="efe0c-115">Remove a entidade de serviço com a ID do objeto '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45'.</span><span class="sxs-lookup"><span data-stu-id="efe0c-115">Removes the service principal with object id '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45'.</span></span>

### <span data-ttu-id="efe0c-116">Exemplo 2 - Remover uma entidade de serviço por ID do aplicativo</span><span class="sxs-lookup"><span data-stu-id="efe0c-116">Example 2 - Remove a service principal by application id</span></span>

```
PS C:\> Remove-AzADServicePrincipal -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76
```

<span data-ttu-id="efe0c-117">Remove a entidade de serviço com a ID do aplicativo '9263469e-d328-4321-8646-3e3e75d20e76'.</span><span class="sxs-lookup"><span data-stu-id="efe0c-117">Removes the service principal with application id '9263469e-d328-4321-8646-3e3e75d20e76'.</span></span>

### <span data-ttu-id="efe0c-118">Exemplo 3 - Remover uma entidade de serviço pelo SPN</span><span class="sxs-lookup"><span data-stu-id="efe0c-118">Example 3 - Remove a service principal by SPN</span></span>

```
PS C:\> Remove-AzADServicePrincipal -ServicePrincipalName MyServicePrincipal
```

<span data-ttu-id="efe0c-119">Remover a entidade de serviço com o nome da entidade de serviço "MyServicePrincipal"</span><span class="sxs-lookup"><span data-stu-id="efe0c-119">Remove the service principal with service principal name "MyServicePrincipal"</span></span>

### <span data-ttu-id="efe0c-120">Exemplo 4 - Remover uma entidade de serviço por piping</span><span class="sxs-lookup"><span data-stu-id="efe0c-120">Example 4 - Remove a service principal by piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45 | Remove-AzADServicePrincipal
```

<span data-ttu-id="efe0c-121">Obtém a entidade de serviço com a ID do objeto '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45' e os canos que estão no cmdlet Remove-AzADServicePrincipal para remover essa entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="efe0c-121">Gets the service principal with object id '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45' and pipes that to the Remove-AzADServicePrincipal cmdlet to remove that service principal.</span></span>

### <span data-ttu-id="efe0c-122">Exemplo 5 - Remover uma entidade de serviço por meio de um aplicativo</span><span class="sxs-lookup"><span data-stu-id="efe0c-122">Example 5 - Remove a service principal by piping an application</span></span>

```
PS C:\> Get-AzApplication -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76 | Remove-AzADServicePrincipal
```

<span data-ttu-id="efe0c-123">Obtém o aplicativo com a ID do aplicativo '9263469e-d328-4321-8646-3e3e75d20e76' e os canos que estão no cmdlet Remove-AzADServicePrincipal para remover a entidade de serviço associada a esse aplicativo.</span><span class="sxs-lookup"><span data-stu-id="efe0c-123">Gets the application with application id '9263469e-d328-4321-8646-3e3e75d20e76' and pipes that to the Remove-AzADServicePrincipal cmdlet to remove the service principal associated with that application.</span></span>

## <span data-ttu-id="efe0c-124">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="efe0c-124">PARAMETERS</span></span>

### <span data-ttu-id="efe0c-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="efe0c-125">-ApplicationId</span></span>
<span data-ttu-id="efe0c-126">A ID do aplicativo principal do serviço.</span><span class="sxs-lookup"><span data-stu-id="efe0c-126">The service principal application id.</span></span>

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

### <span data-ttu-id="efe0c-127">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="efe0c-127">-ApplicationObject</span></span>
<span data-ttu-id="efe0c-128">O objeto do aplicativo cuja entidade de serviço está sendo removida.</span><span class="sxs-lookup"><span data-stu-id="efe0c-128">The application object whose service principal is being removed.</span></span>

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

### <span data-ttu-id="efe0c-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efe0c-129">-DefaultProfile</span></span>
<span data-ttu-id="efe0c-130">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="efe0c-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="efe0c-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="efe0c-131">-DisplayName</span></span>
<span data-ttu-id="efe0c-132">O nome de exibição da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="efe0c-132">The display name of the service principal.</span></span>

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

### <span data-ttu-id="efe0c-133">-Forçar</span><span class="sxs-lookup"><span data-stu-id="efe0c-133">-Force</span></span>
<span data-ttu-id="efe0c-134">Alternar para excluir a entidade de serviço sem uma confirmação.</span><span class="sxs-lookup"><span data-stu-id="efe0c-134">Switch to delete service principal without a confirmation.</span></span>

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

### <span data-ttu-id="efe0c-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="efe0c-135">-InputObject</span></span>
<span data-ttu-id="efe0c-136">O objeto principal do serviço.</span><span class="sxs-lookup"><span data-stu-id="efe0c-136">The service principal object.</span></span>

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

### <span data-ttu-id="efe0c-137">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="efe0c-137">-ObjectId</span></span>
<span data-ttu-id="efe0c-138">A ID do objeto da entidade de serviço a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="efe0c-138">The object id of the service principal to delete.</span></span>

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

### <span data-ttu-id="efe0c-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="efe0c-139">-PassThru</span></span>
<span data-ttu-id="efe0c-140">Se especificado, retornará a entidade de serviço excluída.</span><span class="sxs-lookup"><span data-stu-id="efe0c-140">If specified, returns the deleted service principal.</span></span>

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

### <span data-ttu-id="efe0c-141">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="efe0c-141">-ServicePrincipalName</span></span>
<span data-ttu-id="efe0c-142">O nome da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="efe0c-142">The service principal name.</span></span>

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

### <span data-ttu-id="efe0c-143">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="efe0c-143">-Confirm</span></span>
<span data-ttu-id="efe0c-144">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="efe0c-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efe0c-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efe0c-145">-WhatIf</span></span>
<span data-ttu-id="efe0c-146">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="efe0c-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="efe0c-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="efe0c-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efe0c-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efe0c-148">CommonParameters</span></span>
<span data-ttu-id="efe0c-149">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efe0c-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efe0c-150">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efe0c-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efe0c-151">Entradas</span><span class="sxs-lookup"><span data-stu-id="efe0c-151">INPUTS</span></span>

### <span data-ttu-id="efe0c-152">System.String</span><span class="sxs-lookup"><span data-stu-id="efe0c-152">System.String</span></span>

### <span data-ttu-id="efe0c-153">System.Guid</span><span class="sxs-lookup"><span data-stu-id="efe0c-153">System.Guid</span></span>

### <span data-ttu-id="efe0c-154">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="efe0c-154">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="efe0c-155">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="efe0c-155">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="efe0c-156">Saídas</span><span class="sxs-lookup"><span data-stu-id="efe0c-156">OUTPUTS</span></span>

### <span data-ttu-id="efe0c-157">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="efe0c-157">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="efe0c-158">Notas</span><span class="sxs-lookup"><span data-stu-id="efe0c-158">NOTES</span></span>
<span data-ttu-id="efe0c-159">Palavras-chave: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span><span class="sxs-lookup"><span data-stu-id="efe0c-159">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="efe0c-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="efe0c-160">RELATED LINKS</span></span>

[<span data-ttu-id="efe0c-161">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="efe0c-161">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)

[<span data-ttu-id="efe0c-162">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="efe0c-162">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)


[<span data-ttu-id="efe0c-163">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="efe0c-163">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="efe0c-164">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="efe0c-164">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)
