---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 4DC26C26-6162-4A15-BFCB-4D2B6B52DD81
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadserviceprincipal
schema: 2.0.0
ms.openlocfilehash: 10d95102058c759f9b2641f233bd590364945c71
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785628"
---
# <span data-ttu-id="dcc3c-101">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="dcc3c-101">Get-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="dcc3c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dcc3c-102">SYNOPSIS</span></span>
<span data-ttu-id="dcc3c-103">Filtra as entidades de serviço do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="dcc3c-103">Filters active directory service principals.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dcc3c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dcc3c-104">SYNTAX</span></span>

### <span data-ttu-id="dcc3c-105">EmptyParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="dcc3c-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADServicePrincipal [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="dcc3c-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="dcc3c-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -DisplayNameBeginsWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="dcc3c-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="dcc3c-107">DisplayNameParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="dcc3c-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dcc3c-108">ObjectIdParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="dcc3c-109">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dcc3c-109">ApplicationIdParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="dcc3c-110">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dcc3c-110">ApplicationObjectParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="dcc3c-111">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="dcc3c-111">SPNParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="dcc3c-112">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dcc3c-112">DESCRIPTION</span></span>
<span data-ttu-id="dcc3c-113">Filtra as entidades de serviço do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="dcc3c-113">Filters active directory service principals.</span></span>

## <span data-ttu-id="dcc3c-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dcc3c-114">EXAMPLES</span></span>

### <span data-ttu-id="dcc3c-115">Exemplo 1-lista de entidades de serviço de anúncios</span><span class="sxs-lookup"><span data-stu-id="dcc3c-115">Example 1 - List AD service principals</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal
```

<span data-ttu-id="dcc3c-116">Lista todas as entidades de serviço de anúncio em um locatário.</span><span class="sxs-lookup"><span data-stu-id="dcc3c-116">Lists all AD service principals in a tenant.</span></span>

### <span data-ttu-id="dcc3c-117">Exemplo 2-lista de entidades de serviço de anúncios usando paginação</span><span class="sxs-lookup"><span data-stu-id="dcc3c-117">Example 2 - List AD service principals using paging</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal -First 100
```

<span data-ttu-id="dcc3c-118">Lista as primeiras entidades de serviço do anúncio do 100 em um locatário.</span><span class="sxs-lookup"><span data-stu-id="dcc3c-118">Lists the first 100 AD service principals in a tenant.</span></span>

### <span data-ttu-id="dcc3c-119">Exemplo de entidades de serviço de 3 listas por SPN</span><span class="sxs-lookup"><span data-stu-id="dcc3c-119">Example 3 - List service principals by SPN</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal -ServicePrincipalName 36f81fc3-b00f-48cd-8218-3879f51ff39f
```

<span data-ttu-id="dcc3c-120">Lista as entidades de serviço com o SPN ' 36f81fc3-b00f-48CD-8218-3879f51ff39f '.</span><span class="sxs-lookup"><span data-stu-id="dcc3c-120">Lists service principals with the SPN '36f81fc3-b00f-48cd-8218-3879f51ff39f'.</span></span>

### <span data-ttu-id="dcc3c-121">Exemplo de entidades de serviço de 4 listas por cadeia de pesquisa</span><span class="sxs-lookup"><span data-stu-id="dcc3c-121">Example 4 - List service principals by search string</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal -SearchString "Web"
```

<span data-ttu-id="dcc3c-122">Lista todas as entidades de serviço de anúncio cujo nome para exibição comece com "Web".</span><span class="sxs-lookup"><span data-stu-id="dcc3c-122">Lists all AD service principals whose display name start with "Web".</span></span>

### <span data-ttu-id="dcc3c-123">Exemplo de entidades de serviço de 5 listas por tubulação</span><span class="sxs-lookup"><span data-stu-id="dcc3c-123">Example 5 - List service principals by piping</span></span>

```
PS C:\> Get-AzureRmADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69 | Get-AzureRmADServicePrincipal
```

<span data-ttu-id="dcc3c-124">Obtém o aplicativo do anúncio com a ID de objeto ' 39e64ec6-569B-4030-8e1c-c3c519a05d69 ' e a canaliza para o cmdlet Get-AzureRmADServicePrincipal para listar todas as entidades de serviço desse aplicativo.</span><span class="sxs-lookup"><span data-stu-id="dcc3c-124">Gets the AD application with object id '39e64ec6-569b-4030-8e1c-c3c519a05d69' and pipes it to the Get-AzureRmADServicePrincipal cmdlet to list all service principals for that application.</span></span>

## <span data-ttu-id="dcc3c-125">OS</span><span class="sxs-lookup"><span data-stu-id="dcc3c-125">PARAMETERS</span></span>

