---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 4DC26C26-6162-4A15-BFCB-4D2B6B52DD81
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADServicePrincipal.md
ms.openlocfilehash: 983d5049d0ac58671b3d0766b6b4bcf3f05d4d76
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430059"
---
# <span data-ttu-id="b3dc2-101">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b3dc2-101">Get-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="b3dc2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b3dc2-102">SYNOPSIS</span></span>
<span data-ttu-id="b3dc2-103">Filtra as entidades de serviço do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b3dc2-103">Filters active directory service principals.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3dc2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b3dc2-104">SYNTAX</span></span>

### <span data-ttu-id="b3dc2-105">EmptyParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="b3dc2-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADServicePrincipal [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="b3dc2-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3dc2-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -DisplayNameBeginsWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="b3dc2-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3dc2-107">DisplayNameParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="b3dc2-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3dc2-108">ObjectIdParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="b3dc2-109">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3dc2-109">ApplicationIdParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="b3dc2-110">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3dc2-110">ApplicationObjectParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="b3dc2-111">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3dc2-111">SPNParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="b3dc2-112">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b3dc2-112">DESCRIPTION</span></span>
<span data-ttu-id="b3dc2-113">Filtra as entidades de serviço do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b3dc2-113">Filters active directory service principals.</span></span>

## <span data-ttu-id="b3dc2-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b3dc2-114">EXAMPLES</span></span>

### <span data-ttu-id="b3dc2-115">Exemplo 1-lista de entidades de serviço de anúncios</span><span class="sxs-lookup"><span data-stu-id="b3dc2-115">Example 1 - List AD service principals</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal
```

<span data-ttu-id="b3dc2-116">Lista todas as entidades de serviço de anúncio em um locatário.</span><span class="sxs-lookup"><span data-stu-id="b3dc2-116">Lists all AD service principals in a tenant.</span></span>

### <span data-ttu-id="b3dc2-117">Exemplo 2-lista de entidades de serviço de anúncios usando paginação</span><span class="sxs-lookup"><span data-stu-id="b3dc2-117">Example 2 - List AD service principals using paging</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal -First 100
```

<span data-ttu-id="b3dc2-118">Lista as primeiras entidades de serviço do anúncio do 100 em um locatário.</span><span class="sxs-lookup"><span data-stu-id="b3dc2-118">Lists the first 100 AD service principals in a tenant.</span></span>

### <span data-ttu-id="b3dc2-119">Exemplo de entidades de serviço de 3 listas por SPN</span><span class="sxs-lookup"><span data-stu-id="b3dc2-119">Example 3 - List service principals by SPN</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal -ServicePrincipalName 36f81fc3-b00f-48cd-8218-3879f51ff39f
```

<span data-ttu-id="b3dc2-120">Lista as entidades de serviço com o SPN ' 36f81fc3-b00f-48CD-8218-3879f51ff39f '.</span><span class="sxs-lookup"><span data-stu-id="b3dc2-120">Lists service principals with the SPN '36f81fc3-b00f-48cd-8218-3879f51ff39f'.</span></span>

### <span data-ttu-id="b3dc2-121">Exemplo de entidades de serviço de 4 listas por cadeia de pesquisa</span><span class="sxs-lookup"><span data-stu-id="b3dc2-121">Example 4 - List service principals by search string</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal -SearchString "Web"
```

<span data-ttu-id="b3dc2-122">Lista todas as entidades de serviço de anúncio cujo nome para exibição comece com "Web".</span><span class="sxs-lookup"><span data-stu-id="b3dc2-122">Lists all AD service principals whose display name start with "Web".</span></span>

### <span data-ttu-id="b3dc2-123">Exemplo de entidades de serviço de 5 listas por tubulação</span><span class="sxs-lookup"><span data-stu-id="b3dc2-123">Example 5 - List service principals by piping</span></span>

```
PS C:\> Get-AzureRmADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69 | Get-AzureRmADServicePrincipal
```

<span data-ttu-id="b3dc2-124">Obtém o aplicativo do anúncio com a ID de objeto ' 39e64ec6-569B-4030-8e1c-c3c519a05d69 ' e a canaliza para o cmdlet Get-AzureRmADServicePrincipal para listar todas as entidades de serviço desse aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b3dc2-124">Gets the AD application with object id '39e64ec6-569b-4030-8e1c-c3c519a05d69' and pipes it to the Get-AzureRmADServicePrincipal cmdlet to list all service principals for that application.</span></span>

## <span data-ttu-id="b3dc2-125">OS</span><span class="sxs-lookup"><span data-stu-id="b3dc2-125">PARAMETERS</span></span>

