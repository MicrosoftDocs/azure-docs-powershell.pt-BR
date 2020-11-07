---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 04B1E3A6-6D52-46A3-8241-2CCDB5E71642
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadspcredential
schema: 2.0.0
ms.openlocfilehash: 73fff5ff4cf612c39bacd26fed61c4e856e34128
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785154"
---
# <span data-ttu-id="059de-101">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="059de-101">Remove-AzureRmADSpCredential</span></span>

## <span data-ttu-id="059de-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="059de-102">SYNOPSIS</span></span>
<span data-ttu-id="059de-103">Remove uma credencial de uma entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="059de-103">Removes a credential from a service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="059de-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="059de-104">SYNTAX</span></span>

### <span data-ttu-id="059de-105">ObjectIdWithKeyIdParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="059de-105">ObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzureRmADSpCredential -ObjectId <Guid> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="059de-106">SPNWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="059de-106">SPNWithKeyIdParameterSet</span></span>
```
Remove-AzureRmADSpCredential -ServicePrincipalName <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="059de-107">DisplayNameWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="059de-107">DisplayNameWithKeyIdParameterSet</span></span>
```
Remove-AzureRmADSpCredential -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="059de-108">ServicePrincipalObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="059de-108">ServicePrincipalObjectParameterSet</span></span>
```
Remove-AzureRmADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-KeyId <Guid>] [-PassThru]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="059de-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="059de-109">DESCRIPTION</span></span>
<span data-ttu-id="059de-110">O cmdlet Remove-AzureRmADSpCredential pode ser usado para remover uma chave de credencial de uma entidade de serviço no caso de um comprometimento ou como parte da expiração da sobreposição da chave da credencial.</span><span class="sxs-lookup"><span data-stu-id="059de-110">The Remove-AzureRmADSpCredential cmdlet can be used to remove a credential key from a service principal in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="059de-111">A entidade de serviço é identificada fornecendo a identificação do objeto ou o SPN (nome da entidade de serviço).</span><span class="sxs-lookup"><span data-stu-id="059de-111">The service principal is identified by supplying either the object ID or service principal name (SPN).</span></span>
<span data-ttu-id="059de-112">A credencial a ser removida é identificada pela ID da chave se uma credencial individual for removida ou com uma opção ' all' para excluir todas as credenciais associadas à entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="059de-112">The credential to be removed is identified by its key ID if an individual credential is to be removed or with an 'All' switch to delete all credentials associated with the service principal.</span></span>

## <span data-ttu-id="059de-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="059de-113">EXAMPLES</span></span>

### <span data-ttu-id="059de-114">Exemplo 1: remover uma credencial específica de uma entidade de serviço</span><span class="sxs-lookup"><span data-stu-id="059de-114">Example 1 - Remove a specific credential from a service principal</span></span>

```
PS C:\> Remove-AzureRmADSpCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="059de-115">Remove a credencial com a ID da chave ' 9044423a-60a3-45ac-9ab1-09534157ebb ' da entidade de serviço com a ID de objeto ' 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 '.</span><span class="sxs-lookup"><span data-stu-id="059de-115">Removes the credential with key id '9044423a-60a3-45ac-9ab1-09534157ebb' from the service principal with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span></span>

### <span data-ttu-id="059de-116">Exemplo 2-remover todas as credenciais de uma entidade de serviço</span><span class="sxs-lookup"><span data-stu-id="059de-116">Example 2 - Remove all credentials from a service principal</span></span>

```
PS C:\> Remove-AzureRmADSpCredential -ServicePrincipalName http://test123
```

<span data-ttu-id="059de-117">Remove todas as credenciais da entidade de serviço com o SPN " http://test123 ".</span><span class="sxs-lookup"><span data-stu-id="059de-117">Removes all credentials from the service principal with the SPN "http://test123".</span></span>