### <span data-ttu-id="dcc3c-126">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="dcc3c-126">-ApplicationId</span></span>
<span data-ttu-id="dcc3c-127">A ID do aplicativo principal do serviço.</span><span class="sxs-lookup"><span data-stu-id="dcc3c-127">The service principal application id.</span></span>

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

### <span data-ttu-id="dcc3c-128">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="dcc3c-128">-ApplicationObject</span></span>
<span data-ttu-id="dcc3c-129">O objeto de aplicativo cuja entidade de serviço está sendo recuperada.</span><span class="sxs-lookup"><span data-stu-id="dcc3c-129">The application object whose service principal is being retrieved.</span></span>

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

### <span data-ttu-id="dcc3c-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcc3c-130">-DefaultProfile</span></span>
<span data-ttu-id="dcc3c-131">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="dcc3c-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dcc3c-132">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="dcc3c-132">-DisplayName</span></span>
<span data-ttu-id="dcc3c-133">O nome de exibição da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="dcc3c-133">The service principal display name.</span></span>

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

### <span data-ttu-id="dcc3c-134">-DisplayNameBeginsWith</span><span class="sxs-lookup"><span data-stu-id="dcc3c-134">-DisplayNameBeginsWith</span></span>
<span data-ttu-id="dcc3c-135">A cadeia de caracteres de pesquisa principal do serviço.</span><span class="sxs-lookup"><span data-stu-id="dcc3c-135">The service principal search string.</span></span>

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

### <span data-ttu-id="dcc3c-136">-Primeiro</span><span class="sxs-lookup"><span data-stu-id="dcc3c-136">-First</span></span>
<span data-ttu-id="dcc3c-137">O número máximo de objetos a serem retornados.</span><span class="sxs-lookup"><span data-stu-id="dcc3c-137">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="dcc3c-138">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="dcc3c-138">-IncludeTotalCount</span></span>
<span data-ttu-id="dcc3c-139">Informa o número de objetos no conjunto de dados.</span><span class="sxs-lookup"><span data-stu-id="dcc3c-139">Reports the number of objects in the data set.</span></span> <span data-ttu-id="dcc3c-140">Atualmente, esse parâmetro não faz nada.</span><span class="sxs-lookup"><span data-stu-id="dcc3c-140">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="dcc3c-141">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="dcc3c-141">-ObjectId</span></span>
<span data-ttu-id="dcc3c-142">ID de objeto da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="dcc3c-142">Object id of the service principal.</span></span>

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

### <span data-ttu-id="dcc3c-143">-Serviceprincipalnamename</span><span class="sxs-lookup"><span data-stu-id="dcc3c-143">-ServicePrincipalName</span></span>
<span data-ttu-id="dcc3c-144">SPN do serviço.</span><span class="sxs-lookup"><span data-stu-id="dcc3c-144">SPN of the service.</span></span>

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

### <span data-ttu-id="dcc3c-145">-Skip</span><span class="sxs-lookup"><span data-stu-id="dcc3c-145">-Skip</span></span>
<span data-ttu-id="dcc3c-146">Ignora os primeiros N objetos e, em seguida, obtém os objetos restantes.</span><span class="sxs-lookup"><span data-stu-id="dcc3c-146">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="dcc3c-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcc3c-147">CommonParameters</span></span>
<span data-ttu-id="dcc3c-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcc3c-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcc3c-149">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcc3c-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcc3c-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dcc3c-150">INPUTS</span></span>

### <span data-ttu-id="dcc3c-151">System. String</span><span class="sxs-lookup"><span data-stu-id="dcc3c-151">System.String</span></span>

### <span data-ttu-id="dcc3c-152">System. GUID</span><span class="sxs-lookup"><span data-stu-id="dcc3c-152">System.Guid</span></span>

### <span data-ttu-id="dcc3c-153">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="dcc3c-153">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="dcc3c-154">Parâmetros: applicationObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="dcc3c-154">Parameters: ApplicationObject (ByValue)</span></span>

## <span data-ttu-id="dcc3c-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dcc3c-155">OUTPUTS</span></span>

### <span data-ttu-id="dcc3c-156">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="dcc3c-156">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="dcc3c-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dcc3c-157">NOTES</span></span>

## <span data-ttu-id="dcc3c-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dcc3c-158">RELATED LINKS</span></span>

[<span data-ttu-id="dcc3c-159">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="dcc3c-159">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)



[<span data-ttu-id="dcc3c-160">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="dcc3c-160">Remove-AzureRmADServicePrincipal</span></span>](./Remove-AzureRmADServicePrincipal.md)

[<span data-ttu-id="dcc3c-161">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="dcc3c-161">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="dcc3c-162">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="dcc3c-162">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