### <span data-ttu-id="b3dc2-126">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="b3dc2-126">-ApplicationId</span></span>
<span data-ttu-id="b3dc2-127">A ID do aplicativo principal do serviço.</span><span class="sxs-lookup"><span data-stu-id="b3dc2-127">The service principal application id.</span></span>

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

### <span data-ttu-id="b3dc2-128">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="b3dc2-128">-ApplicationObject</span></span>
<span data-ttu-id="b3dc2-129">O objeto de aplicativo cuja entidade de serviço está sendo recuperada.</span><span class="sxs-lookup"><span data-stu-id="b3dc2-129">The application object whose service principal is being retrieved.</span></span>

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

### <span data-ttu-id="b3dc2-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3dc2-130">-DefaultProfile</span></span>
<span data-ttu-id="b3dc2-131">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="b3dc2-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b3dc2-132">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b3dc2-132">-DisplayName</span></span>
<span data-ttu-id="b3dc2-133">O nome de exibição da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="b3dc2-133">The service principal display name.</span></span>

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

### <span data-ttu-id="b3dc2-134">-DisplayNameBeginsWith</span><span class="sxs-lookup"><span data-stu-id="b3dc2-134">-DisplayNameBeginsWith</span></span>
<span data-ttu-id="b3dc2-135">A cadeia de caracteres de pesquisa principal do serviço.</span><span class="sxs-lookup"><span data-stu-id="b3dc2-135">The service principal search string.</span></span>

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

### <span data-ttu-id="b3dc2-136">-Primeiro</span><span class="sxs-lookup"><span data-stu-id="b3dc2-136">-First</span></span>
<span data-ttu-id="b3dc2-137">O número máximo de objetos a serem retornados.</span><span class="sxs-lookup"><span data-stu-id="b3dc2-137">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="b3dc2-138">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="b3dc2-138">-IncludeTotalCount</span></span>
<span data-ttu-id="b3dc2-139">Informa o número de objetos no conjunto de dados.</span><span class="sxs-lookup"><span data-stu-id="b3dc2-139">Reports the number of objects in the data set.</span></span> <span data-ttu-id="b3dc2-140">Atualmente, esse parâmetro não faz nada.</span><span class="sxs-lookup"><span data-stu-id="b3dc2-140">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="b3dc2-141">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="b3dc2-141">-ObjectId</span></span>
<span data-ttu-id="b3dc2-142">ID de objeto da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="b3dc2-142">Object id of the service principal.</span></span>

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

### <span data-ttu-id="b3dc2-143">-Serviceprincipalnamename</span><span class="sxs-lookup"><span data-stu-id="b3dc2-143">-ServicePrincipalName</span></span>
<span data-ttu-id="b3dc2-144">SPN do serviço.</span><span class="sxs-lookup"><span data-stu-id="b3dc2-144">SPN of the service.</span></span>

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

### <span data-ttu-id="b3dc2-145">-Skip</span><span class="sxs-lookup"><span data-stu-id="b3dc2-145">-Skip</span></span>
<span data-ttu-id="b3dc2-146">Ignora os primeiros N objetos e, em seguida, obtém os objetos restantes.</span><span class="sxs-lookup"><span data-stu-id="b3dc2-146">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="b3dc2-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3dc2-147">CommonParameters</span></span>
<span data-ttu-id="b3dc2-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3dc2-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3dc2-149">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3dc2-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3dc2-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b3dc2-150">INPUTS</span></span>

### <span data-ttu-id="b3dc2-151">System. String</span><span class="sxs-lookup"><span data-stu-id="b3dc2-151">System.String</span></span>

### <span data-ttu-id="b3dc2-152">System. GUID</span><span class="sxs-lookup"><span data-stu-id="b3dc2-152">System.Guid</span></span>

### <span data-ttu-id="b3dc2-153">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="b3dc2-153">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="b3dc2-154">Parâmetros: applicationObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b3dc2-154">Parameters: ApplicationObject (ByValue)</span></span>

## <span data-ttu-id="b3dc2-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b3dc2-155">OUTPUTS</span></span>

### <span data-ttu-id="b3dc2-156">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b3dc2-156">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="b3dc2-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b3dc2-157">NOTES</span></span>

## <span data-ttu-id="b3dc2-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b3dc2-158">RELATED LINKS</span></span>

[<span data-ttu-id="b3dc2-159">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b3dc2-159">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="b3dc2-160">Set-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b3dc2-160">Set-AzureRmADServicePrincipal</span></span>](./Set-AzureRmADServicePrincipal.md)

[<span data-ttu-id="b3dc2-161">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b3dc2-161">Remove-AzureRmADServicePrincipal</span></span>](./Remove-AzureRmADServicePrincipal.md)

[<span data-ttu-id="b3dc2-162">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="b3dc2-162">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="b3dc2-163">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="b3dc2-163">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