### <span data-ttu-id="059de-118">Exemplo 3-remover todas as credenciais de uma entidade de serviço usando o encanamento</span><span class="sxs-lookup"><span data-stu-id="059de-118">Example 3 - Remove all credentials from a service principal using piping</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 | Remove-AzureRmADSpCredential
```

<span data-ttu-id="059de-119">Obtém a entidade de serviço com a ID de objeto ' 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 ' e canaliza-a para o cmdlet Remove-AzureRmADSpCredential para remover todas as credenciais dessa entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="059de-119">Gets the service principal with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82' and pipes that to the Remove-AzureRmADSpCredential cmdlet to remove all credentials from that service principal.</span></span>

## <span data-ttu-id="059de-120">OS</span><span class="sxs-lookup"><span data-stu-id="059de-120">PARAMETERS</span></span>

### <span data-ttu-id="059de-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="059de-121">-DefaultProfile</span></span>
<span data-ttu-id="059de-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="059de-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="059de-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="059de-123">-DisplayName</span></span>
<span data-ttu-id="059de-124">O nome de exibição da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="059de-124">The display name of the service principal.</span></span>

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

### <span data-ttu-id="059de-125">-Force</span><span class="sxs-lookup"><span data-stu-id="059de-125">-Force</span></span>
<span data-ttu-id="059de-126">Alternar para excluir credencial sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="059de-126">Switch to delete credential without a confirmation.</span></span>

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

### <span data-ttu-id="059de-127">-KeyId</span><span class="sxs-lookup"><span data-stu-id="059de-127">-KeyId</span></span>
<span data-ttu-id="059de-128">Especifica a chave de credencial a ser removida.</span><span class="sxs-lookup"><span data-stu-id="059de-128">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="059de-129">As IDs de chave para uma entidade de serviço podem ser obtidas usando o cmdlet Get-AzureRmADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="059de-129">The key Ids for a service principal can be obtained using the Get-AzureRmADSpCredential cmdlet.</span></span>

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

### <span data-ttu-id="059de-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="059de-130">-ObjectId</span></span>
<span data-ttu-id="059de-131">A ID de objeto da entidade de serviço para a qual as credenciais são removidas.</span><span class="sxs-lookup"><span data-stu-id="059de-131">The object id of the service principal to remove the credentials from.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="059de-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="059de-132">-PassThru</span></span>
<span data-ttu-id="059de-133">Se o comando foi concluído, a especificação será retorna true se o comando foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="059de-133">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="059de-134">-Serviceprincipalnamename</span><span class="sxs-lookup"><span data-stu-id="059de-134">-ServicePrincipalName</span></span>
<span data-ttu-id="059de-135">O nome (SPN) da entidade de serviço para a qual remover as credenciais.</span><span class="sxs-lookup"><span data-stu-id="059de-135">The name (SPN) of the service principal to remove the credentials from.</span></span>

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

### <span data-ttu-id="059de-136">-Serviceprincipalnameobject</span><span class="sxs-lookup"><span data-stu-id="059de-136">-ServicePrincipalObject</span></span>
<span data-ttu-id="059de-137">O objeto de entidade de serviço para o qual remover as credenciais.</span><span class="sxs-lookup"><span data-stu-id="059de-137">The service principal object to remove the credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal
Parameter Sets: ServicePrincipalObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="059de-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="059de-138">-Confirm</span></span>
<span data-ttu-id="059de-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="059de-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="059de-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="059de-140">-WhatIf</span></span>
<span data-ttu-id="059de-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="059de-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="059de-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="059de-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="059de-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="059de-143">CommonParameters</span></span>
<span data-ttu-id="059de-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="059de-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="059de-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="059de-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="059de-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="059de-146">INPUTS</span></span>

### <span data-ttu-id="059de-147">System. GUID</span><span class="sxs-lookup"><span data-stu-id="059de-147">System.Guid</span></span>

### <span data-ttu-id="059de-148">System. String</span><span class="sxs-lookup"><span data-stu-id="059de-148">System.String</span></span>

### <span data-ttu-id="059de-149">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="059de-149">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>
<span data-ttu-id="059de-150">Parâmetros: servicePrincipalName (ByValue)</span><span class="sxs-lookup"><span data-stu-id="059de-150">Parameters: ServicePrincipalObject (ByValue)</span></span>

## <span data-ttu-id="059de-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="059de-151">OUTPUTS</span></span>

### <span data-ttu-id="059de-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="059de-152">System.Boolean</span></span>

## <span data-ttu-id="059de-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="059de-153">NOTES</span></span>

## <span data-ttu-id="059de-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="059de-154">RELATED LINKS</span></span>

[<span data-ttu-id="059de-155">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="059de-155">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

[<span data-ttu-id="059de-156">New-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="059de-156">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="059de-157">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="059de-157">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

