---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 04B1E3A6-6D52-46A3-8241-2CCDB5E71642
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADSpCredential.md
ms.openlocfilehash: d40c1a3a5e626d364986352f95bc914b31ced969
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773324"
---
# <span data-ttu-id="f862c-101">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="f862c-101">Remove-AzADSpCredential</span></span>

## <span data-ttu-id="f862c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f862c-102">SYNOPSIS</span></span>
<span data-ttu-id="f862c-103">Remove uma credencial de uma entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="f862c-103">Removes a credential from a service principal.</span></span>

## <span data-ttu-id="f862c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f862c-104">SYNTAX</span></span>

### <span data-ttu-id="f862c-105">ObjectIdWithKeyIdParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="f862c-105">ObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzADSpCredential -ObjectId <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f862c-106">SPNWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f862c-106">SPNWithKeyIdParameterSet</span></span>
```
Remove-AzADSpCredential -ServicePrincipalName <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f862c-107">DisplayNameWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f862c-107">DisplayNameWithKeyIdParameterSet</span></span>
```
Remove-AzADSpCredential -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f862c-108">ServicePrincipalObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f862c-108">ServicePrincipalObjectParameterSet</span></span>
```
Remove-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f862c-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f862c-109">DESCRIPTION</span></span>
<span data-ttu-id="f862c-110">O cmdlet Remove-AzADSpCredential pode ser usado para remover uma chave de credencial de uma entidade de serviço no caso de um comprometimento ou como parte da expiração da sobreposição da chave da credencial.</span><span class="sxs-lookup"><span data-stu-id="f862c-110">The Remove-AzADSpCredential cmdlet can be used to remove a credential key from a service principal in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="f862c-111">A entidade de serviço é identificada fornecendo a identificação do objeto ou o SPN (nome da entidade de serviço).</span><span class="sxs-lookup"><span data-stu-id="f862c-111">The service principal is identified by supplying either the object ID or service principal name (SPN).</span></span>
<span data-ttu-id="f862c-112">A credencial a ser removida é identificada pela ID da chave se uma credencial individual for removida ou com uma opção ' all' para excluir todas as credenciais associadas à entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="f862c-112">The credential to be removed is identified by its key ID if an individual credential is to be removed or with an 'All' switch to delete all credentials associated with the service principal.</span></span>

## <span data-ttu-id="f862c-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f862c-113">EXAMPLES</span></span>

### <span data-ttu-id="f862c-114">Exemplo 1: remover uma credencial específica de uma entidade de serviço</span><span class="sxs-lookup"><span data-stu-id="f862c-114">Example 1 - Remove a specific credential from a service principal</span></span>

```
PS C:\> Remove-AzADSpCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="f862c-115">Remove a credencial com a ID da chave ' 9044423a-60a3-45ac-9ab1-09534157ebb ' da entidade de serviço com a ID de objeto ' 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 '.</span><span class="sxs-lookup"><span data-stu-id="f862c-115">Removes the credential with key id '9044423a-60a3-45ac-9ab1-09534157ebb' from the service principal with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span></span>

### <span data-ttu-id="f862c-116">Exemplo 2-remover todas as credenciais de uma entidade de serviço</span><span class="sxs-lookup"><span data-stu-id="f862c-116">Example 2 - Remove all credentials from a service principal</span></span>

```
PS C:\> Remove-AzADSpCredential -ServicePrincipalName http://test123
```

<span data-ttu-id="f862c-117">Remove todas as credenciais da entidade de serviço com o SPN " http://test123 ".</span><span class="sxs-lookup"><span data-stu-id="f862c-117">Removes all credentials from the service principal with the SPN "http://test123".</span></span>

