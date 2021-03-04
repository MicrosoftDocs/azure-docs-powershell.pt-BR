---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 04B1E3A6-6D52-46A3-8241-2CCDB5E71642
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADSpCredential.md
ms.openlocfilehash: b71a25fa7e3e7c70b363b3462294e3c071a6ce86
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887678"
---
# <span data-ttu-id="6cb33-101">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="6cb33-101">Remove-AzADSpCredential</span></span>

## <span data-ttu-id="6cb33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6cb33-102">SYNOPSIS</span></span>
<span data-ttu-id="6cb33-103">Remove uma credencial de uma entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="6cb33-103">Removes a credential from a service principal.</span></span>

## <span data-ttu-id="6cb33-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6cb33-104">SYNTAX</span></span>

### <span data-ttu-id="6cb33-105">ObjectIdWithKeyIdParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6cb33-105">ObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzADSpCredential -ObjectId <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6cb33-106">SPNWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6cb33-106">SPNWithKeyIdParameterSet</span></span>
```
Remove-AzADSpCredential -ServicePrincipalName <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6cb33-107">DisplayNameWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6cb33-107">DisplayNameWithKeyIdParameterSet</span></span>
```
Remove-AzADSpCredential -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6cb33-108">ServicePrincipalObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6cb33-108">ServicePrincipalObjectParameterSet</span></span>
```
Remove-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6cb33-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6cb33-109">DESCRIPTION</span></span>
<span data-ttu-id="6cb33-110">O Remove-AzADSpCredential cmdlet pode ser usado para remover uma chave de credencial de uma entidade de serviço no caso de um comprometimento ou como parte da expiração de rolagem de chave de credencial.</span><span class="sxs-lookup"><span data-stu-id="6cb33-110">The Remove-AzADSpCredential cmdlet can be used to remove a credential key from a service principal in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="6cb33-111">A entidade de serviço é identificada fornecendo a ID do objeto ou o nome da entidade de serviço (SPN).</span><span class="sxs-lookup"><span data-stu-id="6cb33-111">The service principal is identified by supplying either the object ID or service principal name (SPN).</span></span>
<span data-ttu-id="6cb33-112">A credencial a ser removida será identificada por sua ID de chave se uma credencial individual for removida ou com uma opção 'All' para excluir todas as credenciais associadas à entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="6cb33-112">The credential to be removed is identified by its key ID if an individual credential is to be removed or with an 'All' switch to delete all credentials associated with the service principal.</span></span>

## <span data-ttu-id="6cb33-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6cb33-113">EXAMPLES</span></span>

### <span data-ttu-id="6cb33-114">Exemplo 1: Remover uma credencial específica de uma entidade de serviço</span><span class="sxs-lookup"><span data-stu-id="6cb33-114">Example 1: Remove a specific credential from a service principal</span></span>

```powershell
PS C:\> Remove-AzADSpCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="6cb33-115">Remove a credencial com a id da chave '9044423a-60a3-45ac-9ab1-09534157ebb' da entidade de serviço com a id do objeto '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span><span class="sxs-lookup"><span data-stu-id="6cb33-115">Removes the credential with key id '9044423a-60a3-45ac-9ab1-09534157ebb' from the service principal with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span></span>

### <span data-ttu-id="6cb33-116">Exemplo 2: Remover todas as credenciais de uma entidade de serviço</span><span class="sxs-lookup"><span data-stu-id="6cb33-116">Example 2: Remove all credentials from a service principal</span></span>

```powershell
PS C:\> Remove-AzADSpCredential -ServicePrincipalName http://test123
```

<span data-ttu-id="6cb33-117">Remove todas as credenciais da entidade de serviço com o SPN " http://test123 ".</span><span class="sxs-lookup"><span data-stu-id="6cb33-117">Removes all credentials from the service principal with the SPN "http://test123".</span></span>

