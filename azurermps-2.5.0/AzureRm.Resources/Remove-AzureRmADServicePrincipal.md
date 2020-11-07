---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0C8C07CA-6720-452F-A952-48C76EBF3BBD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadserviceprincipal
schema: 2.0.0
ms.openlocfilehash: 462acabd83090a893119d94d93fd767907c5144b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785151"
---
# <span data-ttu-id="5a9aa-101">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="5a9aa-101">Remove-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="5a9aa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5a9aa-102">SYNOPSIS</span></span>
<span data-ttu-id="5a9aa-103">Exclui a entidade de serviço do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5a9aa-103">Deletes the azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a9aa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5a9aa-104">SYNTAX</span></span>

### <span data-ttu-id="5a9aa-105">ObjectIdParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="5a9aa-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzureRmADServicePrincipal -ObjectId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a9aa-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a9aa-106">ApplicationIdParameterSet</span></span>
```
Remove-AzureRmADServicePrincipal -ApplicationId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a9aa-107">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a9aa-107">SPNParameterSet</span></span>
```
Remove-AzureRmADServicePrincipal -ServicePrincipalName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a9aa-108">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a9aa-108">DisplayNameParameterSet</span></span>
```
Remove-AzureRmADServicePrincipal -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a9aa-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a9aa-109">InputObjectParameterSet</span></span>
```
Remove-AzureRmADServicePrincipal -InputObject <PSADServicePrincipal> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a9aa-110">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a9aa-110">ApplicationObjectParameterSet</span></span>
```
Remove-AzureRmADServicePrincipal -ApplicationObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a9aa-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5a9aa-111">DESCRIPTION</span></span>
<span data-ttu-id="5a9aa-112">Exclui a entidade de serviço do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5a9aa-112">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="5a9aa-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5a9aa-113">EXAMPLES</span></span>

### <span data-ttu-id="5a9aa-114">Exemplo 1-remover uma entidade de serviço por ID do objeto</span><span class="sxs-lookup"><span data-stu-id="5a9aa-114">Example 1 - Remove a service principal by object id</span></span>

```
PS C:\> Remove-AzureRmADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45
```

<span data-ttu-id="5a9aa-115">Remove a entidade de serviço com a ID de objeto ' 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45 '.</span><span class="sxs-lookup"><span data-stu-id="5a9aa-115">Removes the service principal with object id '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45'.</span></span>

### <span data-ttu-id="5a9aa-116">Exemplo 2-remover uma entidade de serviço por ID do aplicativo</span><span class="sxs-lookup"><span data-stu-id="5a9aa-116">Example 2 - Remove a service principal by application id</span></span>

```
PS C:\> Remove-AzureRmADServicePrincipal -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76
```

<span data-ttu-id="5a9aa-117">Remove a entidade de serviço com a ID de aplicativo ' 9263469e-d328-4321-8646-3e3e75d20e76 '.</span><span class="sxs-lookup"><span data-stu-id="5a9aa-117">Removes the service principal with application id '9263469e-d328-4321-8646-3e3e75d20e76'.</span></span>

### <span data-ttu-id="5a9aa-118">Exemplo 3-remover uma entidade de serviço por SPN</span><span class="sxs-lookup"><span data-stu-id="5a9aa-118">Example 3 - Remove a service principal by SPN</span></span>

```
PS C:\> Remove-AzureRmADServicePrincipal -ServicePrincipalName MyServicePrincipal
```

<span data-ttu-id="5a9aa-119">Remover a entidade de serviço com o nome da entidade de serviço "MyServicePrincipal"</span><span class="sxs-lookup"><span data-stu-id="5a9aa-119">Remove the service principal with service principal name "MyServicePrincipal"</span></span>

### <span data-ttu-id="5a9aa-120">Exemplo 4-Remova uma entidade de serviço por tubulação</span><span class="sxs-lookup"><span data-stu-id="5a9aa-120">Example 4 - Remove a service principal by piping</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45 | Remove-AzureRmADServicePrincipal
```

<span data-ttu-id="5a9aa-121">Obtém a entidade de serviço com a ID de objeto ' 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45 ' e canaliza-a para o cmdlet Remove-AzureRmADServicePrincipal para remover essa entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="5a9aa-121">Gets the service principal with object id '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45' and pipes that to the Remove-AzureRmADServicePrincipal cmdlet to remove that service principal.</span></span>

### <span data-ttu-id="5a9aa-122">Exemplo 5-remover uma entidade de serviço ao canalizar um aplicativo</span><span class="sxs-lookup"><span data-stu-id="5a9aa-122">Example 5 - Remove a service principal by piping an application</span></span>

```
PS C:\> Get-AzureRmApplication -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76 | Remove-AzureRmADServicePrincipal
```

