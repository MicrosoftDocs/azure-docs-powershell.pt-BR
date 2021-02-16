---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 4DC26C26-6162-4A15-BFCB-4D2B6B52DD81
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADServicePrincipal.md
ms.openlocfilehash: 01f6b6d6ed119945af7d99bac9227c788976cbab
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398692"
---
# <span data-ttu-id="61a11-101">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="61a11-101">Get-AzADServicePrincipal</span></span>

## <span data-ttu-id="61a11-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="61a11-102">SYNOPSIS</span></span>
<span data-ttu-id="61a11-103">Filtra entidades de serviço do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="61a11-103">Filters active directory service principals.</span></span>

## <span data-ttu-id="61a11-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="61a11-104">SYNTAX</span></span>

### <span data-ttu-id="61a11-105">EmptyParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="61a11-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADServicePrincipal [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="61a11-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="61a11-106">SearchStringParameterSet</span></span>
```
Get-AzADServicePrincipal -DisplayNameBeginsWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="61a11-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="61a11-107">DisplayNameParameterSet</span></span>
```
Get-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="61a11-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="61a11-108">ObjectIdParameterSet</span></span>
```
Get-AzADServicePrincipal -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="61a11-109">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="61a11-109">ApplicationIdParameterSet</span></span>
```
Get-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="61a11-110">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="61a11-110">ApplicationObjectParameterSet</span></span>
```
Get-AzADServicePrincipal -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="61a11-111">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="61a11-111">SPNParameterSet</span></span>
```
Get-AzADServicePrincipal -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="61a11-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="61a11-112">DESCRIPTION</span></span>
<span data-ttu-id="61a11-113">Filtra entidades de serviço do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="61a11-113">Filters active directory service principals.</span></span>

## <span data-ttu-id="61a11-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="61a11-114">EXAMPLES</span></span>

### <span data-ttu-id="61a11-115">Exemplo 1 - Entidades de serviço de List AD</span><span class="sxs-lookup"><span data-stu-id="61a11-115">Example 1 - List AD service principals</span></span>

```
PS C:\> Get-AzADServicePrincipal
```

<span data-ttu-id="61a11-116">Lista todas as entidades de serviço do AD em um locatário.</span><span class="sxs-lookup"><span data-stu-id="61a11-116">Lists all AD service principals in a tenant.</span></span>

### <span data-ttu-id="61a11-117">Exemplo 2 - Listar entidades de serviço de AD usando paging</span><span class="sxs-lookup"><span data-stu-id="61a11-117">Example 2 - List AD service principals using paging</span></span>

```
PS C:\> Get-AzADServicePrincipal -First 100
```

<span data-ttu-id="61a11-118">Lista as primeiras 100 entidades de serviço do AD em um locatário.</span><span class="sxs-lookup"><span data-stu-id="61a11-118">Lists the first 100 AD service principals in a tenant.</span></span>

### <span data-ttu-id="61a11-119">Exemplo 3 - Entidades de serviço de lista por SPN</span><span class="sxs-lookup"><span data-stu-id="61a11-119">Example 3 - List service principals by SPN</span></span>

```
PS C:\> Get-AzADServicePrincipal -ServicePrincipalName 36f81fc3-b00f-48cd-8218-3879f51ff39f
```

<span data-ttu-id="61a11-120">Lista entidades de serviço com o SPN '36f81fc3-b00f-48cd-8218-3879f51ff39f'.</span><span class="sxs-lookup"><span data-stu-id="61a11-120">Lists service principals with the SPN '36f81fc3-b00f-48cd-8218-3879f51ff39f'.</span></span>

### <span data-ttu-id="61a11-121">Exemplo 4 - Listar entidades de serviço por cadeia de caracteres de pesquisa</span><span class="sxs-lookup"><span data-stu-id="61a11-121">Example 4 - List service principals by search string</span></span>

```
PS C:\> Get-AzADServicePrincipal -SearchString "Web"
```

<span data-ttu-id="61a11-122">Lista todas as entidades de serviço do AD cujo nome de exibição comece com "Web".</span><span class="sxs-lookup"><span data-stu-id="61a11-122">Lists all AD service principals whose display name start with "Web".</span></span>