### <span data-ttu-id="6cb33-118">Exemplo 3: Remover todas as credenciais de uma entidade de serviço usando a canalização</span><span class="sxs-lookup"><span data-stu-id="6cb33-118">Example 3: Remove all credentials from a service principal using piping</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 | Remove-AzADSpCredential
```

<span data-ttu-id="6cb33-119">Obtém a entidade de serviço com a id do objeto '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82' e canalizará isso para o cmdlet Remove-AzADSpCredential para remover todas as credenciais dessa entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="6cb33-119">Gets the service principal with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82' and pipes that to the Remove-AzADSpCredential cmdlet to remove all credentials from that service principal.</span></span>

## <span data-ttu-id="6cb33-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6cb33-120">PARAMETERS</span></span>

### <span data-ttu-id="6cb33-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cb33-121">-DefaultProfile</span></span>
<span data-ttu-id="6cb33-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="6cb33-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6cb33-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="6cb33-123">-DisplayName</span></span>
<span data-ttu-id="6cb33-124">O nome de exibição da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="6cb33-124">The display name of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cb33-125">-Force</span><span class="sxs-lookup"><span data-stu-id="6cb33-125">-Force</span></span>
<span data-ttu-id="6cb33-126">Alternar para excluir credencial sem uma confirmação.</span><span class="sxs-lookup"><span data-stu-id="6cb33-126">Switch to delete credential without a confirmation.</span></span>

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

### <span data-ttu-id="6cb33-127">-KeyId</span><span class="sxs-lookup"><span data-stu-id="6cb33-127">-KeyId</span></span>
<span data-ttu-id="6cb33-128">Especifica a chave de credencial a ser removida.</span><span class="sxs-lookup"><span data-stu-id="6cb33-128">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="6cb33-129">As IDs de chave de uma entidade de serviço podem ser obtidas usando o cmdlet Get-AzADSpCredential de serviço.</span><span class="sxs-lookup"><span data-stu-id="6cb33-129">The key Ids for a service principal can be obtained using the Get-AzADSpCredential cmdlet.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdWithKeyIdParameterSet, SPNWithKeyIdParameterSet, ServicePrincipalObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cb33-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="6cb33-130">-ObjectId</span></span>
<span data-ttu-id="6cb33-131">A ID do objeto da entidade de serviço para remover as credenciais.</span><span class="sxs-lookup"><span data-stu-id="6cb33-131">The object id of the service principal to remove the credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cb33-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6cb33-132">-PassThru</span></span>
<span data-ttu-id="6cb33-133">Especificar isso retornará true se o comando tiver sido bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="6cb33-133">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="6cb33-134">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="6cb33-134">-ServicePrincipalName</span></span>
<span data-ttu-id="6cb33-135">O nome (SPN) da entidade de serviço para remover as credenciais.</span><span class="sxs-lookup"><span data-stu-id="6cb33-135">The name (SPN) of the service principal to remove the credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cb33-136">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="6cb33-136">-ServicePrincipalObject</span></span>
<span data-ttu-id="6cb33-137">O objeto principal do serviço para remover as credenciais.</span><span class="sxs-lookup"><span data-stu-id="6cb33-137">The service principal object to remove the credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal
Parameter Sets: ServicePrincipalObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6cb33-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6cb33-138">-Confirm</span></span>
<span data-ttu-id="6cb33-139">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6cb33-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6cb33-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cb33-140">-WhatIf</span></span>
<span data-ttu-id="6cb33-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6cb33-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6cb33-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6cb33-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6cb33-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cb33-143">CommonParameters</span></span>
<span data-ttu-id="6cb33-144">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cb33-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cb33-145">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6cb33-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cb33-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6cb33-146">INPUTS</span></span>

### <span data-ttu-id="6cb33-147">System.String</span><span class="sxs-lookup"><span data-stu-id="6cb33-147">System.String</span></span>

### <span data-ttu-id="6cb33-148">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="6cb33-148">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="6cb33-149">System.Guid</span><span class="sxs-lookup"><span data-stu-id="6cb33-149">System.Guid</span></span>

## <span data-ttu-id="6cb33-150">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6cb33-150">OUTPUTS</span></span>

### <span data-ttu-id="6cb33-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6cb33-151">System.Boolean</span></span>

## <span data-ttu-id="6cb33-152">NOTES</span><span class="sxs-lookup"><span data-stu-id="6cb33-152">NOTES</span></span>

## <span data-ttu-id="6cb33-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6cb33-153">RELATED LINKS</span></span>

[<span data-ttu-id="6cb33-154">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="6cb33-154">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="6cb33-155">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="6cb33-155">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="6cb33-156">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="6cb33-156">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