<span data-ttu-id="5a9aa-123">Obtém o aplicativo com a ID de aplicativo ' 9263469e-d328-4321-8646-3e3e75d20e76 ' e canaliza-o para o cmdlet Remove-AzureRmADServicePrincipal para remover a entidade de serviço associada a esse aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5a9aa-123">Gets the application with application id '9263469e-d328-4321-8646-3e3e75d20e76' and pipes that to the Remove-AzureRmADServicePrincipal cmdlet to remove the service principal associated with that application.</span></span>

## <span data-ttu-id="5a9aa-124">OS</span><span class="sxs-lookup"><span data-stu-id="5a9aa-124">PARAMETERS</span></span>

### <span data-ttu-id="5a9aa-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="5a9aa-125">-ApplicationId</span></span>
<span data-ttu-id="5a9aa-126">A ID do aplicativo principal do serviço.</span><span class="sxs-lookup"><span data-stu-id="5a9aa-126">The service principal application id.</span></span>

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

### <span data-ttu-id="5a9aa-127">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="5a9aa-127">-ApplicationObject</span></span>
<span data-ttu-id="5a9aa-128">O objeto de aplicativo cuja entidade de serviço está sendo removida.</span><span class="sxs-lookup"><span data-stu-id="5a9aa-128">The application object whose service principal is being removed.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a9aa-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a9aa-129">-DefaultProfile</span></span>
<span data-ttu-id="5a9aa-130">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="5a9aa-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5a9aa-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="5a9aa-131">-DisplayName</span></span>
<span data-ttu-id="5a9aa-132">O nome de exibição da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="5a9aa-132">The display name of the service principal.</span></span>

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

### <span data-ttu-id="5a9aa-133">-Force</span><span class="sxs-lookup"><span data-stu-id="5a9aa-133">-Force</span></span>
<span data-ttu-id="5a9aa-134">Alternar para excluir entidade de serviço sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="5a9aa-134">Switch to delete service principal without a confirmation.</span></span>

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

### <span data-ttu-id="5a9aa-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a9aa-135">-InputObject</span></span>
<span data-ttu-id="5a9aa-136">O objeto de entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="5a9aa-136">The service principal object.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a9aa-137">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="5a9aa-137">-ObjectId</span></span>
<span data-ttu-id="5a9aa-138">A ID de objeto da entidade de serviço a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="5a9aa-138">The object id of the service principal to delete.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases: PrincipalId, Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a9aa-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5a9aa-139">-PassThru</span></span>
<span data-ttu-id="5a9aa-140">Se especificado, retorna a entidade de serviço excluída.</span><span class="sxs-lookup"><span data-stu-id="5a9aa-140">If specified, returns the deleted service principal.</span></span>

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

### <span data-ttu-id="5a9aa-141">-Serviceprincipalnamename</span><span class="sxs-lookup"><span data-stu-id="5a9aa-141">-ServicePrincipalName</span></span>
<span data-ttu-id="5a9aa-142">O nome do serviço principal.</span><span class="sxs-lookup"><span data-stu-id="5a9aa-142">The service principal name.</span></span>

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

### <span data-ttu-id="5a9aa-143">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5a9aa-143">-Confirm</span></span>
<span data-ttu-id="5a9aa-144">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a9aa-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a9aa-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a9aa-145">-WhatIf</span></span>
<span data-ttu-id="5a9aa-146">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5a9aa-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a9aa-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5a9aa-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a9aa-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a9aa-148">CommonParameters</span></span>
<span data-ttu-id="5a9aa-149">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a9aa-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a9aa-150">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a9aa-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a9aa-151">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5a9aa-151">INPUTS</span></span>

### <span data-ttu-id="5a9aa-152">System. GUID</span><span class="sxs-lookup"><span data-stu-id="5a9aa-152">System.Guid</span></span>

### <span data-ttu-id="5a9aa-153">System. String</span><span class="sxs-lookup"><span data-stu-id="5a9aa-153">System.String</span></span>

### <span data-ttu-id="5a9aa-154">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="5a9aa-154">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>
<span data-ttu-id="5a9aa-155">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5a9aa-155">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="5a9aa-156">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="5a9aa-156">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="5a9aa-157">Parâmetros: applicationObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5a9aa-157">Parameters: ApplicationObject (ByValue)</span></span>

## <span data-ttu-id="5a9aa-158">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5a9aa-158">OUTPUTS</span></span>

### <span data-ttu-id="5a9aa-159">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="5a9aa-159">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="5a9aa-160">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5a9aa-160">NOTES</span></span>
<span data-ttu-id="5a9aa-161">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, recurso, grupo, modelo, implantação</span><span class="sxs-lookup"><span data-stu-id="5a9aa-161">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="5a9aa-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5a9aa-162">RELATED LINKS</span></span>

[<span data-ttu-id="5a9aa-163">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="5a9aa-163">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="5a9aa-164">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="5a9aa-164">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)



[<span data-ttu-id="5a9aa-165">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="5a9aa-165">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="5a9aa-166">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="5a9aa-166">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)