### <span data-ttu-id="61a11-123">Exemplo 5 - Listar entidades de serviço por piping</span><span class="sxs-lookup"><span data-stu-id="61a11-123">Example 5 - List service principals by piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69 | Get-AzADServicePrincipal
```

<span data-ttu-id="61a11-124">Obtém o aplicativo AD com a ID do objeto '39e64ec6-569b-4030-8e1c-c3c519a05d69' e o leva para o cmdlet Get-AzADServicePrincipal para listar todos os princípios de serviço para esse aplicativo.</span><span class="sxs-lookup"><span data-stu-id="61a11-124">Gets the AD application with object id '39e64ec6-569b-4030-8e1c-c3c519a05d69' and pipes it to the Get-AzADServicePrincipal cmdlet to list all service principals for that application.</span></span>

## <span data-ttu-id="61a11-125">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="61a11-125">PARAMETERS</span></span>

### <span data-ttu-id="61a11-126">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="61a11-126">-ApplicationId</span></span>
<span data-ttu-id="61a11-127">A ID do aplicativo principal do serviço.</span><span class="sxs-lookup"><span data-stu-id="61a11-127">The service principal application id.</span></span>

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

### <span data-ttu-id="61a11-128">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="61a11-128">-ApplicationObject</span></span>
<span data-ttu-id="61a11-129">O objeto do aplicativo cuja entidade de serviço está sendo recuperada.</span><span class="sxs-lookup"><span data-stu-id="61a11-129">The application object whose service principal is being retrieved.</span></span>

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

### <span data-ttu-id="61a11-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61a11-130">-DefaultProfile</span></span>
<span data-ttu-id="61a11-131">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="61a11-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="61a11-132">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="61a11-132">-DisplayName</span></span>
<span data-ttu-id="61a11-133">O nome de exibição da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="61a11-133">The service principal display name.</span></span>

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

### <span data-ttu-id="61a11-134">-DisplayNameBeginsWith</span><span class="sxs-lookup"><span data-stu-id="61a11-134">-DisplayNameBeginsWith</span></span>
<span data-ttu-id="61a11-135">A cadeia de caracteres de pesquisa da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="61a11-135">The service principal search string.</span></span>

```yaml
Type: System.String
Parameter Sets: SearchStringParameterSet
Aliases: SearchString

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61a11-136">-First</span><span class="sxs-lookup"><span data-stu-id="61a11-136">-First</span></span>
<span data-ttu-id="61a11-137">O número máximo de objetos a retornar.</span><span class="sxs-lookup"><span data-stu-id="61a11-137">The maximum number of objects to return.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61a11-138">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="61a11-138">-IncludeTotalCount</span></span>
<span data-ttu-id="61a11-139">Relata o número de objetos no conjunto de dados.</span><span class="sxs-lookup"><span data-stu-id="61a11-139">Reports the number of objects in the data set.</span></span> <span data-ttu-id="61a11-140">Atualmente, esse parâmetro não faz nada.</span><span class="sxs-lookup"><span data-stu-id="61a11-140">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="61a11-141">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="61a11-141">-ObjectId</span></span>
<span data-ttu-id="61a11-142">ID do objeto da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="61a11-142">Object id of the service principal.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61a11-143">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="61a11-143">-ServicePrincipalName</span></span>
<span data-ttu-id="61a11-144">SPN do serviço.</span><span class="sxs-lookup"><span data-stu-id="61a11-144">SPN of the service.</span></span>

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

### <span data-ttu-id="61a11-145">-Ignorar</span><span class="sxs-lookup"><span data-stu-id="61a11-145">-Skip</span></span>
<span data-ttu-id="61a11-146">Ignora os primeiros objetos N e obtém os objetos restantes.</span><span class="sxs-lookup"><span data-stu-id="61a11-146">Ignores the first N objects and then gets the remaining objects.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61a11-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61a11-147">CommonParameters</span></span>
<span data-ttu-id="61a11-148">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61a11-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61a11-149">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61a11-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61a11-150">Entradas</span><span class="sxs-lookup"><span data-stu-id="61a11-150">INPUTS</span></span>

### <span data-ttu-id="61a11-151">System.String</span><span class="sxs-lookup"><span data-stu-id="61a11-151">System.String</span></span>

### <span data-ttu-id="61a11-152">System.Guid</span><span class="sxs-lookup"><span data-stu-id="61a11-152">System.Guid</span></span>

### <span data-ttu-id="61a11-153">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="61a11-153">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="61a11-154">Parâmetros: ApplicationObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="61a11-154">Parameters: ApplicationObject (ByValue)</span></span>

## <span data-ttu-id="61a11-155">Saídas</span><span class="sxs-lookup"><span data-stu-id="61a11-155">OUTPUTS</span></span>

### <span data-ttu-id="61a11-156">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="61a11-156">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="61a11-157">Notas</span><span class="sxs-lookup"><span data-stu-id="61a11-157">NOTES</span></span>

## <span data-ttu-id="61a11-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="61a11-158">RELATED LINKS</span></span>

[<span data-ttu-id="61a11-159">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="61a11-159">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)


[<span data-ttu-id="61a11-160">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="61a11-160">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="61a11-161">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="61a11-161">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="61a11-162">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="61a11-162">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