### <span data-ttu-id="f862c-118">Exemplo 3-remover todas as credenciais de uma entidade de serviço usando o encanamento</span><span class="sxs-lookup"><span data-stu-id="f862c-118">Example 3 - Remove all credentials from a service principal using piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 | Remove-AzADSpCredential
```

<span data-ttu-id="f862c-119">Obtém a entidade de serviço com a ID de objeto ' 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 ' e canaliza-a para o cmdlet Remove-AzADSpCredential para remover todas as credenciais dessa entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="f862c-119">Gets the service principal with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82' and pipes that to the Remove-AzADSpCredential cmdlet to remove all credentials from that service principal.</span></span>

## <span data-ttu-id="f862c-120">OS</span><span class="sxs-lookup"><span data-stu-id="f862c-120">PARAMETERS</span></span>

### <span data-ttu-id="f862c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f862c-121">-DefaultProfile</span></span>
<span data-ttu-id="f862c-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="f862c-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f862c-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f862c-123">-DisplayName</span></span>
<span data-ttu-id="f862c-124">O nome de exibição da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="f862c-124">The display name of the service principal.</span></span>

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

### <span data-ttu-id="f862c-125">-Force</span><span class="sxs-lookup"><span data-stu-id="f862c-125">-Force</span></span>
<span data-ttu-id="f862c-126">Alternar para excluir credencial sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="f862c-126">Switch to delete credential without a confirmation.</span></span>

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

### <span data-ttu-id="f862c-127">-KeyId</span><span class="sxs-lookup"><span data-stu-id="f862c-127">-KeyId</span></span>
<span data-ttu-id="f862c-128">Especifica a chave de credencial a ser removida.</span><span class="sxs-lookup"><span data-stu-id="f862c-128">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="f862c-129">As IDs de chave para uma entidade de serviço podem ser obtidas usando o cmdlet Get-AzADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="f862c-129">The key Ids for a service principal can be obtained using the Get-AzADSpCredential cmdlet.</span></span>

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

### <span data-ttu-id="f862c-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="f862c-130">-ObjectId</span></span>
<span data-ttu-id="f862c-131">A ID de objeto da entidade de serviço para a qual as credenciais são removidas.</span><span class="sxs-lookup"><span data-stu-id="f862c-131">The object id of the service principal to remove the credentials from.</span></span>

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

### <span data-ttu-id="f862c-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f862c-132">-PassThru</span></span>
<span data-ttu-id="f862c-133">Se o comando foi concluído, a especificação será retorna true se o comando foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="f862c-133">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="f862c-134">-Serviceprincipalnamename</span><span class="sxs-lookup"><span data-stu-id="f862c-134">-ServicePrincipalName</span></span>
<span data-ttu-id="f862c-135">O nome (SPN) da entidade de serviço para a qual remover as credenciais.</span><span class="sxs-lookup"><span data-stu-id="f862c-135">The name (SPN) of the service principal to remove the credentials from.</span></span>

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

### <span data-ttu-id="f862c-136">-Serviceprincipalnameobject</span><span class="sxs-lookup"><span data-stu-id="f862c-136">-ServicePrincipalObject</span></span>
<span data-ttu-id="f862c-137">O objeto de entidade de serviço para o qual remover as credenciais.</span><span class="sxs-lookup"><span data-stu-id="f862c-137">The service principal object to remove the credentials from.</span></span>

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

### <span data-ttu-id="f862c-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f862c-138">-Confirm</span></span>
<span data-ttu-id="f862c-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f862c-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f862c-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f862c-140">-WhatIf</span></span>
<span data-ttu-id="f862c-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f862c-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f862c-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f862c-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f862c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f862c-143">CommonParameters</span></span>
<span data-ttu-id="f862c-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f862c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f862c-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f862c-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f862c-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f862c-146">INPUTS</span></span>

### <span data-ttu-id="f862c-147">System. String</span><span class="sxs-lookup"><span data-stu-id="f862c-147">System.String</span></span>

### <span data-ttu-id="f862c-148">Microsoft. Azure. Commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="f862c-148">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="f862c-149">System. GUID</span><span class="sxs-lookup"><span data-stu-id="f862c-149">System.Guid</span></span>

## <span data-ttu-id="f862c-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f862c-150">OUTPUTS</span></span>

### <span data-ttu-id="f862c-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f862c-151">System.Boolean</span></span>

## <span data-ttu-id="f862c-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f862c-152">NOTES</span></span>

## <span data-ttu-id="f862c-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f862c-153">RELATED LINKS</span></span>

[<span data-ttu-id="f862c-154">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="f862c-154">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="f862c-155">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="f862c-155">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="f862c-156">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="f862c-156">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)
